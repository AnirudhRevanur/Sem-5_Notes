# Unit 3

## Assymetric Key Cryptography

- Trusted Key Distribution Center establish a shared secret key over the network
- Private and Public Key crypto will exist in parallel and continue to serve
- They are complements of each other
- Advantages of one can compensate for the disadvantages of the other
- ___Public Key:___ May be known by anybody, and can be used to encrypt messages
- ___Private Key:___ Known only to the recipient, used to decrypt messages and create signatures
- It is Asymmetric, because those who encrypt messages or verify signatures cannot decrypt the messages

### Why Public Key Cryptography?
- ___Key Distribution:___ How to have a secure communication in general without having to trust a KDC
- ___Digital Signatures:___ How to verify a message comes intact from the claimed sender
- Invented by:
  - Whitefield Diffie
  - Martin Hellman
  - Ralph Merkle
- Public Key alogs rely on two keys:
  - Computationally impossible to find decryption key knowing only algo and encryptio key
  - Computationally easy to en/decrypt messages when relevant key is known
  - Either of the two keys can be used for encryption, while the other is used for decryption
- The burden of security comes onto the reciever
- Reciever needs to create two keys, one private and one public
- Reciever is responsible for distributing the public key to the public

- This provides a good amount of Authentication and Secrecy
- ___Drawback:___ This public key algo is complex, and must be done 4 times rather than two times in each communication

### Requirements for Public-Key
- Computationally easy to generate a pair of keys
- Easy for a sender, knowing the public key and the plaintext to be encrypted, to generate the corresponding CipherText
- Computationally east for the reciever to decrypt the resulting ciphertext using the private key to retrieve the message
- Infeasible for anyone to get to know the private key if the public key is known
- Infeasible for anyone knowing the public key and a Cipher Text to retreive the original message


### Public Key Encryption Scheme
- It is a tuple of probabilistic polynomial-time alogrithms such that
  - Key generation Algorithm ___Gen___ takes as input the security parameter and outputs a pair of keys _pk_ and _sk_. These keys are are the public and private keys respectively
  - Encryption Algorithm ___Enc___ takes as input public key and message. It outputs ciphertext 'C'.
  - Decryption Algorithm ___Dec___ takes as input a private key _sk_ and a ciphertext _c_ and outputs a message _m_ in the case of success or a special symbol in the case of failure

### Private Key vs Public Key Cryptography

|Private Key Encryption|Public Key Encryption|
|:--:|:--:|
|Uses one key for encryption and decryption|Uses two keys, public and private|
|Key must be kept a secret|One key is a secret and the other can be freely exposed|
|Low power consumption|High power consumption|
|Speed in performace|Slow in performance|
|Inexpesive to generate|Expensive to generate|
|Randomly generated k-bit strings|Have special structures|
|Best  used for secrecy and integration of data|Best used key exchange and authentication|
|Key distribution is problematic|Key distribution is simple|
|Ex: AES, DES|Ex: Elliptic Curve, RSA, Diffie-Hellman key exchange|

### Public Key Applications
- Can classify uses into 3 categories
  - Encryption/Decryption (Provide secrecy)
  - Digital Signatures (Provide Authentication)
  - Key Exchange (of session keys)
- Some algos are suitable for all uses, others are specific to one























## One Way Functions and Permutations

- A function whose output length is polynomially related to its input length is ___one-way___ if the following conditions hold
  1. Easy to compute
  2. Hard to Invert

- A tuple of probabilistic, polynomial-time algos is a ___family of functions___ if the following hold true:
  1. ___Parameter generation Algorithm (Gen)___ outputs parameters _I_. Each value of _I_ output by the Parameter Gen Algo defines the Domain and Range of a function, that is later defined
  2. The ___Sampling Algorithm__ on input I, outputs a uniformly distributed element of the Domain
  3. The deterministic ___Evaluation Algorithm___ on input I and x, belonging to Domain, output an element y belonging to the Range

  - This tuple is a ___family of permutations___ if for each value of _I_ (Output of the function Gen) holds that Domain = Range, and the function `f: D -> D` is a bijection



  
