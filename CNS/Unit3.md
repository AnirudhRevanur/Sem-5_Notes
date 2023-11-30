# Unit 3

## Remote DNS Attack
- ___Challenges:___ For remot attackers who are not on th same network as the local DNS Server, spoofing replies becomes much more difficult, as they cannot see the DNS Query
1. Attacker needs to guess:
  - Source port number (16-bit random number)
  - Transaction ID (16-bit random number)
  - Probability of a good guess is 1 in $`2^32`$
2. Time of spoofing:
  - How do you know when the DNS request is sent?
  - TO overcome this, we can trigger a request to the DNS server
3. Cache Effect:
  - If one attempt fails, then the actual reply will be cached by local DNS server
  - Attacker needs to wait for the cache to timeout for the next attempt
  - This waiting period can be hours, days or weeks
- Due to these challenges, remote attacks were considered not feasible

- To launch the attacks, we need to accomplish 3 tasks:
  1. Trigger DNS Server(Apollo) to send out the DNS Query
  2. Spoof the Reply
  3. Negate the Cache Effect
- Negating the Cache is the important part, as without that it is impossible to perform the attack

![DNS](DNS.png "DNS Server")


### What should be in spoofed reply?
- ___Kaminsky's Idea:___
  - Look away from the answer section
  - Use the authority section to provide nameserver
  - Tell Apollo that the name server for example.com is ns.attacker32.com (Attacker machine)
  - After this information is cached, Apollo will query the attacker's machine whenever it needs resolve a hostname in this domain

### What query should be used to trigger attack?
- The domain used in the authority section must be related the the query section
  - The query should be a host within example.com domain
- To trigger Apollo to keep sending queries, Apollo must be asked different questions
  - Query Apollo for a random name in example.com domain
  - Answer will not be in Apollo's cache, so it will query to the root server, then .com, then nameserver of example.com
  - While Apollo waits for the reply, attacker floods Apollo with stream of Spoofed DNS replies each with different Transaction ID and Port Number
- If the spoofed response fails, then the attacker will repeat the entire process, but use a different host name
- If attack successds, then the nameserver for example.com will be replaced by the attacker's nameserver


### Implementation

|Language|Code|Speed|
|:--:|:--:|:--:|
|__C/C++__|Difficult|High|
|__Python__|Easy|Low|

- Use a hybrid approach to launch the attack
- Use Python to construct the packet and use C to send out the pre-built packet


## Protection Against DNS Cache Poisoning

- Arnold writes a document
  - Doc is passed to a hashing algo and a digest is created
  - Digest is encrypted using Arnold's Private Key
    - This is known as Digital Signature
- Arnold sends the original document + Digital Signature to Jamie
- Jamie does the following
  - Hashes the document to a digest using the same hashing algorithm
  - Decrypts the Digital Signature using Arnold's Public Key and gets the digest
  - If the digests match, then the document actually came from Arnold, as the document was signed using Arnold's Private Key

### DNSSEC
- It is a set of extension to DNS
- DNSSEC strengthens the authentication and ensures data integrity in DNS using Digital Signature
- With DNSSEC, DNS data is signed by the owner of the data
  - All answers from DNSSEC protected zones are digitally signed
- DNSSEC allows a resolver of name server to verify the authenticity and integrity of DNS Response by establishing a _"chain of trust"_ to the source of DNS data and validating the digital signatures
- Cache poisoning will be defeated by this mechanism as any fake data will be detected because they will fail the signature checking
- To maintain data origint authenticity, both servers and resolvers should use DNSSEC

- ___Idea in simple:___
  - Every DNS Zone has a public/private key pair
  - Zone owner uses the private key to sign DNS data and generate digital signatures
  - "Private key" is known only to the zone owner
  - Public Key is published in the zone for anyone to retrieve

- ___Trusting DNSSEC Keys:___
  - Every zone publishes its Public Key
  - How can a resolver ensure that a zone's public key is authentic?
  - The public key is signed by the __parent zone's private key__
  - Just as a DNS Zone's parent is responisble for publishing a child zone's list of authoritative name servers, a zone's parent is also responsible for vouching for the authenticity of its child zone's public key
  - Every zone's public key is signed by its parent zone, except for the root zone

