 Unit 3

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
  - 





