---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B25: Policies and Procedures"
author: blackeye
categories: [ exam network, security, comptia, experience ]
image: assets/images/10.jpg
---
# Policies and Procedures
* **Policies and Procedures**
    * Governance provides a comprehensive security management framework
    * Policies
        * Defines the role of security in an organization and establishes the desired end state of the security program
        * Policies are very broad
    * Organizational Policies
        * Provide general direction and goals, a framework to meet the business
        goals, and define the roles, responsibilities, and terms
    * System-Specific Policies
        * Address the security needs of a specific technology, application, network,
        or computer system
    * Issue-Specific Policies
        * Built to address a specific security issue, such as email privacy employee termination procedures, or other specific issues
    * Policies may be regulatory, advisory, or informative
    * Standards are used to implement a policy in an organization
    * Baseline
        * Created as reference points which are documented for use as a method of comparison during an analysis conducted in the future
    * Guidelines are used to recommend actions
    * Procedures
        * Detailed step-by-step instructions that are created to ensure personnel
        can perform a given action
    * Exam Tip
        * Policies are generic
        * Procedures are specific
* **Data Classifications**
    * Data Classification
        * Category based on the value to the organization and the sensitivity of the
        information if it were to be disclosed
    * Sensitive Data
        * Any information that can result in a loss of security, or loss of advantage to a company, if accessed by unauthorized persons
    * Commercial businesses and the government use different classification systems
    * Commercial Classifications
        * Public Data
            * Has no impact to the company if released and is often posted in
            the open-source environment
            * Sensitive data might have a minimal impact if released
        * Private Data
            * Contains data that should only be used within the organization
        * Confidential Data
            * Highest classification level that contains items such as trade
            secrets, intellectual property data, source code, and other types
            that would seriously affect the business if disclosed
    * Government Classifications
        * Unclassified data can be released to the public
        * Sensitive but Unclassified
            * Items that wouldn’t hurt national security if released but could
            impact those whose data is contained in it
        * Confidential Data
            * Data that could seriously affect the government if unauthorized
            disclosure were to happen
        * Secret Data
            * Data that could seriously damage national security if disclosed
        * Top Secret Data
            * Data that could gravely damage national security if it were known
            to those who are not authorized for this level of information
    * Data should not be stored forever
* **PII and PHI**
    * It is your responsibility to protect the data collected
    * Personal Identifiable Information (PII)
        * A piece of data that can be used either by itself or in combination with
        some other pieces of data to identify a single person
            * Full Name
            * Driver’s License
            * Date of Birth
            * Place of Birth
            * Biometric Data
            * Financial Account Numbers
            * Email Addresses
            * Social Media Usernames
        * Verify with your legal team what is considered PII
    * Privacy Act of 1974
        * Affects U.S. government computer systems that collects, stores, uses, or
        disseminates personally identifiable information
    * Health Insurance Portability and Accountability Act (HIPAA)
        * Affects healthcare providers, facilities, insurance companies, and medical
        data clearing houses
    * Sarbanes-Oxley (SOX)
        * Affects publicly-traded U.S. corporations and requires certain accounting
        methods and financial reporting requirements
    * Gramm-Leach-Bliley Act (GLBA)
        * Affects banks, mortgage companies, loan offices, insurance companies,
        investment companies, and credit card providers
    * Federal Information Security Management (FISMA) Act of 2002
        * Requires each agency to develop, document, and implement an agencywide information systems security program to protect their data
    * Payment Card Industry Data Security Standard (PCI DSS) is a contractual
    obligation
    * Help America Vote Act (HAVA) of 2002
        * Provides regulations that govern the security, confidentiality, and
        integrity of the personal information collected, stored, or processed
        during the election and voting process
    * SB 1386 requires any business that stores personal data to disclose a breach
