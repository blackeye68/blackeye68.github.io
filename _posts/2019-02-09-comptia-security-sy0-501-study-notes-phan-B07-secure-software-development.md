---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B07: Secure Software Develoment"
author: blackeye
categories: [ exam, network security, comptia, study notes ]
image: assets/images/6.jpg
securityplus: true
---

# Secure Software Development
* **Software Development**
    * SDLC
        * Software Development Life Cycle
        * SDLC is an organized process of developing a secure application
        throughout the life of the project

    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd01.png)

    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd02.png)

    * Agile
        * Software development is performed in time-boxed or small increments to
        allow more adaptivity to change
    * DevOps
        * Software development and information technology operations

* **SDLC Principles**
    * Developers should always remember confidentiality, integrity, and availability
        * Confidentiality
            * Ensures that only authorized users can access the data
        * Integrity
            * Ensures that the data is not modified or altered without permission
        * Availability
            * Ensuring that data is available to authorized users when it is needed
    * Threat modeling helps prioritize vulnerability identification and patching
    * Least Privilege
            * Users and processes should be run using the least amount of access necessary to perform a given function
    * Defense in Depth
        * Layering of security controls is more effective and secure than relying on a single control
    * Never Trust User Input
        * Any input that is received from a user should undergo input validation prior to allowing it to be utilized by an application
    * Minimize Attack Surface
        * Reduce the amount of code used by a program, eliminate unneeded functionality, and require authentication prior to running additional plugins
    * Create Secure Defaults
        * Default installations should include secure configurations instead of requiring an administrator or user to add in additional security
    * Authenticity and Integrity
        * Applications should be deployed using code signing to ensure the program is not changed inadvertently or maliciously prior to delivery to an end user
    * Fail Securely
        * Applications should be coded to properly conduct error handling for exceptions in order to fail securely instead of crashing
    * Fix Security Issues
        * If a vulnerability is identified then it should be quickly and correctly patched to remove the vulnerability
    * Rely on Trusted SDKs
        * SDKs must come from trusted source to ensure no malicious code is being added

* **Testing Methods**
    * System Testing
        * Black-box Testing
            * Occurs when a tester is not provided with any information about the system or program prior to conducting the test
        * White-box Testing
            * Occurs when a tester is provided full details of a system including the source code, diagrams, and user credentials in order to conduct the test

    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd03.png)

    * Structured Exception Handling (SEH)
        * Provides control over what the application should do when faced with a runtime or syntax error
    * Programs should use input validation when taking data from users
        * Input Validation
            * Applications verify that information received from a user matches a specific format or range of values
        * Example

    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd04.png)

    * Static Analysis
        * Source code of an application is reviewed manually or with automatic tools without running the code
    * Dynamic Analysis
        * Analysis and testing of a program occurs while it is being executed or run
    * Fuzzing
        * Injection of randomized data into a software program in an attempt to find system failures, memory leaks, error handling issues, and improper input validation

* **Software Vulnerabilities and Exploits**
    * Backdoors
        * Code placed in computer programs to bypass normal authentication and other security mechanisms
        * Backdoors are a poor coding practice and should not be utilized
    * Directory Traversal
        * Method of accessing unauthorized directories by moving through the directory structure on a remote server
    * Arbitrary Code Execution
        * Occurs when an attacker is able to execute or run commands on a victim computer
    * Remote Code Execution (RCE)
        * Occurs when an attacker is able to execute or run commands on a remote computer
    * Zero Day
        * Attack against a vulnerability that is unknown to the original developer or manufacturer

* **Buffer Overflows**
    * Buffer Overflow
        * Occurs when a process stores data outside the memory range allocated by the developer
    * Buffer
        * A temporary storage area that a program uses to store data
        * Over 85% of data breaches were caused by a buffer overflow
    * Example

    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd05.png)
    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd06.png)

    * What happens if we try to enter a number that is too long?

    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd07.png)
    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd08.png)
    
    * Let’s get technical…
        * Stack
            * Reserved area of memory where the program saves the return address when a function call instruction is received

    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd10.png)

        * “Smash the Stack”
            * Occurs when an attacker fills up the buffer with NOP so that the
            return address may hit a NOP and continue on until it finds the
            attacker’s code to run

    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd11.png)

* **XSS and XSRF**
    * Cross-Site Scripting (XSS)
        * Occurs when an attacker embeds malicious scripting commands on a
        trusted website
        * Stored/Persistent
            * Attempts to get data provided by the attacker to be saved on the
            web server by the victim
        * Reflected
            * Attempts to have a non-persistent effect activated by a victim
            clicking a link on the site
        * DOM-based
            * Attempt to exploit the victim’s web browser
        * Prevent XSS with output encoding and proper input validation
    * Cross-Site Request Forgery (XSRF/CSRF)
        * Occurs when an attacker forces a user to execute actions on a web server
        for which they are already authenticated
        * Prevent XSRF with tokens, encryption, XML file scanning, and cookie
        verification

* **SQL Injection**
    * **SQL Injection**
        * Attack consisting of the insertion or injection of an SQL query via input
        data from the client to a web application
    * **Injection Attack**
        * Insertion of additional information or code through data input from a
        client to an application
            * SQL
            * HTML
            * XML
            * LDAP
        * Most common type is an SQL injection
    * **How does a normal SQL request work?**

    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd12.png)
    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd13.png)
    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd14.png)
    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd15.png)
    ![]({{site.baseurl}}/Assets/images/cs_plus/ssd16.png)

    * **How does an SQL injection work?**

![]({{site.baseurl}}/Assets/images/cs_plus/ssd17.png)
![]({{site.baseurl}}/Assets/images/cs_plus/ssd18.png)
![]({{site.baseurl}}/Assets/images/cs_plus/ssd19.png)
![]({{site.baseurl}}/Assets/images/cs_plus/ssd20.png)
![]({{site.baseurl}}/Assets/images/cs_plus/ssd21.png)

        * SQL injection is prevented through input validation and using least privilege when accessing a database
        * If you see ` OR 1=1; on the exam, it’s an SQL injection