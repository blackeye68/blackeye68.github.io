---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B19: Cryptography"
author: blackeye
categories: [ exam network, security, comptia, experience ]
image: assets/images/5.jpg
securityplus: true
---

# Cryptography

* **Cryptography**
    * **Cryptography**
        * The practice and study of writing and solving codes in order to hide the
        true meaning of information
    * **Encryption**
        * Process of converting ordinary information (plaintext) into an
        unintelligible form (ciphertext)
        * Encryption protects data at rest, data in transit, or data in use
            * Data at Rest
                * Inactive data that is archived, such as data resident on a hard disk drive
            * Data in Transit
                * Data crossing the network or data that resides in a computer’s memory
            * Data in Use
                * Data that is undergoing constant change

    ![]({{site.baseurl}}/assets/images/cs_plus/c01.png)

    * 
        * Encryption strength comes from the key, not the algorithm
            * Key
                * The essential piece of information that determines the output of a cipher

* **Symmetric vs Asymmetric**
    * **Symmetric Algorithm (Private Key)**
        * Encryption algorithm in which both the sender and the receiver must know the same secret using a privately-held key
        * Confidentiality can be assured with symmetric encryption
        * Key distribution can be challenging with symmetric encryption
        * Symmetric Algorithms
            * DES, 3DES, IDEA, AES, Blowfish, Twofish, RC4, RC5, RC6
    * **Asymmetric Encryption (Public Key)**
        * Encryption algorithm where different keys are used to encrypt and decrypt the data
        * Asymmetric Algorithms
            * Diffie-Hellman, RSA, and ECC
    * **Symmetric is 100-1000x faster than asymmetric**
    * **Hybrid Implementation**
        * Utilizes asymmetric encryption to securely transfer a private key that can then be used with symmetric encryption
    * **Stream Cipher**
        * Utilizes a keystream generator to encrypt data bit by bit using a mathematical XOR function to create the ciphertext
    * **Block Cipher**
        * Breaks the input into fixed-length blocks of data and performs the encryption on each block
        * Block ciphers are easier to implement through a software solution

* **Symmetric Algorithms**
    * **Symmetric Algorithms**
        * DES, 3DES, IDEA, AES, Blowfish, Twofish, RC4, RC5, RC6
    * **Data Encryption Standard (DES)**
        * Encryption algorithm which breaks the input into 64-bit blocks and uses transposition and substitution to create ciphertext using an effective key strength of only 56-bits
        * DES used to be the standard for encryption
    * **Triple DES (3DES)**
        * Encryption algorithm which uses three separate symmetric keys to encrypt, decrypt, then encrypt the plaintext into ciphertext in order to increase the strength of DES
    * **International Data Encryption Algorithm (IDEA)**
        * Symmetric block cipher which uses 64-bit blocks to encrypt plaintext into ciphertext
    * **Advanced Encryption Standard (AES)**
        * Symmetric block cipher that uses 128-bit, 192-bit, or 256-bit blocks and a matching encryption key size to encrypt plaintext into ciphertext
        * AES is the standard for encrypting sensitive U.S. Government data
    * **Blowfish**
        * Symmetric block cipher that uses 64-bit blocks and a variable length encryption key to encrypt plaintext into ciphertext
    * **Twofish**
        * Symmetric block cipher that replaced blowfish and uses 128-bit blocks and a 128-bit, 192-bit, or 256-bit encryption key to encrypt plaintext into ciphertext
    * **Rivest Cipher (RC4)**
        * Symmetric stream cipher using a variable key size from 40-bits to 2048- bits that is used in SSL and WEP
    * **Rivest Cipher (RC5)**
        * Symmetric block cipher with a key size up to 2048-bits
    * **Rivest Cipher (RC6)**
        * Symmetric block cipher that was introduced as a replacement for DES but AES was chosen instead
    * **Exam Tips**
        * RC4 is the only stream cipher covered

* **Public Key Cryptography**
    * **Asymmetric algorithms are also known as Public Key Cryptography**
        * Confidentiality
        * Integrity
        * Authentication
        * Non-repudiation

    ![]({{site.baseurl}}/assets/images/cs_plus/c02.png)

        * Organizations want both confidentiality and non-repudiation
    * **Digital Signature**
        * A hash digest of a message encrypted with the sender’s private key to let the recipient know the document was created and sent by the person claiming to have sent it
    * **PKI**
        * Public Key Infrastructure
    * **Exam Tips**
        * Asymmetric encryption is also known as public key cryptography
        * Two keys are used in public key cryptography

* **Asymmetric Algorithms**
    * **Asymmetric Algorithms**
        * Diffie-Hellman, RSA, and ECC
    * **Diffie-Hellman (DH)**
        * Used to conduct key exchanges and secure key distribution over an unsecure network
        * Diffie-Hellman is used for the establishment of a VPN tunnel using IPSec
    * **RSA (Rivest, Shamir, and Adleman)**
        * Asymmetric algorithm that relies on the mathematical difficulty of factoring large prime numbers
        * RSA is widely used for key exchange, encryption, and digital signatures
        * RSA can use key sizes of 1024-bits to 4096-bits
    * **Elliptic Curve Cryptography (ECC)**
        * Algorithm that is based upon the algebraic structure of elliptic curves over finite fields to define the keys
        * ECC with a 256-bit key is just as secure as RSA with a 2048-bit key
        * ECDH
            * Elliptic Curve Diffie-Hellman
        * ECDHE
            * Elliptic Curve Diffie-Hellman Ephemeral
        * ECDSA
            * Elliptic Curve Digital Signature Algorithm
        * ECC is most commonly used for mobile devices and low-power computing device

