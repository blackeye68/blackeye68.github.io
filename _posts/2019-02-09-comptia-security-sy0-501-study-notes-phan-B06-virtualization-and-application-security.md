---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B05: Virtualization & Application Security"
author: blackeye
categories: [ exam, network security, comptia, study notes ]
image: assets/images/10.jpg
---

# Virtualization
* **Virtualization**
    * Virtualization
        * Creation of a virtual resource
    * A virtual machine is a container for an emulated computer that runs an entire operating system
    * VM Types
        * System Virtual Machine
            * Complete platform designed to replace an entire physical computer and includes a full desktop/server operating system
        * Processor Virtual Machine
            * Designed to only run a single process or application like a virtualized web browser or a simple web server
    * Virtualization continues to rise in order to reduce the physical requirements for data centers
* **Hypervisors**
    * Hypervisor
        * Manages the distribution of the physical resources of a host machine (server) to the virtual machines being run (guests)

    ![]({{site.baseurl}}/Assets/images/cs_plus/v01.png)
    ![]({{site.baseurl}}/Assets/images/cs_plus/v02.png)
    *  
        * Type I (bare metal) hypervisors are more efficient than Type II
    * Container-based
        * Application Containerization
            * A single operating system kernel is shared across multiple virtual machines but each virtual machine receives its own user space for programs and data
            * Containerization allows for rapid and efficient deployment of distributed applications
    * Docker
    * Parallels Virtuozzo
    * OpenVZ
* **Threats to VMs**
    * VMs are separated from other VMs by default
    * VM Escape
        * An attack that allows an attacker to break out of a normally isolated VM by interacting directly with the hypervisor
        * Elasticity allows for scaling up or down to meet user demands
    * Data Remnants
        * Contents of a virtual machine that exist as deleted files on a cloud-based server after deprovisioning of a virtual machine
    * Privilege Elevation
        * Occurs when a user is able to grant themselves the ability to run functions as a higher-level user
    * Live migration occurs when a VM is moved from one physical server to another over the network
* **Securing VMs**
    * Uses many of the same security measures as a physical server
        * Limit connectivity between the virtual machine and the host
        * Remove any unnecessary pieces of virtual hardware from the virtual machine
        * Using proper patch management is important to keeping your guest’s operating system secure
    * Virtualization Sprawl
        * Occurs when virtual machines are created, used, and deployed without proper management or oversight by the system admins
# Application Security**
* **Application Security**
* **Web Browser Security**
    * Ensure your web browser is up-to-date with patches…
        * …but don’t adopt the newest browser immediately
    * Which web browser should I use?
    * General Security for Web Browsers
        * 1. Implement Policies
            * Create and implement web browsing policies as an administrative control or technical control
        * 2. Train Your Users
            * User training will prevent many issues inside your organization
        * 3. Use Proxy & Content Filter
            * Proxies cache the website to reduce requests and bandwidth usage
            * Content filters can be used to blacklist specific websites or entire categories of sites
        * 4. Prevent Malicious Code
            * Configure your browsers to prevent ActiveX controls, Java applets, JavaScript, Flash, and other active content
* **Web Browser Concerns**
    * Cookies
        * Text files placed on a client’s computer to store information about the
        user’s browsing habits, credentials, and
        other data
    * Locally Shared Object (LSO)
        * Also known as Flash cookies, they are stored in your Windows user profile under the Flash folder inside of your AppData folder
    * Add-Ons
        * Smaller browser extensions and plugins that provide additional
        functionality to the browser
    * Advanced Security Options
        * Browser configuration and settings for numerous options such as SSL/TLS settings, local storage/cache size, browsing history, and much more
* **Securing Applications**
    * **Use passwords to protect the contents of your documents**
    * **Digital signatures and digital certificates are used by MS Outlook for email security**
    * **User Account Control**
        ▪ Prevents unauthorized access and avoid user error in the form of accidental changes