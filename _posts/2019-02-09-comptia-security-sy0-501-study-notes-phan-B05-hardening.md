---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B04: Hardening"
author: blackeye
categories: [ exam, network security, comptia, study notes ]
image: assets/images/11.jpg
---
# Hardening
* **Hardening**
    * **Hardening**
        * Act of configuring an operating system securely by updating it, creating
        rules and policies to govern it, and removing unnecessary applications and services
    * **We are not guaranteed security, but we can minimize the risk…**
    * **Mitigate risk by minimizing vulnerabilities to reduce exposure to threats**
* **Unnecessary Applications**
    * **Least Functionality**
        * Process of configuring workstation or server to only provide essential applications and services
    * **Personal computers often accumulate unnecessary programs over time**
    * **Utilize a secure baseline image when adding new computers**
    * **SCCM**
        * Microsoft’s System Center Configuration Management
* **Restricting Applications**
    * **Application Whitelist**
        * Only applications that are on the list are allowed to be run by the
        operating system while all other applications are blocked
    * **Application Blacklist**
        * Any application placed on the list will be prevented from running while all others will be permitted to run
    * **Whitelisting and blacklisting can be centrally managed**
* **Unnecessary Services**
    * **Any services that are unneeded should be disabled in the OS**
* **Trusted Operating Systems**
    * **Trusted Operating System (TOS)**
        * An operating system that meets the requirements set forth by government and has multilevel security
        * Windows 7 (and newer)
        * Mac OS X 10.6 (and newer)
        * FreeBSD (TrustedBSD)
        * Red Hat Enterprise Server
    * **You need to identify the current version and build prior to updating a system**
* **Updates and Patches**
    * **Patches**
        * A single problem-fixing piece of software for an operating system or
        application
    * **Hotfix**
        * A single problem-fixing piece of software for an operating system or
        application
    * **Patches and Hotfixes are now used interchangeably by most manufacturers**
    * **Categories of Updates**
        * Security Update
* **Software code that is issued for a product-specific security-related vulnerability**
        * Critical Update
* **Software code for a specific problem addressing a critical, nonsecurity bug in the software**
        * Service Pack
* **A tested, cumulative grouping of patches, hotfixes, security updates, critical updates, and possibly some feature or design changes**
        * Windows Update
* **Recommended update to fix a noncritical problem that users have found, as well as to provide additional features or capabilities**
        * Driver Update
* **Updated device driver to fix a security issue or add a feature to a supported piece of hardware**
        * Windows 10 uses the Windows Update program (wuapp.exe) to manage updates
* **Patch Management**
    * **Patch Management**
        * Process of planning, testing, implementing, and auditing of software patches
        * Planning
        * Testing
        * Implementing
        * Auditing
    * **Verify it is compatible with your systems and plan for how you will test and deploy it**
    * **Always test a patch prior to automating its deployment**
    * **Manually or automatically deploy the patch to all your clients to implement it**
    * **Large organizations centrally manage updates through an update server**
    * **Disable the wuauserv service to prevent Windows Update from running automatically**
    * **It is important to audit the client’s status after patch deployment**
    * **Linux and OSX also have built-in patch management systems**
* **Group Policies**
    * **Group Policy**
        * A set of rules or policies that can be applied to a set of users or computer accounts within the operating system
        * Access the Group Policy Editor by opening the Run prompt and enter gpedit
        * Password complexity
        * Account lockout policy
        * Software restrictions
        * Application restrictions
    * **Active Directory domain controllers have a more advanced Group Policy Editor**
    * **Security Template**
        * A group of policies that can be loaded through one procedure
    * **Group Policy objectives (GPOs) aid in the hardening of the operating system**
    * **Baselining**
        * Process of measuring changes in the network, hardware, and software environment
        * A baseline establishes what is normal so you can find deviations
* **File Systems and Hard Drives**
    * **Level of security of a system is affected by its file system type**
        * NTFS
        * FAT32
        * ext4
        * HFS+
        * APFS
    * **Windows systems can utilize NTFS or FAT32**
    * **NTFS**
        * New Technology File System is the default file system format for Windows and is more secure because it supports logging, encryption, larger partition sizes, and larger file sizes than FAT32
    * **Linux systems should use ext4 and OSX should use the APFS**
    * **All hard drives will eventually fail**
        1. Remove temporary files by using Disk Cleanup
        2. Periodic system file checks
        3. Defragment your disk drive
        4. Back up your data
        5. Use and practice restoration techniques