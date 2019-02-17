---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B22: Planning for the Worst"
author: blackeye
categories: [ exam network, security, comptia, experience ]
image: assets/images/10.jpg
---

# Planning for the Worst
• Planning for the Worst
o Redundancy usually refers to when you have something extra or unnecessary
o Redundancy helps ensure fault-tolerance to continue operations
o Single Point of Failure
▪ The individual elements, objects, or parts of a system that would cause
the whole system to fail if they were to fail
• Redundant Power
o Redundant Power Supply
▪ An enclosure that provides two or more complete power supplies
▪ A redundant power supply mitigates a single point of failure
o Surge
▪ An unexpected increase in the amount of voltage provided
o Spike
▪ A short transient in voltage that can be due to a short circuit, tripped
circuit breaker, power outage, or lightning strike
o Sag
▪ An unexpected decrease in the amount of voltage provided
o Brownout
▪ Occurs when the voltage drops low enough that it typically causes the
lights to dim and can cause a computer to shut off
o Blackout
▪ Occurs when there is a total loss of power for a prolonged period
• Backup Power
o Uninterruptible Power Supply (UPS)
▪ Combines the functionality of a surge protector with that of a battery
backup
o Backup Generator
▪ An emergency power system used when there is an outage of the regular
electric grid power
▪ Portable gas-engine
▪ Permanently installed
▪ Battery-inverter
o How do you decide which to use?
• Data Redundancy
o Redundant Array of Independent Disks (RAID)
▪ Allows the combination of multiple physical hard disks into a single logical
hard disk drive that is recognized by the operating system
o RAID 0
▪ Provides data striping across multiple disks to increase performance
o RAID 1
▪ Provides redundancy by mirroring the data identically on two hard disks
o RAID 5
▪ Provides redundancy by striping data and parity data across the disk
drives
o RAID 6
▪ Provides redundancy by striping and double parity data across the disk
drives
o RAID 10
▪ Creates a striped RAID of two mirrored RAIDs (combines RAID 1 & RAID 0)
o Fault-resistant RAID
▪ Protects against the loss of the array’s data if a single disk fails (RAID 1 or
RAID 5)
o Fault-tolerant RAID
▪ Protects against the loss of the array’s data if a single component fails
(RAID 1, RAID 5, RAID 6)
o Disaster-tolerant RAID
▪ Provides two independent zones with full access to the data (RAID 10)
o RAIDs provide redundancy and high-availability
• Network Redundancy
o Focused on ensuring that the network remains up
o Redundant Internet connections
• Server Redundancy
o Cluster
▪ Two or more servers working together to perform a particular job
function
o Failover Cluster
▪ A secondary server can take over the function when the primary one fails
o Load-balancing Cluster
▪ Servers are clustered in order to share resources such as CPU, RAM, and
hard disks
• Redundant Sites
o Hot Site
▪ A near duplicate of the original site of the organization that can be up
and running within minutes
o Warm Site
▪ A site that has computers, phones, and servers but they might require
some configuration before users can start working
o Cold Site
▪ A site that has tables, chairs, bathrooms, and possibly some technical
items like phones and network cabling
o How do you choose the type of site?
• Data Backup
o Maintaining a good backup is crucial to disaster recovery
o Full Backup
▪ All of the contents of a drive are backed up
o Incremental Backup
▪ Only conducts a backup of the contents of a drive that have changed
since the last full or incremental backup
o Differential Backup
▪ Only conducts a backup of the contents of a drive that has changed since
the last full backup
▪ Differential backups take more time to create but less time to restore
• Tape Rotation
o 10 Tape Rotation
▪ Each tape is used once per day for two weeks and then the entire set is
reused
o Grandfather-Father-Son
▪ Three sets of backup tapes are defined as the son (daily), the father
(weekly), and the grandfather (monthly)
o Towers of Hanoi
▪ Three sets of backup tapes (like the grandfather-father-son) that are
rotated in a more complex system
o Snapshot Backup
▪ Type of backup primarily used to capture the entire operating system
image including all applications and data
▪ Snapshots are also commonly used with virtualized systems
• Disaster Recovery Planning
o Disaster Recovery Planning
▪ The development of an organized and in-depth plan for problems that
could affect the access of data or the organization’s building
• Fire
• Flood
• Long-term Power Loss
• Theft or Attack
• Loss of Building
o Disaster Recovery Plan (DRP) should be written down
▪ Contact Information
▪ Impact Determination
▪ Recovery Plan
▪ Business Continuity Plan (BCP)
▪ Copies of Agreements
▪ Disaster Recovery Exercises
▪ List of Critical Systems and Data