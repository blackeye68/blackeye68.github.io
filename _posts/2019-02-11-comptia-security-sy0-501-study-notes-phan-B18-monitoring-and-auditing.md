---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B18: Monitoring and Auditing"
author: blackeye
categories: [ exam network, security, comptia, experience ]
image: assets/images/10.jpg
securityplus: true
---

# Monitoring and Auditing
* **Monitoring Types**
    * **Signature-based**
        * Network traffic is analyzed for predetermined attack patterns
    * **Anomaly-based**
        * A baseline is established and any network traffic that is outside of the baseline is evaluated
    * **Behavior-based**
        * Activity is evaluated based on the previous behavior of applications, executables, and the operating system in comparison to the current activity of the system
    * **Methods may be combined into a hybrid approach in some IDS/IPS systems**
* **Performance Baselining**
    * **Baselining**
        * Process of measuring changes in networking, hardware, software, and applications
    * **Baseline Reporting**
        * Documenting and reporting on the changes in a baseline
    * **Security Posture**
        * Risk level to which a system or other technology element is exposed
    * **Perfmon.exe is the Windows program for Performance Monitor**

* **Protocol Analyzers**
    * **Protocol analyzers are used to capture and analyze network traffic**
    * **Promiscuous Mode**
        * Network adapter is able to capture all of the packets on the network, regardless of the destination MAC address of the frames carrying them
    * **Non-promiscuous Mode**
        * Network adapter can only capture the packets directly addressed to itself
    * **To capture the most information, you need to be in promiscuous mode**
    * **Port Mirroring**
        * One or more switch ports are configured to forward all of their packets to another port on the switch
    * **If you cannot configure a SPAN port, then you can use a network tap**
        * Network Tap
            * A physical device that allows you to intercept the traffic between two points on the network

* **SNMP**
    * **Simple Network Management Protocol (SNMP)**
        * A TCP/IP protocol that aids in monitoring network-attached devices and computers
        * SNMP is incorporated into a network management and monitoring system
    * **Managed Devices**
        * Computers and other network-attached devices monitored through the use of agents by a network management system
    * **Agents**
        * Software that is loaded on a managed device to redirect information to the network management system
    * **Network Management System (NMS)**
        * Software running on one or more servers to control the monitoring of network-attached devices and computers

    ![]({{site.baseurl}}/assets/images/cs_plus/maa01.md)

    * **SNMP v1/v2 are insecure due to the use of community strings to access a device**
    * **SNMP v3**
        * Version of SNMP that provides integrity, authentication, and encryption of the messages being sent over the network
    * **Management should be conducted on an out-of-band network to increase security**

* **Auditing**
    * **Auditing**
        * A technical assessment conducted on applications, systems, or networks
        * Auditing is a detective control
            * Security logs
            * ACLs
            * User rights/permissions
            * Group policies (GPOs)
            * Vulnerability scans
            * Written organizational policies
            * Interviewing personnel
        * Software tools are also used to help conduct audits

* **Logging**
    * **Logs**
        * Data files that contain the accounting and audit trail for actions performed by a user on a computer or network
    * **Security, System, and Application logs should be audited on a Windows system**
        * Security Logs
            * Logs the events such as successful and unsuccessful user logins to the system
        * System Logs
            * Logs the events such as a system shutdown and driver failures
        * Application Logs
            * Logs the events for the operating system and third-party applications
    * **To consolidate all the logs into a single repository, you can use SYSLOG**
        * SYSLOG
            * A standardized format used for computer message logging that allows for the separation of the software that generates messages, the system that stores them, and the software that reports and analyzes them
            * SYSLOG uses port 514 over UDP

* **Log Files**
    * **Log files are important to your ability to reconstruct an event after it occurs**
    * **Log File Maintenance**
        * Actions taken to ensure the proper creation and storage of a log file, such
        as the proper configuration, saving, back up, security, and encryption of the log files
        * Log files should be saved to a different partition or an external server
    * **Overwrite Events**
        * When a maximum log size is reached, the system can begin overwriting the oldest events in the log files to make room
    * **Logs should be archived and backed up to ensure they are available when required**
    * **Write Once Read Many (WORM)**
        * Technology like a DVD-R that allows data to be written only once but read unlimited times

* **SIEM**
    * **Security Information and Event Management (SIEM)**
        * Combines security event management and security information management systems into one tool
    * **A SIEM performs data aggregation and correlation**
        * Data Aggregation
            * Combines data from various network devices, servers, and applications from across the enterprise network
        * Data Correlation
            * Automatically looks for common attributes of events across the monitored portions of the network
    * **SIEMs may also perform regulatory audits and forensic analysis functions**