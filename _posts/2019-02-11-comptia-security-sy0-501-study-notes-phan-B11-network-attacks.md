---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B11: Network Attacks"
author: blackeye
categories: [ exam network, security, comptia, experience ]
image: assets/images/10.jpg
---

Network Attacks
• Network Attacks
o Denial of Service
o Spoofing
o Hijacking
o Replay
o Transitive Attacks
o DNS attacks
o ARP Poisoning
o Ports and protocols will be tested on the Security+ exam
• Ports and Protocols
o Port
▪ A logical communication endpoint that exists on a computer or server
o Inbound Port
▪ A logical communication opening on a server that is listening for a
connection from a client
o Outbound Port
▪ A logical communication opening created on a client in order to call out
to a server that is listening for a connection
o Ports can be any number between 0 and 65,535
o Well-Known Ports
▪ Ports 0 to 1023 are considered well-known and are assigned by the
Internet Assigned Numbers Authority (IANA)
o Registered Ports
▪ Ports 1024 to 49,151 are considered registered and are usually assigned
to proprietary protocols
o Dynamic or Private Ports
▪ Ports 49,152 to 65,535 can be used by any application without being
registered with IANA
• Memorization of Ports
o 65,536 ports are available for use
21 TCP FTP File Transfer Protocol is used to transfer files from host to host
22 TCP/UDP SSH, SCP, SFTP Secure Shell is used to remotely administer network devices and systems. SCP is used for
secure copy and SFTP for secure FTP.
23 TCP/UDP Telnet Unencrypted method to remotely administer network devices (should not be used)
25 TCP SMTP Simple Mail Transfer Protocol is used to send email over the Internet
53 TCP/UDP DNS Domain Name Service is used to resolve hostnames to IPs and IPs to hostnames
69 UDP TFTP Trivial FTP is used as a simplified version of FTP to put a file on a remote host, or get a file
from a remote host
80 TCP HTTP Hyper Text Transfer Protocol is used to transmit web page data to a client for unsecured web
browsing
88 TCP/UDP Kerberos Used for network authentication using a system of tickets within a Windows domain
110 TCP POP3 Post Office Protocol v3 is used to receive email from a mail server
119 TCP NNTP Network News Transfer Protocol is used to transport Usenet articles
135 TCP/UDP RPC/DCOMscm
Remote Procedure Call is used to located DCOM ports request a service from a program on
another computer on the network
137-139
TCP/UDP
NetBIOS NetBIOS is used to conduct name querying, sending of data, and other functions over a
NetBIOS connection
143 TCP IMAP Internet Message Access Protocol is used to receive email from a mail server with more
features than POP3
161 UDP SNMP Simple Network Management Protocol is used to remotely monitor network devices
162 TCP/UDP SNMPTRAP Used to send Trap and InformRequests to the SNMP Manager on a network
389 TCP/UDP LDAP Lightweight Directory Access Protocol is used to maintain directories of users and other
objects
443 TCP HTTPS Hyper Text Transfer Protocol Secure is used to transmit web page data to a client over an
SSL/TLS-encrypted connection
445 TCP SMB Server Message Block is used to provide shared access to files and other resources on a
network
465/587 TCP SMTP with
SSL/TLS
Simple Mail Transfer Protocol used to send email over the Internet with an SSL and TLS
secured connection
514 UDP Syslog Syslog is used to conduct computer message logging, especially for routers and firewall logs
636 TCP/UDP LDAP SSL/TLS LDAP is used to maintain directories of users and other objects over an encrypted SSL/TLS
connection
860 TCP iSCSI iSCSI is used for linking data storage facilities over IP
989/990 TCP FTPS File Transfer Protocol Secure is used to transfer files from host to host over an encrypted
connection
993 TCP IMAP4 with
SSL/TLS
Internet Message Access Protocol is used to receive email from a mail server over an SSL/TLSencrypted connection
995 TCP POP3
(SSL/TLS)
Post Office Protocol v3 is used to receive email from a mail server using an SSL/TLS-encrypted
connection
1433 TCP Ms-sql-s Microsoft SQL server is used to receive SQL database queries from clients
1645/1646
UDP
RADIUS
(alternative)
Remote Authentication Dial-In User Service is used for authentication and authorization
(1645) and accounting (1646)
1701 UDP L2TP Layer 2 Tunnel Protocol is used as an underlying VPN protocol but has no inherent security
1723 TCP/UDP PPTP Point-to-Point Tunneling Protocol is an underlying VPN protocol with built-in security
1812/1813
UDP
RADIUS Remote Authentication Dial-In User Service is used for authentication and authorization
(1812) and accounting (1813)
3225 TCP/UDP FCIP Fibre Channel IP is used to encapsulate Fibre Channel frames within TCP/IP packets
3260 TCP iSCSI Target iSCSI Target is as the listening port for iSCSI-targeted devices when linking data storage
facilities over IP
3389 TCP/UDP RDP Remote Desktop Protocol is used to remotely view and control other Windows systems via a
Graphical User Interface
3868 TCP Diameter A more advanced AAA protocol that is a replacement for RADIUS
6514 TCP Syslog over
TLS
It is used to conduct computer message logging, especially for routers and firewall logs, over
a TLS-encrypted connection
• Unnecessary Ports
o 65,536 ports available
o 35 ports to memorize
o Unnecessary Port
▪ Any port that is associated with a service or function that is non-essential
to the operation of your computer or network
o Any open port represents a possible vulnerability that might be exposed
o Inbound Port
▪ A logical communication opening on a server that is listening for a
connection from a client
o C:\ net stop service
o # sudo stop service
• Denial of Service
o Denial of Service (DoS)
▪ Term used to describe many different types of attacks which attempt to
make a computer or server’s resources unavailable
• Flood Attacks
• Ping of Death
• Teardrop Attack
• Permanent DoS
• Fork Bomb
o Flood Attack
▪ A specialized type of DoS which attempts to send more packets to a
single server or host than they can handle
o Ping Flood
▪ An attacker attempts to flood the server by sending too many ICMP echo
request packets (which are known as pings)
o Smurf Attack
▪ Attacker sends a ping to subnet broadcast address and devices reply to
spoofed IP (victim server), using up bandwidth and processing
o Fraggle Attack
▪ Attacker sends a UDP echo packet to port 7 (ECHO) and port 19
(CHARGEN) to flood a server with UDP packets
o SYN Flood
▪ Variant on a Denial of Service (DOS) attack where attacker initiates
multiple TCP sessions but never completes the 3-way handshake
▪ Flood guards, time outs, and an IPS can prevent SYN Floods
o XMAS Attack
▪ A specialized network scan that sets the FIN, PSH, and URG flags set and
can cause a device to crash or reboot
o Ping of Death
▪ An attack that sends an oversized and malformed packet to another
computer or server
o Teardrop Attack
▪ Attack that breaks apart packets into IP fragments, modifies them with
overlapping and oversized payloads, and sends them to a victim machine
o Permanent Denial of Service
▪ Attack which exploits a security flaw to permanently break a networking
device by reflashing its firmware
o Fork Bomb
▪ Attack that creates a large number of processes to use up the available
processing power of a computer
• DDoS
o Distributed Denial of Service (DDoS)
▪ A group of compromised systems attack simultaneously a single target to
create a Denial of Service (DOS)
o DNS Amplification
▪ Attack which relies on the large amount of DNS information that is sent in
response to a spoofed query on behalf of the victimized server
• Stopping a DDoS
o GitHub suffered a 1.35 Tbps DDoS
o Blackholing or Sinkholing
▪ Identifies any attacking IP addresses and routes all their traffic to a nonexistent server through the null interface
o An IPS can prevent a small-scale DDoS
o Specialized security services cloud providers can stop DDoS attacks
• Spoofing
o Spoofing
▪ Occurs when an attacker masquerades as another person by falsifying
their identity
▪ Anything that uniquely identifies a user or system can be spoofed
▪ Proper authentication is used to detect and prevent spoofing
• Hijacking
o Hijacking
▪ Exploitation of a computer session in an attempt to gain unauthorized
access to data, services, or other resources on a computer or server
▪ Session theft
▪ TCP/IP hijacking
▪ Blind hijacking
▪ Clickjacking
▪ Man-in-the-Middle
▪ Man-in-the-Browser
▪ Watering hole
▪ Cross-site scripting
o Session Theft
▪ Attacker guesses the session ID for a web session, enabling them to take
over the already authorized session of the client
o TCP/IP Hijacking
▪ Occurs when an attacker takes over a TCP session between two
computers without the need of a cookie or other host access
o Blind Hijacking
▪ Occurs when an attacker blindly injects data into the communication
stream without being able to see if it is successful or not
o Clickjacking
▪ Attack that uses multiple transparent layers to trick a user into clicking on
a button or link on a page when they were intending to click on the
actual page
o Man-in-the-Middle (MITM)
▪ Attack that causes data to flow through the attacker’s computer where
they can intercept or manipulate the data
o Man-in-the-Browser (MITB)
▪ Occurs when a Trojan infects a vulnerable web browser and modifies the
web pages or transactions being done within the browser
o Watering Hole
▪ Occurs when malware is placed on a website that the attacker knows his
potential victims will access
• Replay Attack
o Replay Attack
▪ Network-based attack where a valid data transmission is fraudulently or
malicious rebroadcast, repeated, or delayed
▪ Multi-factor authentication can help prevent successful replay attacks
• Transitive Attacks
o Transitive Attacks aren’t really an attack but more of a conceptual method
o When security is sacrificed in favor of more efficient operations, additional risk
exists
• DNS Attacks
o DNS Poisoning
▪ Occurs when the name resolution information is modified in the DNS
server’s cache
▪ If the cache is poisoned, then the user can be redirected to a malicious
website
o Unauthorized Zone Transfer
▪ Occurs when an attacker requests replication of the DNS information to
their systems for use in planning future attacks
o Altered Hosts File
▪ Occurs when an attacker modifies the host file to have the client bypass
the DNS server and redirects them to an incorrect or malicious website
▪ Windows stores the hosts file in the following directory:
\%systemroot%\system 32\drivers\etc
o Pharming
▪ Occurs when an attacker redirects one website’s traffic to another
website that is bogus or malicious
o Domain Name Kiting
▪ Attack that exploits a process in the registration process for a domain
name that keeps the domain name in limbo and cannot be registered by
an authenticated buyer
• ARP Poisoning
o ARP Poisoning
▪ Attack that exploits the IP address to MAC resolution in a network to
steal, modify, or redirect frames within the local area network
▪ Allows an attacker to essentially take over any sessions within the LAN
▪ ARP Poisoning is prevented by VLAN segmentation and DHCP snooping