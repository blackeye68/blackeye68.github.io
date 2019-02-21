---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B16: Access Control"
author: blackeye
categories: [ exam network, security, comptia, experience ]
image: assets/images/10.jpg
securityplus: true
---

# Access Control
- **Access Control**
    o Access Control
        ▪ Methods used to secure data and information by verifying a user has permissions to read, write, delete, or otherwise modify it
    * Access Control Models
        * Discretionary Access Control (DAC)
            * The access control policy is determined by the owner
            * DAC is used commonly
            1. Every object in a system must have an owner
            2. Each owner determines access rights and permissions for each object
        ▪ Mandatory Access Control (MAC)
            • An access control policy where the computer system determines the access control for an object
            • The owner chooses the permissions in DAC but in MAC, the computer does
            • MAC relies on security labels being assigned to every user (called a subject) and every file/folder/device or network connection (called an object)
            • Data labels create trust levels for all subjects and objects
            • To access something, you need to meet the minimum level and have a “need-to-know”
            • MAC is implemented through the Rule-based and the Latticebased access control methods
        ▪ Rule-based Access Control
            • Label-based access control that defines whether access should be
            granted or denied to objects by comparing the object label and
            the subject label
        ▪ Lattice-based Access Control
            • Utilizes complex mathematics to create sets of objects and
            subjects to define how they interact
            • Mandatory Access Control is a feature in FreeBSD & SELinux
            • Only in high security systems due to its complex configuration
        ▪ Role-Based Access Control (RBAC)
            • An access model that is controlled by the system (like MAC) but
            utilizes a set of permissions instead of a single data label to define
            the permission level
            • Power Users is a role-based permission
        ▪ Attribute-Based Access Control (ABAC)
            • An access model that is dynamic and context-aware using IF-THAN
            statements
            • If Jason is in HR, then give him access to \\fileserver\HR

- Best Practices
    o Best Practices
        ▪ The access control policy is determined by the owner
        ▪ Best Practices for Access Control
    o Implicit Deny
        ▪ All access to a resource should be denied by default and only be allowed
        when explicitly stated
    o Least Privilege
        ▪ Users are only given the lowest level of access needed to perform their
        job functions
        ▪ Does everyone in the company need to know employee salary data?
    o Separation of Duties
        ▪ Requires more than one person to conduct a sensitive task or operation
        ▪ Separation of duties can be implemented by a single user with a user and
        admin account
    o Job Rotation
        ▪ Occurs when users are cycled through various jobs to learn the overall
        operations better, reduce their boredom, enhance their skill level, and
        most importantly, increase our security
        ▪ Job rotation helps the employee become more well-rounded and learn
        new skills
        ▪ Job rotation also helps the organization identify theft, fraud, and abuse of
        position

- Users and Groups
    o Computers can have multiple users and groups
        1. Right-click on an empty area in the Users folder of ADUC and select
        Create New User
        2. Create a new user within the Organizational Unit (OU) within Active
        Directory
    o User Rights
        ▪ Permissions assigned to a given user
    o Groups
        ▪ Collection of users based on common attributes (generally work roles)
    o Permissions in Windows
        ▪ Permissions are broken down into Read, Write, and Execute inside Linux
            • Full Control
            • Modify
            • Read & Execute
            • List Folder Contents
            • Read
            • Write
        ▪ Permissions are assigned to Owners (U), Groups (G), and All Users (O or A)
    o chmod
        ▪ Program in Linux that is used to change the permissions or rights of a file
        or folder using a shorthand number system
    o R (Read) = 4
        W (Write) = 2
        X (Execute) = 1
        o # chmod 760 filename
        7 = Owner can RWX
        6 = Group can RW
        0 = All Users (no access)
    o 777 allows everyone to Read, Write, and Execute
    o Privilege Creep
        ▪ Occurs when a user gets additional permission over time as they rotate
        through different positions or roles
        ▪ Privilege creep violates the principles of least privilege
        o User Access Recertification
        ▪ Process where each user’s rights and permissions are revalidated to
        ensure they are correct
            • Hired
            • Fired
            • Promoted

- Permissions
    o Permissions are inherited by default from the parent when a new folder is created
    o Any permissions added/removed from the parent folder will pass to the child
    by default too!
    o Propagation
        ▪ Occurs when permissions are passed to a subfolder from the parent
        through inheritance
    o Use Groups for roles and do not assign users directly to a folder’s permissions
    o Review Note: CompTIA A+
    o If you copy a folder, then permissions are inherited from the parent folder it is
    copied into
    o If you move a folder, then permissions are retained from its
    original permissions

- Usernames and Passwords
    o first.last@yourcompany.com
    o Strong Passwords
        ▪ Contain uppercase letters, lowercase letters, numbers, special characters,
        and at least 8 characters or more (preferably 14 or more)
        1. Always require the user to change the default password when the
        account is created
        2. Require that the password is changed frequently (every 90 days)
        3. Always change the default Administrator or Root password
        4. Disable the Guest account on your systems
        5. Enable CTRL+ALT+DEL for logging into the system
            • Turn this on in the Advanced tab of the User Accounts dialogue box
        6. Use good, strong policies in regards to your passwords

- **User Account Control**
    * **User Account Control (UAC)**
        ▪ A security component in Windows that keeps every user in standard user
        mode instead of acting like an administrative user
        + _**[*] Only exception is the Administrator account**_
        1. Eliminates unnecessary admin-level requests for Windows resources
        2. Reduces risk of malware using admin-level privileges to cause system
        issues
        ▪ UAC can be disabled from the Control Panel