- ___Root Zone's Public Key___
  - Root zone's public key is an important starting point for validating  DNS data
  - Sequence of cryptographic keys signing other cryptographic keys is called a __chain of trust__
  - The public key at the beginning of a chain is called as __trust anchor__
  - Most resolvers are configured with just one anchor
  - By trusting this key at the top of the DNS Hierarchy, a resolver can build a chain of trust to any location in the DNS name space


#### Terminology
- A nameserver digitally signs a zone with 2 key pairs
  - Zone signing key: Used to sign/verify the records
  - Key signing key: Used to sign/verify the zone keys

- DNSSEC Resource Record Types:
  - DNS Public Key Resource Records: Holds the Public Zone signing key and Public Key signing key
  - Resource Record Signature(RRSIG): RR sets digitally signed by either PrivateZSK or PrivateKSK
  - Next Secure records(NSEC/NSEC3): Next nameserver to refer to
  - Delegation Signer Resource Records(DSRR): To authenticate PublicKSK of child zone. Has the hash digest of the child zone's PubKSK

#### DNSSEC Working
- DNS Resolver initiates an iterative query to a Root Zone
- Root Zone replies to the DNS resolver with the five records:
  1. NSEC RR for the next name server
  2. DNSKEY RR set for root zone
  3. RRSIG of above DNSKEY RR set signed by root's PrivateKSK
  4. DSRR for the zone
  5. RRSIG of above DS RR signed by Root's PvtZSK
- On receiving the above RRs from the Root Zone, the resolver
  - Verifies the RR sets using the Root's PubKSK
    - Get the root's PubKSK and PubZSK from DNSKEY RR
  - Verifies the Root Zone
    - DNS resolver has a trusted copy of root zone's PubKSK
    - Decrypts the RRSig record containing the DS Record using PubZSK
- DNS resolver now initiates a query to a .net/.com/.in zone
- .net/.com zone replies to DNS resolver with the 4 Resource Records
  - You get everything except for the first one
- On receiving the above RRs from example.net zone, the DNS resolver
  - Verifies the records
  - Verifies the zone
- On successful authentication, the DNS resolver replies the user with the IP address of the website being requested

#### Purpose of DNSSEC
- It is to authenticate DNS responses to prevent spoofing
- Recursive DNS server has a validating mechanism to verify the answer before storing it in its cache
- With DNSSEC enables, the authoritative DNS server with security signatures that can be fully validated up until the root, making it nearly impossible to spoof
- The attacker will have to spoof example.com, .com and the root server in order for the recursive server to accept the forged answer into its cache

### TLS/SSL
- ___HTTP:___ Protocol used for viewing web pages
  - All info is sent over the publlic internet in plain/clear text, which can be easily captured
- ___HTTPS:___ HTTP + Security Feature
  - Encrypts daata and ensures data protection
  - Protects using TLS/SSL

- ___SSL:___
  - When a computer connects to a website using SSL, the web browser will ask the website the identity
  - Website sends a copy of its SSL certificate to the Computer's Web Browser
    - If it is trustworthy, then the browser sends an OK message to the server
    - Web server responds with an ACK to the browser
    - SSL session proceeds and the encrypted data gets exchanged
  - ___TLS is the successor to SSL___
  - SSL uses both Symmetric and Asymmetric
    - Public Key Authority is the set of hardware, software, people, policies etc that are needed to create, manage, distribute and store digital certificates
    - PKI is also what binds keys with users
      - A Certificate Authority is a trusted third party entity that issues digital certs and manages public keys
    - In SSL comms, the server's SSL contains an assymetric public and private key pair
    - Session key that is created during the SSL Handshake is symmetric

### DNSSEC vs TLS/SSl
- Both are based on public key technology, but chains of trust are different
- DNSSEC provides chain of trust using DNS zone hierarchy, so name servers in parten zones vouch for the child zones
- TLS/SSL relies on Public Key Infrastructure which contains Certificate Authorities vouching for other computers