* **Security Policies**
    * Privacy policies govern the labeling and handling of data
    * Acceptable Use Policy
        * Defines the rules that restrict how a computer, network, or other systems
        may be used
    * Change Management Policy
        * Defines the structured way of changing the state of a computer system,
        network, or IT procedure
    * Separation of Duties is a preventative type of administrative control
    * Job Rotation
        * Different users are trained to perform the tasks of the same position to
        help prevent and identify fraud that could occur if only one employee
        had the job
    * Onboarding and Offboarding Policy
        * Dictates what type of things need to be done when an employee is hired,
        fired, or quits
        * Terminated employees are often not cooperative
    * Due Diligence
        * Ensuring that IT infrastructure risks are known and managed properly
    * Due Care
        * Mitigation actions that an organization takes to defend against the risks
        that have been uncovered during due diligence
    * Due Process
        * A legal term that refers to how an organization must respect and
        safeguard personnel’s rights
        * Due process protects citizens from their government and companies from
        lawsuits
* **User Education**
    * Security Awareness Training
        * Used to reinforce to users the importance of their help in securing the
        organization’s valuable resources
        * User security awareness training has the best return on investment
    * Security Training
        * Used to teach the organization’s personnel the skills they need to
        perform their job in a more secure manner
    * Security education is generalized training (like Security+)
    * Specialized training may be developed too
* **Vendor Relationships**
    * Non-Disclosure Agreement (NDA)
        * Agreement between tw* parties that defines what data is considered
        confidential and cannot be shared outside of the relationship
        * NDAs are a binding contract
    * Memorandum of Understanding (MOU)
        * A non-binding agreement between two or more organizations to detail
        an intended common line of action
        * MOUs can be between multiple organizations
    * Service-Level Agreement (SLA)
        * An agreement concerned with the ability to support and respond to
        problems within a given timeframe and continuing to provide the agreed
        upon level of service to the user
        * SLA may promise 99.999% uptime
    * Interconnection Security Agreement (ISA)
        * An agreement for the owners and operators of the IT systems to
        document what technical requirements each organization must meet
        * Business Partnership Agreement (BPA)
        * Conducted between two business partners that establishes the
        conditions of their relationship
        * A BPA can also include security requirements
* **Disposal Policies**
    * Asset disposal occurs whenever a system is no longer needed
    * Degaussing
        * Exposes the hard drive to a powerful magnetic field which in turn causes
        previously-written data to be wiped from the drive
    * Purging (Sanitizing)
        * Act of removing data in such a way that it cannot be reconstructed using
        any known forensic techniques
    * Clearing
        * Removal of data with a certain amount of assurance that it cannot be
        reconstructed
    * Data remnants are a big security concern
    * Possible reuse of the device will influence the disposal method
        1. Define which equipment will be disposed of
        2. Determine a storage location until disposal
        3. Analyze equipment to determine disposal – reuse, resell, or destruction
        4. Sanitize the device and remove all its data
        5. Throw away, recycle, or resell the device
* **Incident Response Procedures**
    * Our systems will never be 100% secure
    * Incident Response
        * A set of procedures that an investigator follows when examining a
        computer security incident
    * Incident Management Program
        * Program consisting of the monitoring and detection of security events on
        a computer network and the execution of proper responses to those
        security events
        * Preparation
        * Identification
            * Process of recognizing whether an event that occurs should be
            classified as an incident
        * Containment
            * Containment is focused on isolating the incident
        * Eradication
        * Recovery
            * Focused on data restoration, system repair, and re-enabling any
            servers or networks taken offline during the incident response
        * Lessons Learned
* **Data Collection Procedures**
    * Create a forensic disk image of the data as evidence
        * Capture and hash system images
        * Analyze data with tools
        * Capture screenshots
        * Review network traffic and logs
        * Capture video
        * Consider Order of Volatility
        * Take statements
        * Review licensing and documentation
        * Track man-hours and expenses
    * FTK and EnCase are popular forensic tools
* **IT Security Frameworks**
    * Sherwood Applied Business Security Architecture (SABSA) is a risk-driven
    architecture
    * Control Objectives for Information and Related Technology (COBIT)
        * A security framework that divides IT into four domains: Plan and
        Organize, Acquire and Implement, Deliver and Support, and Monitor and
        Evaluate
    * NIST SP 800-53 is a security control framework developed by the Dept. of
    Commerce
    * ISO 27000
    * ITIL is the de facto standard for IT service management
        * Being able to discuss ITIL will help in your job interviews