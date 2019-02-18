---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B10: Cloud Security"
author: blackeye
categories: [ exam network, security, comptia, experience ]
image: assets/images/11.jpg
---

# Cloud Security
* **Cloud Computing**
    * Cloud Computing
        * A way of offering on-demand services that extend the traditional capabilities of a computer or network
        * Cloud computing relies on virtualization to gain efficiencies and cost savings
    * Hyperconvergence allows providers to fully integrate the storage, network, and servers
    * Virtual Desktop Infrastructure (VDI)
        * VDI allows a cloud provider to offer a full desktop operating system to an end user from a centralized server
    * Secure Enclaves and Secure Volumes

* **Cloud Types**
    * **Public Cloud**
        * A service provider makes resources available to the end users over the Internet
    * **Private Cloud**
        * A company creates its own cloud environment that only it can utilize as an internal enterprise resource
        * A private cloud should be chosen when security is more important than cost
    * **Hybrid**
    * **Community Cloud**
        * Resources and costs are shared among several different organizations who have common service needs

* **As a Service**
    * **Software as a Service (SaaS)**
        * Provides all the hardware, operating system, software, and applications needed for a complete service to be delivered
    * **Infrastructure as a Service (IaaS)**
        * Provides all the hardware, operating system, and backend software needed in order to develop your own software or service
    * **Platform as a Service (PaaS)**
        * Provides your organization with the hardware and software needed for a specific service to operate
    * **Security as a Service (SECaaS)**
        * Provides your organization with various types of security services without the need to maintain a cybersecurity staff
        * Anti-malware solutions were one of the first SECaaS products
    * **Some solutions may not scan all the files on your system**
    * **Cloud-based vulnerability scans can better provide the attacker’s perspective**
    * **Your vulnerability data may be stored on the cloud provider’s server**
    * **Sandboxing**
        * Utilizes separate virtual networks to allow security professionals to test suspicious or malicious files
    * **Data Loss Prevention (DLP)**
    * **Continuous Monitoring**
    * **Access Control**
    * **Identity Management**
    * **Business Continuity**
    * **Disaster Recovery**

* **Cloud Security**
    * **Collocated data can become a security risk**
    * **Configure, manage, and audit user access to virtualized servers**
    * **Utilizing the cloud securely requires good security policies**
    * **Data remnants may be left behind after deprovisioning**

* **Defending Servers**
    * **File Servers**
        * Servers are used to store, transfer, migrate, synchronize, and archive files for your organization
    * **Email servers are a frequent target of attacks for the data they hold**
    * **Web servers should be placed in your DMZ**
    * **FTP Server**
        * A specialized type of file server that is used to host files for distribution across the web
        * FTP servers should be configured to require TLS connections
    * **Domain Controller**
        * A server that acts as a central repository of all the user accounts and their associated passwords for the network
    * **Active Directory is targeted for privileged escalation and lateral movement**