---
layout: post
title:  "CompTIA Security+ SY0-501 Study Notes - Phần B17: Risk Assessments"
author: blackeye
categories: [ exam network, security, comptia, experience ]
image: assets/images/10.jpg
securityplus: true
---

# Risk Assessments
• Risk Assessments
    o Risk Assessments
▪ A process used inside of risk management to identify how much risk
exists in a given network or system
o Risk
▪ The probability that a threat will be realized
o Vulnerabilities
▪ Weaknesses in the design or implementation of a system
o Threat
▪ Any condition that could cause harm, loss, damage, or compromise to
our information technology systems
▪ Threats are external and beyond your control
▪ What can we do about the threats we identified?
o Risk management is used to minimize the likelihood of a negative outcome
from occurring
▪ Risk Avoidance
• A strategy that requires stopping the activity that has risk or
choosing a less risky alternative
▪ Risk Transfer
• A strategy that passes the risk to a third party
▪ Risk Mitigation
• A strategy that seeks to minimize the risk to an acceptable level
▪ Risk Acceptance
• A strategy that seeks to accept the current level of risk and the
costs associated with it if the risk were realized
▪ Residual Risk
• The risk remaining after trying to avoid, transfer, or mitigate the
risk
o Identify assets
o Identify vulnerabilities
o Identify threats
o Identify the impact
• Qualitative Risk
o Qualitative analysis uses intuition, experience, and other methods to assign a
relative value to risk
o Experience is critical in qualitative analysis
• Quantitative Risk
o Quantitative analysis uses numerical and monetary values to calculate risk
o Quantitative analysis can calculate a direct cost for each risk
o Magnitude of Impact
▪ An estimation of the amount of damage that a negative risk might
achieve
▪ Single Loss Expectancy (SLE)
• Cost associated with the realization of each individualized threat
that occurs
Asset Value x Exposure Factor
▪ Annualized Rate of Occurrence (ARO)
• Number of times per year that a threat is realized
▪ Annualized Loss Expectancy (ALE)
• Expected cost of a realized threat over a given year
ALE = SLE x ARO
    o If it costs $200,000 to build a server room that never loses power, then it would take 33 years to recover the building costs instead of losing power 3x year!
    o Hybrid approaches that combine quantitative and qualitative analysis are commonly used

• Methodologies
    o Security Assessments
        ▪ Verify that the organization’s security posture is designed and configured
        properly to help thwart different types of attacks
        ▪ Assessments might be required by contracts, regulations, or laws
        ▪ Assessments may be active or passive
• Active Assessments
    o Utilize more intrusive techniques like scanning, hands-on
    testing, and probing of the network to determine
    vulnerabilities

• Passive Assessments
    o Utilize open source information, the passive collection and
    analysis of the network data, and other unobtrusive
    methods without making direct contact with the targeted
    systems
    o Passive techniques are limited in the amount of detail they
    find

• Security Controls
    o Security Controls
        ▪ Methods implemented to mitigate a particular risk
    o Security controls are categorized as physical, technical, or administrative
        ▪ Physical Controls
• Any security measures that are designed to deter or prevent
unauthorized access to sensitive information or the systems that
contain it
▪ Technical Controls
• Safeguards and countermeasures used to avoid, detect,
counteract, or minimize security risks to our systems and
information
▪ Administrative Controls
• Focused on changing the behavior of people instead of removing
the actual risk involved
o NIST categories are management, operational, and technical
▪ Management Controls
• Security controls that are focused on decision-making and the
management of risk
▪ Operational Controls
• Focused on the things done by people
▪ Technical Controls
• Logical controls that are put into a system to help secure it
o Preventative, Detective, or Corrective controls
▪ Preventative Controls
• Security controls that are installed before an event happens and
are designed to prevent something from occurring
▪ Detective Controls
• Used during the event to find out whether something bad might
be happening
▪ Corrective Controls
• Used after an event occurs
o A single control can be categorized into multiple types or categories
o Compensating Control
▪ Used whenever you can’t meet the requirement for a normal control
▪ Residual risk not covered by a compensating control is an accepted risk
• Vulnerability Management
o Vulnerability Assessment
▪ Seeks to identify any issues in a network, application, database, or other
systems prior to it being used that might compromise the system
▪ Defines, identifies, and classifies vulnerabilities within a system
o Vulnerability Management
▪ Practice of finding and mitigating the vulnerabilities in computers and
networks
o These 3 questions can help to scope your assessments
▪ 1. What is the value of the information?
▪ 2. What is the threat your system is facing?
▪ 3. What is the mitigation that could be deployed?
o Nessus, Qualysguard, and AlienVault are used for vulnerability assessments
▪ 1. Define the desired state of security
▪ 2. Create a baseline
▪ 3. Prioritize the vulnerabilities
▪ 4. Mitigate vulnerabilities
▪ 5. Monitor the network and systems
o Scan, Patch, Scan, …
• Penetration Testing
o Penetration tests look at a network’s vulnerabilities from the outside
o Metasploit and CANVAS are commonly used
o Get permission and document info
o Conduct reconnaissance
o Enumerate the targets
o Exploit the targets
o Document the results
o Vulnerability Assessment
▪ Seeks to identify any issues in a network, application, database, or other
systems prior to it being used that might compromise the system
o Pivot
▪ Occurs when an attacker moves onto another workstation or user
account
o Persistence
▪ Ability of an attacker to maintain a foothold inside the compromised
network
o A pentester can also simulate an insider threat
• OVAL
o Open Vulnerability and Assessment Language (OVAL)
▪ A standard designed to regulate the transfer of secure public information
across networks and the Internet utilizing any security tools and services
available
▪ OVAL is comprised of a language and an interpreter
o OVAL Language
▪ An XML schema used to define and describe the information being
created by OVAL to be shared among the various programs and tools
o OVAL Interpreter
▪ A reference developed to ensure the information passed around by these
programs complies with the OVAL schemas and definitions used by the
OVAL language
• Vulnerability Assessments
o Vulnerability Assessment
▪ Baselining of the network to assess the current security state of
computers, servers, network devices, and the entire network in general
▪ Network Mapping
• Discovery and documentation of physical and logical connectivity
that exists in the network
• Commercial and free network mapping software is available
▪ Vulnerability Scanning
• A technique that identifies threats on the network without
exploiting them
• Banner Grabbing
o A technique used to gain information about servers and
inventory the systems or services
• Nessus and Qualysguard are commercial vulnerability scanners
▪ Network Sniffing
• The process of finding and investigating other computers on the
network by analyzing the network traffic or capturing the packets
being sent
• Network sniffer, packet sniffing, and protocol analyzer can all
conduct packet capture
• Protocol Analyzer
o Software tool that allows for the capture, reassembly, and
analysis of packets from the network
▪ Password Analysis