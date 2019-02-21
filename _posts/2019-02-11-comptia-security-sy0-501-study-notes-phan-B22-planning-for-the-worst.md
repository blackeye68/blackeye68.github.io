---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B22: Planning for the Worst"
author: blackeye
categories: [ exam network, security, comptia, experience ]
image: assets/images/6.jpg
securityplus: true
---

# Planning for the Worst
* **Planning for the Worst**
    * **Redundancy usually refers to when you have something extra or unnecessary**
    * **Redundancy helps ensure fault-tolerance to continue operations**
    * **Single Point of Failure**
        * The individual elements, objects, or parts of a system that would cause the whole system to fail if they were to fail

* **Redundant Power**
    * **Redundant Power Supply**
        * An enclosure that provides two or more complete power supplies
        * A redundant power supply mitigates a single point of failure
    * **Surge**
        * An unexpected increase in the amount of voltage provided
    * **Spike**
        * A short transient in voltage that can be due to a short circuit, tripped
        circuit breaker, power outage, or lightning strike
    * **Sag**
        * An unexpected decrease in the amount of voltage provided
    * **Brownout**
        * Occurs when the voltage drops low enough that it typically causes the
        lights to dim and can cause a computer to shut off
    * **Blackout**
        * Occurs when there is a total loss of power for a prolonged period

* **Backup Power**
    * **Uninterruptible Power Supply (UPS)**
        * Combines the functionality of a surge protector with that of a battery
        backup
    * **Backup Generator**
        * An emergency power system used when there is an outage of the regular electric grid power
        * Portable gas-engine
        * Permanently installed
        * Battery-inverter
    * **How do you decide which to use?**

* **Data Redundancy**
    * **Redundant Array of Independent Disks (RAID)**
        * Allows the combination of multiple physical hard disks into a single logical
        hard disk drive that is recognized by the operating system
    * **RAID 0**
        * Provides data striping across multiple disks to increase performance

    ![]({{site.baseurl}}/assets/images/cs_plus/pftw01.png)

    * **RAID 1**
        * Provides redundancy by mirroring the data identically on two hard disks

    ![]({{site.baseurl}}/assets/images/cs_plus/pftw02.png)

    * **RAID 5**
        * Provides redundancy by striping data and parity data across the disk
        drives
    ![]({{site.baseurl}}/assets/images/cs_plus/pftw03.png)

    * **RAID 6**
        * Provides redundancy by striping and double parity data across the disk drives

    ![]({{site.baseurl}}/assets/images/cs_plus/pftw04.png)

    * **RAID 10**
        * Creates a striped RAID of two mirrored RAIDs (combines RAID 1 & RAID 0)

    ![]({{site.baseurl}}/assets/images/cs_plus/pftw05.png)

    * **Fault-resistant RAID**
        * Protects against the loss of the array’s data if a single disk fails (RAID 1 or
        RAID 5)
    * **Fault-tolerant RAID**
        * Protects against the loss of the array’s data if a single component fails
        (RAID 1, RAID 5, RAID 6)
    * **Disaster-tolerant RAID**
        * Provides two independent zones with full access to the data (RAID 10)

    ![]({{site.baseurl}}/assets/images/cs_plus/pftw06.png)

    * **RAIDs provide redundancy and high-availability**

* **Network Redundancy**
    * **Focused on ensuring that the network remains up**
    * **Redundant Internet connections**

* **Server Redundancy**
    * **Cluster**
        * Two or more servers working together to perform a particular job
        function
    * **Failover Cluster**
        * A secondary server can take over the function when the primary one fails
    * **Load-balancing Cluster**
        * Servers are clustered in order to share resources such as CPU, RAM, and
        hard disks

* **Redundant Sites**
    * **Hot Site**
        * A near duplicate of the original site of the organization that can be up
        and running within minutes
    * **Warm Site**
        * A site that has computers, phones, and servers but they might require
        some configuration before users can start working
    * **Cold Site**
        * A site that has tables, chairs, bathrooms, and possibly some technical
        items like phones and network cabling
    * **How do you choose the type of site?**

* **Data Backup**
    * **Maintaining a good backup is crucial to disaster recovery**
    * **Full Backup**
        * All of the contents of a drive are backed up
    * **Incremental Backup**
        * Only conducts a backup of the contents of a drive that have changed since the last full or incremental backup
    * **Differential Backup**
        * Only conducts a backup of the contents of a drive that has changed since the last full backup

    ![]({{site.baseurl}}/assets/images/cs_plus/pftw07.png)
    ![]({{site.baseurl}}/assets/images/cs_plus/pftw08.png)

    * 
        * Differential backups take more time to create but less time to restore

* **Tape Rotation**
    * **10 Tape Rotation**
        * Each tape is used once per day for two weeks and then the entire set is reused
    * **Grandfather-Father-Son**
        * Three sets of backup tapes are defined as the son (daily), the father (weekly), and the grandfather (monthly)
    * **Towers of Hanoi**
        * Three sets of backup tapes (like the grandfather-father-son) that are rotated in a more complex system

    ![]({{site.baseurl}}/assets/images/cs_plus/pftw09.png)

    * **Snapshot Backup**
        * Type of backup primarily used to capture the entire operating system image including all applications and data
        * Snapshots are also commonly used with virtualized systems

* **Disaster Recovery Planning**
    * **Disaster Recovery Planning**
        * The development of an organized and in-depth plan for problems that could affect the access of data or the organization’s building
            * Fire
            * Flood
            * Long-term Power Loss
            * Theft or Attack
            * Loss of Building
    * **Disaster Recovery Plan (DRP) should be written down**
        * Contact Information
        * Impact Determination
        * Recovery Plan
        * Business Continuity Plan (BCP)
        * Copies of Agreements
        * Disaster Recovery Exercises
        * List of Critical Systems and Data