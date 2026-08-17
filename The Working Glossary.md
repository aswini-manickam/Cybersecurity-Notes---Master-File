# The Working Glossary

A running log of cybersecurity terms, tools, and exam keywords - added as I come across them, not in any particular order. 
Each row is a quick lookup: what category it falls into, what it's often confused with, and a one-line note to jog memory fast.

**Model key:** ☁️ Cloud | 🏢 On-Prem | 🔀 Hybrid | 🌐 Common

| Term | Acronym | Model |Category|  Note | Tools | Talk About It With |
|---|---|---|---|---|---|---|
| Security Information & Event Management | SIEM | 🌐 | - | Collects/correlates logs but doesn't respond on its own - that's SOAR | Splunk, Wazuh, Sentinel, QRadar | Log aggregation, correlation, SOC, SOAR |
| Resource Reuse | - | ☁️ | - | Cloud provider reassigns disks/storage to new tenants without wiping them-->vulnerability - old customer's sensitive data can leak to the new one | - | Data remanence, disk sanitization, multi-tenancy |
| VM Escape | - | ☁️/🔀 | - | Vulnerability in the hypervisor lets an attacker break out of their VM and access the host or other VMs | - | Hypervisor, resource reuse, multi-tenancy |
| VM Sprawl | - | ☁️/🔀 | - | VMs left running/not deprovisioned after they're no longer needed -Vulnerability - wastes resources and expands attack surface | - | Resource reuse, asset management, shadow IT | 
| Legacy Vulnerabilities | - | 🏢/🔀 | - | Systems still running after the manufacturer has stopped supporting/patching them | - | end of life |
| Baseline Lifecycle | - | 🌐 | - | cycle: establish → deploy → maintain → update | tools/vendors | 1. Baseline configuration(Establishing) ,2. Baseline deployment, 3. Baseline deviation/Drift (Maintaining), 4. Patch management(Update) | 
| Simple Network Management Protocol | SNMP | 🌐 | - | **Monitors**/manages network-attached devices | SolarWinds, PRTG, Nagios | Network monitoring, Management Information Base (MIB), traps, TCP/IP |
| File Transfer Protocol | FTP | 🌐 | - | **Transfers** files - unencrypted by default, so it's often flagged as insecure vs SFTP/FTPS | FileZilla, WinSCP | SFTP, FTPS, TCP port 21 |
| Simple Mail Transfer Protocol | SMTP | 🌐 | - | **Sends/relays email** receiving uses different protocols (POP3/IMAP), a common exam trap | Postfix, Exchange, Sendmail | Email security, SPF, DKIM, DMARC |
| Domain Name System | DNS | 🌐 | --- | Translates/**Resolves** domain names to IP addresses frequently abused for spoofing/poisoning/tunneling attacks | BIND, Pi-hole, Route 53 | DNS spoofing, DNS sinkholing, DNSSEC |
| Shadow IT | - | 🌐 | Risk/Practice | Employees using unapproved tech/workarounds outside IT-approved process - e.g. personal device instead of proper guest access | - | Insider threat, unauthorized workaround, BYOD |
| Insider Threat | - | 🌐 | Threat Actor | Someone with legitimate access who creates risk, intentionally or not - broader category than shadow IT | - | Shadow IT, unauthorized access |
| Rogue Access Point | - | 🏢🔀 | Hardware/Attack | Unauthorized WAP physically connected to the network - different from a software/process workaround | - | Wireless security, evil twin |
| Black-Box Engagement | - | 🌐 | Testing Method | Pentesting, white-box, gray-box | - | Tester has zero prior knowledge of the target system - simulates an outside attacker | 
| SQL Injection | SQLi | 🌐 | Attack | Malicious SQL inserted via input fields to manipulate/access the database | sqlmap, Burp Suite | OWASP Top 10, input validation |
| Data in Use | - | 🌐 | Data State | Hardest to protect - must be decrypted and actively processed in memory | Confidential computing, TEE | Data at rest, data in transit, memory protection |
| Data in Transit | - | 🌐 | Data State | Vulnerable during transmission - protect with strong encrypted protocols | TLS, IPsec | Data in use, data at rest |
| Data at Rest | - | 🌐 | Data State | Generally easiest to secure - encryption + access controls | Disk/storage encryption, DLP | Data in use, data in transit | 
| Session Replay | - | 🌐 | Attack | Intercepted communications replayed to potentially bypass authentication | - | Session hijacking, authentication bypass |
| Typosquatting | - | 🌐 | Attack | Registering domains that closely resemble a legitimate site | - | Phishing, domain spoofing | 
| Watering Hole Attack | - | 🌐 | Attack | Attacker compromises a site the victim already visits, injects exploit code to redirect them | - | Social engineering, compromised sites, exploit code | 
| Pretexting | - | 🌐 | Attack/Social Engineering | Phishing, social engineering | - | Creating a fabricated scenario/situation to fool the target | |
| Signature-Based Monitoring | - | 🌐 | Detection Method | Compares traffic against known attack patterns - lightweight but blind to zero-days until signature exists | Snort, Suricata | IDS/IPS, known threats |
 Zero-Day Attack | - | 🌐 | Attack/Vulnerability | Exploit for a vulnerability with no existing patch/signature - best mitigated with behavior/anomaly detection | - | unknown software flaw, not a signature-based or anomaly-based detection, novel attack |
| Anomaly-Based Detection | - | 🌐 | Detection Method | Flags behavior that deviates from an established baseline | - | Baseline, behavior-based detection, zero-day |
| Stateless Firewall | - | 🌐 | Hardware/Software | Filters based on static factors like port and IP, no connection context | - | ACL, IP, port filtering, connectionless | 
| Stateful Firewall | - | 🌐 | Hardware/Software | Tracks the context/state of active connections | - | connection tracking |
| Application Log Files | - | 🌐 | Data Source | Contains security events, errors, and user activity - key input for SOC monitoring | Splunk, ELK | SIEM, security monitoring, user activity |
| System Baselining (CPU/Memory Monitoring) | - | 🌐 | Technique | Tracks normal CPU/memory usage to spot deviations indicating issues or attacks | Nagios, Zabbix | Anomaly-based detection, performance monitoring |
| Hardware Security Module | HSM | 🏢🔀 | Hardware Appliance | Used for encryption during secure login/auth, digital signing, payment security - preferred when performance matters, faster than software encryption | Thales, YubiHSM, AWS CloudHSM | TPM, encryption, digital signatures, key management |
| Host-Based Intrusion Detection System | HIDS | 🌐 | Software | Identifies suspicious behavior on a single system/host | OSSEC, Wazuh | IDS, endpoint monitoring, NIDS |
| Router | - | 🌐 | Hardware Appliance | Makes decisions about sending packets out of a network | Cisco, Juniper | Routing, packet forwarding, firewall | 
| Trusted Platform Module | TPM | 🏢🔀 | Hardware Appliance | Similar duties to HSM but built into/embedded in the system, whereas HSM is external/additional | - | HSM, secure boot, disk encryption |
| Due Care | - | 🌐 | Governance/Compliance | Regularly reviewing and updating policies, taking proactive steps to keep controls effective | - | Due diligence, policy review, compliance |
| Acknowledgment | - | 🌐 | Governance/Compliance | Employees stating they are aware of compliance requirements | - | Attestation, onboarding, policy sign-off | 
| Attestation | - | 🌐 | Governance/Compliance | Employee confirming their actions adhere to policies | - | Acknowledgment, audit, compliance |
| Offboarding | - | 🌐 | Process | Process used when an employee is terminated | - | Access revocation, onboarding, HR security | 
| Fileless Virus | - | 🌐 | Malware | Doesn't install files - piggybacks on another program and loads into memory each time it runs, hard for AV to detect | - | Malware, memory-resident attack, LOLBins |
| Spyware | - | 🌐 | Malware | Used to gather information from a target | - | Malware, keyloggers, data exfiltration |
| Backdoor | - | 🌐 | Malware/Attack | Grants an attacker a way to re-enter the system later | -| Rootkit, persistence, RAT |
| Rootkit | - | 🌐 | Malware | Gives an attacker administrative access to a system | - | Backdoor, privilege escalation, persistence |
| Debug Mode | - | 🌐 | Weak Configuration/Vulnerability | Gives detailed error messages - can disclose too much info to attackers | - | Weak configurations, information disclosure |
| Weak Configuration (Default Credentials) | - | 🌐 | Vulnerability | System running with default user credentials | - | Debug mode, insecure protocols, hardening |
| Insecure Protocols (Telnet) | - | 🌐 | Vulnerability | System allowing telnet access is classified as having insecure protocols | - | Weak configurations, legacy platform | 
| Legacy Platform Vulnerability | - | 🏢🔀 | Vulnerability | System running an outdated operating system | - | Legacy vulnerabilities, EOL/EOS systems | 
| Risk Tolerance | - | 🌐 | Risk Management | Amount of risk an organization is willing to take - helps prioritize which vulnerabilities to address first | - | Exposure factor, residual risk, risk appetite | 
| Exposure Factor | - | 🌐 | Risk Management | Percentage of loss an organization may experience if a vulnerability is exploited | - | Risk tolerance, ALE, SLE | 
| Environmental Variables | - | 🌐 | Risk Management | Factors that influence vulnerability for specific industries | - | Risk tolerance, exposure factor |
| Residual Risk | - | 🌐 | Risk Management | Risk that remains after a control has been applied | - | Risk tolerance, inherent risk, mitigation | 
| Asymmetric Encryption | - | 🌐 | Algorithm/Encryption | Enables non-repudiation - private key corresponds to public key that authenticates digital signatures, only owner knows private key | RSA, ECC | Symmetric encryption, digital signatures, PKI |
| Symmetric Encryption | - | 🌐 | Algorithm/Encryption | Offers confidentiality, used for bulk encryption, faster than asymmetric | AES, DES | Asymmetric encryption, bulk encryption | 
| Access Control List | ACL | 🌐 | Software/Framework | List of permissions attached to an object, resides on firewalls/routers/computers, allows or denies access to a resource | - | NAC, firewalls, routers |
| Network Access Control | NAC | 🌐 | Framework/Software | Enforces security policies before granting access to network resources | Cisco ISE, Aruba ClearPass | ACL, endpoint compliance | 
| Certificate Revocation List | CRL | 🌐 | Software/Framework | Lists digital certificates from a CA that are no longer valid | - | PKI, CA, OCSP |
| Secure Access Service Edge | SASE | ☁️🔀 | Architecture/Framework | An approach to network security combining networking and security into a cloud-delivered service | Zscaler, Palo Alto Prisma, Cato Networks | SD-WAN, Zero Trust, cloud security | 
| Automated User Provisioning | - | 🌐 | Process/Technique | Ensures consistent, rapid account creation with correct permissions - eliminates manual errors, automates the identity lifecycle (not incident response) | SailPoint, Okta Workflows | Identity lifecycle, deprovisioning, RBAC |
| Software as a Service | SaaS | ☁️ | Cloud Service Model | Provides a complete, ready-to-use application (e.g. Microsoft 365) | M365, Salesforce | PaaS, IaaS, DaaS |
Platform as a Service | PaaS | ☁️ | Cloud Service Model | Provides OS/runtime/middleware - developer manages only app and data | Azure App Service, AWS Elastic Beanstalk | SaaS, IaaS, managed database | 
| Infrastructure as a Service | IaaS | ☁️ | Cloud Service Model | Provides VMs/networking - customer still manages OS, runtime, and application | AWS EC2, Azure VMs | PaaS, SaaS |
| Desktop as a Service | DaaS | ☁️ | Cloud Service Model | Provides virtual desktops - not application hosting | Citrix DaaS, AWS WorkSpaces | SaaS, VDI |
| WEP (Wired Equivalent Privacy) | WEP | 🌐 | Protocol/Vulnerability | Broken RC4 implementation - crackable in minutes with tools like Aircrack-ng; issue is cryptographic, not device limits or cost | Aircrack-ng | WPA2, WPA3, wireless security | 
| Zero Trust: Policy Engine | - | 🌐 | Architecture Component | Makes the allow/deny access decision using policy and signals | - | Zero Trust, PDP, PEP |  
| Zero Trust: Policy Administrator | - | 🌐 | Architecture Component | Executes the decision by establishing/terminating session credentials | - | Policy Engine, PEP |
| Zero Trust: Policy Enforcement Point | PEP | 🌐 | Architecture Component | Enables, monitors, and terminates the connection to the resource | - | Policy Engine, Policy Administrator |
| Zero Trust: Subject | - | 🌐 | Architecture Component | The user or service requesting access to a resource | - | Zero Trust, IAM |
| Unrestricted File Upload | - | 🌐 | Vulnerability | Allows attackers to upload executable files the server processes - fix: validate type, magic bytes, store outside webroot | - | CSRF, XSS, SQLi |
| Cross-Site Request Forgery | CSRF | 🌐 | Attack | Forces an authenticated user's browser to perform unwanted actions | - | XSS, session management |
| Cross-Site Scripting | XSS | 🌐 | Attack | Injects client-side scripts - differs from file upload (server-side executable) | - | CSRF, input validation |
| Availability | - | 🌐 | CIA Triad | Ensures authorized users can access systems/data when needed - an outage is an availability issue, not integrity/confidentiality | - | Integrity, confidentiality, uptime |
| Integrity (CIA) | - | 🌐 | CIA Triad | Ensures data hasn't been altered/corrupted | Hashing | Availability, confidentiality, hashing |
| Confidentiality (CIA) | - | 🌐 | CIA Triad | Prevents unauthorized access/exposure of data | Encryption | Availability, integrity |
| Baiting | - | 🌐 | Attack/Social Engineering | Leaves enticing physical media (USB, CD) for targets to find - exploits curiosity, physical vs. digital | - | Phishing, vishing, pretexting |
| Vishing | - | 🌐 | Attack/Social Engineering | Voice-call-based social engineering | - | Phishing, baiting, pretexting |
| Software Bill of Materials | SBOM | 🌐 | Framework/Document | Inventories all components/dependencies for supply-chain transparency | - | Supply chain security, dependencies |
| Quantitative Risk Analysis | - | 🌐 | Risk Management | Uses dollar figures (SLE, ARO, ALE) - objective, enables cost-benefit/ROI comparisons, but slower (needs financial data) | - | Qualitative analysis, ALE, SLE, ARO |
| Qualitative Risk Analysis | - | 🌐 | Risk Management | Uses subjective categories (high/medium/low) - faster than quantitative | - | Quantitative analysis | 
| Honeypot | - | 🌐 | Deception Technique | Not part of real business operations - any interaction with it lacks legitimate explanation, unlike production traffic | - | Deception tech, threat detection | 
| Policy | - | 🌐 | Governance Document | High-level mandatory statement of management's security intent | - | Standard, procedure, guideline |
| Procedure | - | 🌐 | Governance Document | Step-by-step instructions to carry out a task | - | Policy, standard, guideline |
| Standard | - | 🌐 | Governance Document | Mandatory specification implementing a policy (e.g. min. 14-char password) | - | Policy, procedure, guideline |
| Guideline | - | 🌐 | Governance Document | Optional, recommended best-practice advice | - | Policy, standard, procedure |
| Vulnerability Scanning Process | - | 🌐 | Process | Order: 1) scope & authorization → 2) host/service discovery → 3) run scan (credentialed preferred) → 4) review findings report | Nessus, Qualys | Credentialed scan, pentesting | 
| Risk Avoidance | - | 🌐 | Risk Management | Eliminates the activity creating risk entirely (e.g. not storing card data removes PCI-DSS scope) | - | Risk mitigation, risk sharing/transfer |
| Risk Sharing (Transfer) | - | 🌐 | Risk Management | Distributes risk among parties (e.g. outsourcing to a payment processor) | - | Risk avoidance, risk mitigation |
| Risk Mitigation | - | 🌐 | Risk Management | Reduces risk while still performing the activity | - | Risk avoidance, risk sharing |
| Attack Surface | - | 🌐 | Concept | All exposed points an attacker could exploit - includes overlooked infra like a monitoring tool with default creds and network access | - | Default credentials, weak configuration | |
| Recovery Point Objective | RPO | 🌐 | Metric/BCDR | Max acceptable data loss - directly determines required backup frequency (lower RPO = more frequent backups) | - | RTO, backup automation | |
| Recovery Time Objective | RTO | 🌐 | Metric/BCDR | Max acceptable downtime/recovery speed - distinct from RPO (data loss) | - | RPO, disaster recovery |
| Gray-Box Testing | - | 🌐 | Testing Method | Partial information (some architecture/user-level access) - between black-box and white-box | - | Black-box engagement, pentesting |
| AES (Advanced Encryption Standard) | AES | 🌐 | Algorithm | Supports 128-, 192-, and 256-bit key sizes | - | Symmetric encryption |
| Nation-State Actor | - | 🌐 | Threat Actor | Well-funded APT pursuing strategic espionage/disruption | - | APT, hacktivist, insider threat | 
| Hacktivist | - | 🌐 | Threat Actor | Attacks to advance an ideological/political message, not profit | - | Nation-state, insider threat | 
| Managerial Control | — | 🌐 | Control Type | Administrative/policy-driven (e.g. AUP) — directs behavior via management decisions, not technology | — | Technical, physical, operational controls |
| Physical Control | — | 🌐 | Control Type | Tangible barriers (e.g. bollards) protecting a facility | — | Managerial, technical, operational |
| Technical Control | — | 🌐 | Control Type | Enforced by technology/hardware/software (e.g. firewall ACL) | — | Managerial, physical, operational |
| Operational Control | — | 🌐 | Control Type | Day-to-day process executed by people (e.g. guard badge checks) | — | Managerial, physical, technical |
| HIPAA | — | 🌐 | Regulation | Governs PHI protection — requires admin, physical, technical safeguards for e-health records | — | GDPR, SOX, PCI-DSS |
| SOX (Sarbanes-Oxley) | SOX | 🌐 | Regulation | Governs financial reporting integrity for publicly traded companies | — | HIPAA, GDPR, PCI-DSS |
| GDPR | GDPR | 🌐 | Regulation | Governs personal data of EU residents — primary reg for EU data, not primary for US healthcare (HIPAA is) | — | Data controller, data processor, HIPAA |










---



### Quick-Add Row (copy & fill)

```markdown
| Term Name | ACRONYM | ☁️/🏢/🔀/🌐 | is it a protocol,port, vulnerability,attack,hardware appliance, software,open source intelligence/knowleged/framework| related terms | tools/vendors | one-liner note | Comment here to revisit|
```
Disclaimer: This is just personal quick-reference notes, not an authoritative or exhaustive source, always cross-check against official documentation when it matters.
