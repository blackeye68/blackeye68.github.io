---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B15: Authentication"
author: blackeye
categories: [ exam network, security, comptia, experience ]
image: assets/images/11.jpg
securityplus: true
---

# Authentication
• Authentication
    o Multi-factor Authentication
        ▪ Use of two or more authentication factors to prove a user’s identity
            • Knowledge
            • Ownership
            • Characteristic
            • Location
            • Action
        ▪ Username and password are only considered single-factor authentication
    o One-Time Passwords
        ▪ Time-based One Time Password (TOTP)
            • A password is computed from a shared secret and current time
        ▪ HMAC-based One Time Password (HOTP)
            • A password is computed from a shared secret and is synchronized
            between the client and the server
            
• Authentication Models
o Context-aware Authentication
▪ Process to check the user’s or system’s attributed or characteristics prior
to allowing it to connect
▪ Restrict authentication based on the time of day or location
o Single Sign-On (SSO)
▪ A default user profile for each user is created and linked with all of the
resources needed
▪ Compromised SSO credentials cause a big breach in security
o Federated Identity Management (FIdM)
▪ A single identity is created for a user and shared with all of the
organizations in a federation
▪ Cross-Certification
• Utilizes a web of trust between organizations where each one
certifies others in the federation
▪ Trusted Third-Party
• Organizations are able to place their trust in a single third-party
(also called the bridge model)
• Trusted third-party model is more efficient than a cross
certification or web of trust model
▪ Security Assertion Markup Language (SAML)
• Attestation model built upon XML used to share federated
identity management information between systems
▪ OpenID
• An open standard and decentralized protocol that is used to
authenticate users in a federated identity management system
• User logs into an Identity Provider (IP) and uses their account at
Relying Parties (RP)
• OpenID is easier to implement than SAML
• SAML is more efficient than OpenID
• 802.1x
o 802.1x
▪ Standardized framework used for port-based authentication on wired
and wireless networks
▪ RADIUS
▪ TACACS+
▪ 802.1x can prevent rogue devices
o Extensible Authentication Protocol (EAP)
▪ A framework of protocols that allows for numerous methods of
authentication including passwords, digital certificates, and public key
infrastructure
▪ EAP-MD5 uses simple passwords for its challenge-authentication
▪ EAP-TLS uses digital certificates for mutual authentication
▪ EAP-TTLS uses a server-side digital certificate and a client-side password
for mutual authentication
o EAP-FAST
▪ Provides flexible authentication via secure tunneling (FAST) by using a
protected access credential instead of a certificate for mutual
authentication
o Protected EAP (PEAP)
▪ Supports mutual authentication by using server certificates and
Microsoft’s Active Directory to authenticate a client’s password
o LEAP is proprietary to Cisco-based networks
• LDAP and Kerberos
o Lightweight Directory Access Protocol (LDAP)
▪ A database used to centralize information about clients and objects on
the network
▪ Unencrypted
• Port 389
▪ Encrypted
• Port 636
▪ Active Directory is Microsoft’s version
o Kerberos
▪ An authentication protocol used by Windows to provide for two-way
(mutual) authentication using a system of tickets
▪ Kerberos
• Port 88
▪ A domain controller can be a single point of failure for Kerberos
• Remote Desktop Services
o Remote Desktop Protocol (RDP)
▪ Microsoft’s proprietary protocol that allows administrators and users to
remotely connect to another computer via a GUI
▪ RDP doesn’t provide authentication natively
o Virtual Network Computing (VNC)
▪ Cross-platform version of the Remote Desktop Protocol for remote user
GUI access
▪ VNC requires a client, server, and protocol be configured
o RDP
▪ Port 3389
o VNC
▪ Port 5900
• Remote Access Services
o Password Authentication Protocol (PAP)
▪ Used to provide authentication but is not considered secure since it
transmits the login credentials unencrypted (in the clear)
o Challenge Handshake Authentication Protocol (CHAP)
▪ Used to provide authentication by using the user’s password to encrypt a
challenge string of random numbers
▪ Microsoft’s version of CHAP is MS-CHAP
o PAP and CHAP used mostly with dial-up
• VPN
o Virtual Private Network (VPN)
▪ Allows end users to create a tunnel over an untrusted network and
connect remotely and securely back into the enterprise network
▪ Client-to-Site VPN or Remote Access VPN
o VPN Concentrator
▪ Specialized hardware device that allows for hundreds of simultaneous
VPN connections for remote workers
o Split Tunneling
▪ A remote worker’s machine diverts internal traffic over the VPN but
external traffic over their own internet connection
▪ Prevent split tunneling through proper configuration and network
segmentation
• RADIUS and TACACS+
o Remote Authentication Dial-In User Service (RADIUS)
▪ Provides centralized administration of dial-up, VPN, and wireless
authentication services for 802.1x and the Extensible Authentication
Protocol (EAP)
▪ RADIUS operates at the application layer
o Cisco’s TACACS+ is a proprietary version of RADIUS
• Authentication Summary
o 802.1x
▪ IEEE standard that defines Port-based Network Access Control (PNAC)
and is a data link layer authentication technology used to connected
devices to a wired or wireless LAN
o LDAP
▪ Application layer protocol for accessing and modifying directory services
data (Active Directory uses it)
o Kerberos
▪ Authentication protocol used in Windows to identify clients to a sever
using mutual authentication (Uses tickets)
o Remote Access Services (RAS)
▪ Service that enables dial-up and VPN connections to occur from remote
clients
o Challenge Handshake Protocol (CHAP)
▪ Authentication scheme that is used in dial-up connections
o RADIUS
▪ Centralization administration system for dial-up, VPN, and wireless
authentication that uses either ports 1812/1813 (UDP) or 1645/1646
(UDP)
o TACACS+
▪ Cisco’s proprietary version of RADIUS that provides separate
authentication and authorization functions over port 49 (TCP)