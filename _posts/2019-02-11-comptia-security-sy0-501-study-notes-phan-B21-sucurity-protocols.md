---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B21: Security Protocols"
author: blackeye
categories: [ exam network, security, comptia, experience ]
image: assets/images/10.jpg
securityplus: true
---

# Security Protocols
* Security Protocols
    * Emails
    * Websites
    * Remote control
    * Remote access

* S/MIME
    * Secure/Multipurpose Internet Mail Extensions (S/MIME)
        * A standard that provides cryptographic security for electronic messaging
    * Authentication
    * Integrity
    * Non-repudiation
    * S/MIME can encrypt emails and their contents …including malware

* SSL and TLS
    * Secure Socket Layer (SSL) and Transport Layer Security (TLS)
        * Cryptographic protocols that provide secure Internet communications for web browsing, instant messaging, email, VoIP, and many other services
        * We already covered how TLS works in the PKI lesson
    * Downgrade Attack
        * A protocol is tricked into using a lower quality version of itself instead of a higher quality version
    * Break and Inspect

* SSH
    * Secure Shell (SSH)
        * A protocol that can create a secure channel between two computers or network devices to enable one device to control the other device
        * SSH requires a server (daemon) to be run on one device and a client on the other
        * SSH 2.0 uses Diffie-Hellman key exchange and MACs

* VPN Protocols
    * Virtual Private Networks
        * A secure connection between two or more computers or device that are not on the same private network
    * Point-to-Point Tunneling Protocol (PPTP)
        * A protocol that encapsulates PPP packets and ultimately sends data as encrypted traffic
        * PPTP can use CHAP-based authentication, making it vulnerable to attacks
    * Layer 2 Tunneling Protocol (L2TP)
        * A connection between two or more computers or device that are not on the same private network
        * L2TP is usually paired with IPSec to provide security
    * IPSec
        * A TCP/IP protocol that authenticates and encrypts IP packets and effectively securing communications between computers and devices using this protocol
        * IPSec provides confidentiality (encryption), integrity (hashing), and authentication (key exchange)
    * Internet Key Exchange (IKE)
        * Method used by IPSec to create a secure tunnel by encrypting the connection between authenticated peers
    * Main
    * Aggressive
    * Quick
    * Security Association (SA)
        * Establishment of secure connections and shared security information using certificates or cryptographic keys
    * Authentication Header (AH)
        * Protocol used in IPSec that provides integrity and authentication
    * Encapsulating Security Payload (ESP)
        * Provides integrity, confidentiality, and authenticity of packets by encapsulating and encrypting them
        * Transport Mode
            * Host-to-host transport mode only uses encryption of the payload of an IP packet but not its header
            * Transport mode is used for transmission between hosts on a private network
        * Tunnel Mode
            * A network tunnel is created which encrypts the entire IP packet (payload and header)
            * Tunnel mode is commonly used for transmission between networks