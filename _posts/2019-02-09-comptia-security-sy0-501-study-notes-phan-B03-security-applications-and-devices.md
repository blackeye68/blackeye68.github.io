---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B03: Security Application and Devices"
author: blackeye
categories: [ exam, network security, comptia, study notes ]
image: assets/images/3.jpg
---

# Security Applications and Devices

* **Security Applications and Devices**
    * Removable media comes in different formats
    * You should always encrypt files on removable media
    * Removable Media Controls
        * Technical limitations placed on a system in regards to the utilization of USB storage devices and other removable media
        * Create administrative controls such as policies
    * Network Attached Storage (NAS)
        * Storage devices that connect directly to your organization’s network
        * NAS systems often implement RAID arrays to ensure high availability
    * Storage Area Network (SAN)
        * Network designed specifically to perform block storage functions that may consist of NAS devices
        * Use data encryption
        * Use proper authentication
        * Log NAS access
* **Software Firewalls**
    * Personal Firewalls
        * Software application that protects a single computer from unwanted Internet traffic
        * Host-based firewalls
        * Windows Firewall (Windows)
        * PF and IPFW (OS X)
        * iptables (Linux)
    * Many anti-malware suites also contain software firewalls
* **IDS**
    * Intrusion Detection System
        * Device or software application that monitors a system or network and analyzes the data passing through it in order to identify an incident or attack
        * HIDS
            * Host-based IDS
        * NIDS
            * Network-based IDS

    ![]({{site.baseurl}}/assets/images/cs_plus/sad01.png)

    * Signature, Policy, and Anomaly-based detection methods
        * Signature-based
            * A specific string of bytes triggers an alert
        * Policy-based
            * Relies on specific declaration of the security policy (i.e., ‘No Telnet Authorized’)
        * Anomaly-based
            * Analyzes the current traffic against an established baseline and triggers an alert if outside the statistical average
    * Types of Alerts
        * True positive
            * Malicious activity is identified as an attack
        * False positive
            * Legitimate activity is identified as an attack
        * True negative
            * Legitimate activity is identified as legitimate traffic
        * False negative
            * Malicious activity is identified as legitimate traffic
    * IDS can only alert and log suspicious activity…
    * IPS can also stop malicious activity from being executed
    * HIDS logs are used to recreate the events after an attack has occurred
* **Pop-up Blockers**
    * Most web-browsers have the ability to block JavaScript created pop-ups
    * Users may enable pop-ups because they are required for a website to function
    * Malicious attackers could purchase ads (pay per click) through various networks
    * Content Filters
        * Blocking of external files containing JavaScript, images, or web pages from loading in a browser
    * Ensure your browser and its extensions are updated regularly
* **Data Loss Prevention**
    * Data Loss Prevention (DLP)
        * Monitors the data of a system while in use, in transit, or at rest to detect attempts to steal the data
        * Software or hardware solutions
        * Endpoint DLP System
            * Software-based client that monitors the data in use on a computer and can stop a file transfer or alert an admin of the occurrence
        * Network DLP System
            * Software or hardware-based solution that is installed on the perimeter of the network to detect data in transit
        * Storage DLP System
            * Software installed on servers in the datacenter to inspect the data at rest
        * Cloud DLP System
            * Cloud software as a service that protects data being stored in cloud services
* **Securing the BIOS**
    * Basic Input Output System
        * Firmware that provides the computer instructions for how to accept input and send output
        * Unified Extensible Firmware Interface (UEFI)
        * BIOS and UEFI are used interchangeable in this lesson
    1. Flash the BIOS
    2. Use a BIOS password
    3. Configure the BIOS boot order
    4. Disable the external ports and devices
    5. Enable the secure boot option
* **Securing Storage Devices**
    * Removable media comes in many different formats
        * You should always encrypt files on removable media
    * Removable media controls
        * Technical limitations placed on a system in regards to the utilization of USB storage devices and other removable media
        * Create administrative controls such as policies
    * Network Attached Storage (NAS)
        * Storage devices that connect directly to your organization’s network
        * NAS systems often implement RAID arrays t* ensure high availability
    * Storage Area Network (SAN)
        * Network designed specifically to perform block storage functions that may consist of NAS devices
        1. Use data encryption
        2. Use proper authentication
        3. Log NAS access
* **Disk Encryption**
    * Encryption scrambles data into unreadable information
    * Self-Encrypting Drive (SED)
        * Storage device that performs whole disk encryption by using embedded hardware
    * Encryption software is most commonly used
        * FileVault
        * BitLocker
    * Trusted Platform Module (TPM)
        * Chip residing on the motherboard that contains an encryption key
        * If your motherboard doesn’t have TPM, you can use an external USB drive as a key
    * Advanced Encryption Standard
        * Symmetric key encryption that supports 128-bit and 256-bit keys
    * Encryption adds security but has lower performance
    * Hardware Security Module (HSM)
        * Physical devices that act as a secure cryptoprocessor during the encryption process