* **Pretty Good Privacy**
    * **Pretty Good Privacy (PGP)**
        * An encryption program used for signing, encrypting, and decrypting emails
        * The IDEA algorithm is used by PGP
    * **Symmetric functions use 128-bit or higher keys and the asymmetric functions use 512-bit to 2048-bit key sizes**
    * **GNU Privacy Guard (GPG)**
        * A newer and updated version of the PGP encryption suite that uses AES for its symmetric encryption functions
        * GPG has cross-platform availability

* **Key Management**
    * **Key Management**
        * Refers to how an organization will generate, exchange, store, and use encryption keys
    * **The strength of an encryption system lies in the key strength**
    * **Keys must be securely stored**
    * **Periodically change your keys**

* **One-Time Pad**
    * **One-Time Pad**
        * A stream cipher that encrypts plaintext information with a secret random key that is the same length as the plaintext input
    * **There are no such thing as truly random numbers in computers**
    * **Pseudo-Random Number Generator (PRNG)**
        * A simulated random number stream generated by a computer that is used in cryptography, video games, and more
    * **One-time pads are not commonly used**

* **Steganography**
    * **Steganography**
        * The science and art of hiding messages within other messages
        * Steganography is a form of obfuscation, not encryption

* **Hashing**
    * **Hashing**
        * A one-way cryptographic function which takes an input and produces a unique message digest
    * **Message Digest 5 (MD5)**
        * Algorithm that creates a fixed-length 128-bit hash value unique to the input file
    * **Collision**
        * Condition that occurs when two different files create the same hash digest
    * **Secure Hash Algorithm (SHA-1)**
        * Algorithm that creates a fixed-length 160-bit hash value unique to the input file
    * **Secure Hash Algorithm (SHA-2)**
        * Family of algorithms that includes SHA-224, SHA-256, SHA-348, and SHA-512
    * **Secure Hash Algorithm (SHA-3)**
        * Family of algorithms that creates hash digests between 224-bits and 512-bits
    * **RACE Integrity Primitive Evaluation Message Digest (RIPEMD)**
        * An open-source hash algorithm that creates a unique 160-bit, 256-bit, or 320-bit message digest for each input file
    * **Hash-based Message Authentication Code (HMAC)**
        * Uses a hash algorithm to create a level of assurance as to the integrity and authenticity of a given message or file
        * HMAC-MD5
        * HMAC-SHA1
        * HMAC-SHA256
    * **Digital signatures prevent collisions from being used to spoof the integrity of a message**

    ![]({{site.baseurl}}/assets/images/cs_plus/c03.png)

    * **Digital signatures use either DSA, RSA, ECDSA, or SHA**
    * **Code Signing**
        * Uses digital signatures to provide an assurance that the software code has not been modified after it was submitted by the developer
    * **LANMAN (LM Hash)**
        * Original version of password hashing used by Windows that uses DES and is limited to 14 characters
    * **NT LAN Manager Hash (NTLM Hash)**
        * Replacement for LM Hash that uses RC4 and was released with Windows NT 3.1 in 1993
    * **NTLMv2 Hash**
        * Replacement for NTLM Hash that uses HMAC-MD5 and is considered difficult to crack
        * NTLMv2 is used when you do not have a domain with Kerberos for authentication
    * **Exam Tips**
        * Instantly match integrity and hashing on the exam
        * MD5 and SHA are the most common hash functions used

* **Hashing Attacks**
    * **Pass the Hash**
        * A technique that allows an attacker to authenticate to a remote server or service by using the 
        underlying NTLM or LM hash instead of requiring the associated plaintext password

    ![]({{site.baseurl}}/assets/images/cs_plus/c04.png)

    * 
        * Pass the Hash is difficult to defend against
        * Mimikatz
            * A penetration testing tool used to automate the harvesting of hashes and conducting the Pass the Hash attack
        * Only use a trusted OS
        * Patch/update workstations
        * Use multifactor authentication
        * Use least privilege
    * **Birthday Attack**
        * Technique used by an attacker to find two different messages that have the same identical hash digest
        * 99% chance of finding a matching birthday in a 57-person group
        * 50% chance of finding a matching birthday in a 23-person group
        * Collision
            * Occurs when two different inputs to a hash create an identical hash digest output

* **Increasing Hash Security**
    * **Key Stretching**
        * A technique that is used to mitigate a weaker key by increasing the time needed to crack it
        * WPA, WPA2, PGP, bcrypt, and other algorithms utilize key stretching
    * **Salting**
        * Adding random data into a one-way cryptographic hash to help protect against password cracking techniques
        * A “nonce” is used to prevent password reuse