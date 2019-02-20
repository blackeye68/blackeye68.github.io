---
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B20: Public Key Infrastructure"
author: blackeye
categories: [ exam network, security, comptia, experience ]
image: assets/images/4.jpg
securityplus: true
---

# Public Key Infrastructure
* **Public Key Infrastructure**
    * **Public Key Infrastructure (PKI)**
        * An entire system of hardware, software, policies, procedures, and people that is based on asymmetric encryption

    ![]({{site.baseurl}}/assets/images/cs_plus/pki01.png)
    ![]({{site.baseurl}}/assets/images/cs_plus/pki02.png)

    * **PKI and public key encryption are related but they are not the same thing**
    * **PKI is the entire system and just uses public key cryptography to function**

* **Digital Certificates**
    * **Certificates**
        * Digitally-signed electronic documents that bind a public key with a user’s identity
    * **X.509**
        * Standard used PKI for digital certificates and contains the owner/user’s information and the certificate authority’s information
    * **Wildcard Certificates**
        * Allow all of the subdomains to use the same public key certificate and have it displayed as valid
        * Wildcard certificates are easier to manage
    * **Subject Alternative Name (SAN)**
        * Allows a certificate owner to specify additional domains and IP addresses to be supported
    * **Single-sided certificates only require the server to be validated**
        * Dual-sided certificates require both the server and the user to be validated
    * **X.690 uses BER, CER, and DER for encoding**
    * **Basic Encoding Rules (BER)**
        * The original ruleset governing the encoding of data structures for certificates where several different encoding types can be utilized
    * **Canonical Encoding Rules (CER)**
        * A restricted version of the BER that only allows the use of only one encoding type
    * **Distinguished Encoding Rules (DER)**
        * Restricted version of the BER which allows one encoding type and has more restrictive rules for length, character strings, and how elements of a digital certificate are stored in X.509
    * **PEM**
    * **CER**
    * **CRT**
    * **KEY**
    * **P12**
    * **PFX**
    * **P7B**
    * **Privacy-enhanced Electronic Mail**
        * .pem, .cer, .crt, or .key
    * **Public Key Cryptographic System #12 (PKCS#12)**
        * .p12
    * **Personal Information Exchange**
        * .pfx
    * **Public Key Cryptographic Systems #7 (PKCS#7)**
        * .p7b
    * **Remember, these file types are associated with PKI**

* **Certificate Authorities**
    * **Registration Authority**
        * Used to verify information about a user prior to requesting that a certificate authority issue the certificate
    * **Certificate Authority**
        * The entity that issues certificates to a user
        * Verisign, Digisign, and many others act as Root CA
    * **Certificate Revocation List (CRL)**
        * An online list of digital certificates that the certificate authority has revoked
    * **Online Certificate Status Protocol (OCSP)**
        * A protocol that allows you to determine the revocation status of a digital certificate using its serial number
    * **OCSP Stapling**
        * Allows the certificate holder to get the OCSP record from the server at regular intervals and include it as part of the SSL or TLS handshake
    * **Public Key Pinning**
        * Allows an HTTPS website to resist impersonation attacks by presenting a set of trusted public keys to the user’s web browser as part of the HTTP header
    * **Key Escrow and Key Recovery Agent**
        * Key Escrow
            * Occurs when a secure copy of a user’s private key is held in case the user accidently loses their key
        * Key Recovery Agent
            * A specialized type of software that allows the restoration of a lost or corrupted key to be performed
    * **All of a CA’s certificates must be revoked if it is compromised**

* **Web of Trust**
    * **Web of Trust**
        * A decentralized trust model that addresses issues associated with the public authentication of public keys within a CA-based PKI system
        * A peer-to-peer model
        * Certificates are created as self-signed certificates
        * Pretty Good Privacy (PGP) is a web of trus