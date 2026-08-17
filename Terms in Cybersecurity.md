# Personal quick-reference table

Cybersecurity has countless terms, tools, and acronyms - with new ones surfacing constantly. 
So, this is a personal quick-reference table, filled in gradually as I come across new terms, so entries build up naturally over time rather than all at once. 
Updated regularly.

**Model key:** ☁️ Cloud | 🏢 On-Prem | 🔀 Hybrid | 🌐 Common

| Term | Acronym | Model |Category|  Note | Tools | Talk About It With |
|---|---|---|---|---|---|---|
| Security Information & Event Management | SIEM | 🌐 | --- | Collects/correlates logs but doesn't respond on its own - that's SOAR | Splunk, Wazuh, Sentinel, QRadar | Log aggregation, correlation, SOC, SOAR |
| Resource Reuse | --- | ☁️ | --- | Cloud provider reassigns disks/storage to new tenants without wiping them-->vulnerability - old customer's sensitive data can leak to the new one | --- | Data remanence, disk sanitization, multi-tenancy |
| VM Escape | --- | ☁️/🔀 | --- | Vulnerability in the hypervisor lets an attacker break out of their VM and access the host or other VMs | --- | Hypervisor, resource reuse, multi-tenancy |
| VM Sprawl | --- | ☁️/🔀 | --- | VMs left running/not deprovisioned after they're no longer needed -Vulnerability - wastes resources and expands attack surface | --- | Resource reuse, asset management, shadow IT | 
| Legacy Vulnerabilities | --- | 🏢/🔀 | --- | Systems still running after the manufacturer has stopped supporting/patching them | --- | end of life |
| Baseline Lifecycle | --- | 🌐 | --- | cycle: establish → deploy → maintain → update | tools/vendors | 1. Baseline configuration(Establishing) ,2. Baseline deployment, 3. Baseline deviation/Drift (Maintaining), 4. Patch management(Update) | 
| Simple Network Management Protocol | SNMP | 🌐 | --- | **Monitors**/manages network-attached devices | SolarWinds, PRTG, Nagios | Network monitoring, Management Information Base (MIB), traps, TCP/IP |
| File Transfer Protocol | FTP | 🌐 | --- | **Transfers** files - unencrypted by default, so it's often flagged as insecure vs SFTP/FTPS | FileZilla, WinSCP | SFTP, FTPS, TCP port 21 |
| Simple Mail Transfer Protocol | SMTP | 🌐 | --- | **Sends/relays email** receiving uses different protocols (POP3/IMAP), a common exam trap | Postfix, Exchange, Sendmail | Email security, SPF, DKIM, DMARC |
| Domain Name System | DNS | 🌐 | --- | Translates/**Resolves** domain names to IP addresses frequently abused for spoofing/poisoning/tunneling attacks | BIND, Pi-hole, Route 53 | DNS spoofing, DNS sinkholing, DNSSEC |
| Shadow IT | — | 🌐 | Risk/Practice | Employees using unapproved tech/workarounds outside IT-approved process — e.g. personal device instead of proper guest access | — | Insider threat, unauthorized workaround, BYOD |
| Insider Threat | — | 🌐 | Threat Actor | Someone with legitimate access who creates risk, intentionally or not — broader category than shadow IT | — | Shadow IT, unauthorized access |
| Rogue Access Point | — | 🏢🔀 | Hardware/Attack | Unauthorized WAP physically connected to the network — different from a software/process workaround | — | Wireless security, evil twin |
| Black-Box Engagement | — | 🌐 | Testing Method | Pentesting, white-box, gray-box | — | Tester has zero prior knowledge of the target system — simulates an outside attacker | 
| SQL Injection | SQLi | 🌐 | Attack | Malicious SQL inserted via input fields to manipulate/access the database | sqlmap, Burp Suite | OWASP Top 10, input validation |
| Data in Use | — | 🌐 | Data State | Hardest to protect — must be decrypted and actively processed in memory | Confidential computing, TEE | Data at rest, data in transit, memory protection |
| Data in Transit | — | 🌐 | Data State | Vulnerable during transmission — protect with strong encrypted protocols | TLS, IPsec | Data in use, data at rest |
| Data at Rest | — | 🌐 | Data State | Generally easiest to secure — encryption + access controls | Disk/storage encryption, DLP | Data in use, data in transit | 
| Session Replay | — | 🌐 | Attack | Intercepted communications replayed to potentially bypass authentication | — | Session hijacking, authentication bypass |
| Typosquatting | — | 🌐 | Attack | Registering domains that closely resemble a legitimate site | — | Phishing, domain spoofing | 
| Watering Hole Attack | — | 🌐 | Attack | Attacker compromises a site the victim already visits, injects exploit code to redirect them | — | Social engineering, compromised sites, exploit code | 
| Pretexting | — | 🌐 | Attack/Social Engineering | Phishing, social engineering | — | Creating a fabricated scenario/situation to fool the target | |
| Signature-Based Monitoring | — | 🌐 | Detection Method | Compares traffic against known attack patterns — lightweight but blind to zero-days until signature exists | Snort, Suricata | IDS/IPS, known threats |
 Zero-Day Attack | — | 🌐 | Attack/Vulnerability | Exploit for a vulnerability with no existing patch/signature — best mitigated with behavior/anomaly detection | — | unknown software flaw, not a signature-based or anomaly-based detection, novel attack |
| Anomaly-Based Detection | — | 🌐 | Detection Method | Flags behavior that deviates from an established baseline | — | Baseline, behavior-based detection, zero-day |
| Stateless Firewall | — | 🌐 | Hardware/Software | Filters based on static factors like port and IP, no connection context | — | ACL, IP, port filtering, connectionless | 
| Stateful Firewall | — | 🌐 | Hardware/Software | Tracks the context/state of active connections | — | connection tracking |
| Application Log Files | — | 🌐 | Data Source | Contains security events, errors, and user activity — key input for SOC monitoring | Splunk, ELK | SIEM, security monitoring, user activity |
| System Baselining (CPU/Memory Monitoring) | — | 🌐 | Technique | Tracks normal CPU/memory usage to spot deviations indicating issues or attacks | Nagios, Zabbix | Anomaly-based detection, performance monitoring |
| Hardware Security Module | HSM | 🏢🔀 | Hardware Appliance | Used for encryption during secure login/auth, digital signing, payment security — preferred when performance matters, faster than software encryption | Thales, YubiHSM, AWS CloudHSM | TPM, encryption, digital signatures, key management |
| Host-Based Intrusion Detection System | HIDS | 🌐 | Software | Identifies suspicious behavior on a single system/host | OSSEC, Wazuh | IDS, endpoint monitoring, NIDS |
| Router | — | 🌐 | Hardware Appliance | Makes decisions about sending packets out of a network | Cisco, Juniper | Routing, packet forwarding, firewall | 
| Trusted Platform Module | TPM | 🏢🔀 | Hardware Appliance | Similar duties to HSM but built into/embedded in the system, whereas HSM is external/additional | — | HSM, secure boot, disk encryption |
| Due Care | — | 🌐 | Governance/Compliance | Regularly reviewing and updating policies, taking proactive steps to keep controls effective | — | Due diligence, policy review, compliance |
| Acknowledgment | — | 🌐 | Governance/Compliance | Employees stating they are aware of compliance requirements | — | Attestation, onboarding, policy sign-off | 
| Attestation | — | 🌐 | Governance/Compliance | Employee confirming their actions adhere to policies | — | Acknowledgment, audit, compliance |
| Offboarding | — | 🌐 | Process | Process used when an employee is terminated | — | Access revocation, onboarding, HR security | 


---

### Quick-Add Row (copy & fill)

```markdown
| Term Name | ACRONYM | ☁️/🏢/🔀/🌐 | is it a protocol,port, vulnerability,attack,hardware appliance, software,open source intelligence/knowleged/framework| related terms | tools/vendors | one-liner note | Comment here to revisit|
```
Disclaimer: This is just personal quick-reference notes, not an authoritative or exhaustive source, always cross-check against official documentation when it matters.
