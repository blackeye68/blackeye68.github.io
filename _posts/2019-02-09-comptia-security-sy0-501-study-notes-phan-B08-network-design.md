---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B08: Network Design"
author: blackeye
categories: [ exam, network security, comptia, study notes ]
image: assets/images/10.jpg
---

# Network Design
* **Network Security**
    * OSI Model

    ![]({{site.baseurl}}/Assets/images/cs_plus/nd01.png)

    * If you never learned network fundamentals, go back and review

* **OSI Model**
    * OSI Model
        * Used to explain network communications between a host and remote device over a LAN or WAN

    ![]({{site.baseurl}}/Assets/images/cs_plus/nd02.png)
    ![]({{site.baseurl}}/Assets/images/cs_plus/nd03.png)

    * Physical Layer
        * Represents the actual network cables and radio waves used to carry data over a network
        * Bits
    * Data Link Layer
        * Describes how a connection is established, maintained, and transferred over the physical layer and uses physical addressing (MAC addresses)
        * Frames
    * Network Layer
        * Uses logical address to route or switch information between hosts, the network, and the internetworks
        * Packets
    * Transport Layer
        * Manages and ensures transmission of the packets occurs from a host to a destination using either TCP or UDP
        * Segments (TCP) or Datagrams (UDP)
    * Session Layer
        * Manages the establishment, termination, and synchronization of a session over the network
    * Presentation Layer
        * Translates the information into a format that the sender and receiver both understand
    * Application Layer
        * Layer from which the message is created, formed, and originated
        * Consists of high-level protocols like HTTP, SMTP, and FTP

* **Switches**
    * Switches are the combined evolution of hubs and bridges
    * MAC Flooding
        * Attempt to overwhelm the limited switch memory set aside to store the MAC addresses for each port
        * Switches can fail-open when flooded and begin to act like a hub
    * MAC Spoofing
        * Occurs when an attacker masks their own MAC address to pretend they have the MAC address of another device
        * MAC Spoofing is often combined with an ARP spoofing attack
        * Limit static MAC addresses accepted
        * Limit duration of time for ARP entry on hosts
        * Conduct ARP inspection
    * Physical Tampering
        * Physical tampering occurs when an attacker attempts to gain physical access

* **Routers**
    * Routers operate at Layer 3
    * Routers
        * Used to connect two or more networks to form an internetwork
        * Routers rely on a packet’s IP Addresses to determine the proper destination
        * Once on the network, it conducts an ARP request to find final destination
    * Access Control List
        * An ordered set of rules that a router uses to decide whether to permit or deny traffic based upon given characteristics
        * IP Spoofing is used to trick a router’s ACL

* **Network Zones**
    * Any traffic you wish to keep confidential crossing the internet should use a VPN
    * De-Militarized Zone (DMZ)
        * Focused on providing controlled access to publicly available servers that are hosted within your organizational network
        * Sub-zones can be created to provide additional protection for some servers
    * Extranet
        * Specialized type of DMZ that is created for your partner organizations to access over a wide area network
    * Intranets are used when only one company is involved

* **Network Access Control**
    * Network Access Control (NAC)
        * Security technique in which devices are scanned to determine its current state prior to being allowed access onto a given network
        * If a device fails the inspection, it is placed into digital quarantine
    * Persistent Agents
        * A piece of software that is installed on the device requesting access to the network
    * Non-Persistent Agents
        * Uses a piece of software that scans the device remotely or is installed and subsequently removed after the scan
    * NAC can be used as a hardware or software solution
    * IEEE 802.1x standard is used in port-based NAC

* **VLANs**
    * Segment the network
    * Reduce collisions
    * Organize the network
    * Boost performance
    * Increase security
    * Switch Spoofing
        * Attacker configures their device to pretend it is a switch and uses it to negotiate a trunk link to break out of a VLAN
    * Double Tagging
        * Attacker adds an additional VLAN tag to create an outer and inner tag
        * Prevent double tagging by moving all ports out of the default VLAN group

* **Subnetting**
    * Subnetting
        * Act of creating subnetworks logically through the manipulation of IP addresses
        * Efficient use of IP addresses
        * Reduced broadcast traffic
        * Reduced collisions
        * Compartmentalized
    * Subnet’s policies and monitoring can aid in the security of your network

* **Network Address Translation**
    * Network Address Translation (NAT)
        * Process of changing an IP address while it transits across a router
        * Using NAT can help us hide our network IPs
    * Port Address Translation (PAT)
        * Router keeps track of requests from internal hosts by assigning them random high number ports for each request
    * Class A
        * 10.0.0.0 to 10.255.255.255
    * Class B
        * 172.16.0.0 to 172.31.0.0
    * Class C
        * 192.168.0.0 to 192.168.255.255

* **Telephony**
    * Telephony
        * Term used to describe devices that provide voice communication to users
    * Modem
        * A device that could modulate digital information into an analog signal for transmission over a standard dial-up phone line
    * War Dialing
        * Protect dial-up resources by using the callback feature
    * Public Branch Exchange (PBX)
        * Internal phone system used in large organizations
    * Voice Over Internet Protocol (VoIP)
        * Digital phone service provided by software or hardware devices over a data network
    * Quality of Service (QoS)