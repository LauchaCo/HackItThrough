### Attack Ecuation

Attacks = Motive (Goal) + Methods + Vulnerabilities

If either one of these factors doesn't exist, the attack will not be performed, so it's highly important that we keep all the elements of the ecuation in our control as safe as we can.

A __motive__ originates out of the notion that the target system __stores or processes__ something important, and this leads to the threat of an attack on the system

Attackers try various attacks techniques and tools to exploit vulns in a system or its security policies and controls in order to fulfil their motives.

Possible motives:
- Disrupting business continuity
- Stealing info and manipulating data
- Creating fear and chaos by disrupting critical infrastructures
- Causing financial loss to the target
- Damaging the reputation of the target

### Classification of attacks

#### Passive attacks
- Do not tamper with the data and involve intercepting and monitoring the network traffic.
- Ex: Sniffing and eavesdropping

#### Active attacks
- Tamper with the data in transti to __disrupt the communication__ or services between the systems to bypass or break into secured systems.
- Ex.: DoS, MitM, Session Hijacking and SQLi

#### Close-in attacks
- Are performed when the hacker is in close physical proximity with the target in order to gather, modify or disrupt access to info
- Ex.: Social engineering such as eavesdropping, shoulder surfing and dumpster diving 

#### Insider attacks
- Involve using privileged access to violate rules or intentionally cause a threat to the organization's info
- Ex.: Theft of physical devices and planting keyloggers, backdoors and malware.

#### Distribution attacks
- Occur when attackers __tamper with hardware__ or __software__ prior to installation.
- Attackers tamper with the hardware or software at its source or in transit

### Information security attack vectors

- Cloud computing threads: Is an on-demand delivery of IT capabilities where sensitive data of organizations, and their clients is stored. Flaw in this kind of apps can lead to client's data being leaked
- Advanced Persistent Threats (APT): An attack that consists on stealing information from a victim's machine without the user being aware of it.
- Virus and Worms: The most prevalent networking threat that are capable of infecting the network within seconds.
- Ransomware: Restricts access to the computer system's files and folders and demands an online ransom payment to the malware creators in order to remove the restrictions.
- Mobile Threats: Focus of attackers has changed towards mobile devices because of the increased usage of them for business and personal purposes and comparatively lesser security controls.
- Botnet: A huge network of compromised systems used by an intruder to perform various network attacks.
- Insider attack: An attack performed on a corporate network or on a single computer by an entrusted person (Insider) who has access to the network
- Phishing: The practice of sending an illegitimate email falsely claiming from a legitimate site in an attempt to acquire a user's personal or account information
- Web application threads: Attackers target web apps to steal credentials, set up a phishing website, or acquire private information to threaten the performance of the security and hamper its security.
- IoT Threats: 
	- IoT devices include many software applications that are used to access the device remotely
	- Flaws in IoT devices allows attackers to access remotely to the device and perform various attacks.

### Payment Card Industry Data Security Standard (PCI DSS)
- A proprietary information security standard for organizations that handle cardholder information.
- PCI DSS applies to all entities involved in payment card processing

#### PCI DSS Overview
- Build and mantain a secure network
- Protect Cardholder data
- Mantain a Vulnerability Managment Program.
- Implement Strong Access Control Measures
- Regularly Monitor and Test Networks
- Mantain an Information Security Policy

Failure to meet the PCI DSS requirements may result in fines or the termination of payment card processing privileges

### ISO/IEC 27001:2013
- Specifies the requirements for establishing, implementing, mantaining and continually improving an information security managment system whitin the context of the organization.

### Health Insurance Portability and Accountability ACT (HIPAA)
HIPAA rules:
- Electronic Transaction and Code Set Standards: Every provider have to use the same health care transactions, code sets and identifiers
- Privacy Rule: Provides federal protection for the personal health information.
- Security Rule: Specifies administrative, physical and technological safeguards for covered entities to use to ensure the confidentiality, integrity and availability of electronically protected health information.
- National Identifier Requirements: Requires that covered entities have standard national numbers that identify them attached to standard transactions
- Enforcement Rule: Provides the standards for enforcing all the Administration Simplification Rules.