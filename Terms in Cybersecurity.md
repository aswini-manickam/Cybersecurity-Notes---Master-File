# Personal quick-reference table

Cybersecurity has countless terms, tools, and acronyms - with new ones surfacing constantly. 
So, this is a personal quick-reference table, filled in gradually as I come across new terms, so entries build up naturally over time rather than all at once. 
Updated regularly.

**Model key:** ☁️ Cloud | 🏢 On-Prem | 🔀 Hybrid | 🌐 Common

| Term | Acronym | Model |Category|  Note | Tools | Talk About It With | Comment |
|---|---|---|---|---|---|---|---|
| Security Information & Event Management | SIEM | 🌐 | --- | Collects/correlates logs but doesn't respond on its own - that's SOAR | Splunk, Wazuh, Sentinel, QRadar | Log aggregation, correlation, SOC, SOAR | - |
| Resource Reuse | --- | ☁️ | --- | Cloud provider reassigns disks/storage to new tenants without wiping them-->vulnerability - old customer's sensitive data can leak to the new one | --- | Data remanence, disk sanitization, multi-tenancy | CompTIA Security plus |
| VM Escape | --- | ☁️/🔀 |---| 	Hypervisor, resource reuse, multi-tenancy | ---| Vulnerability in the hypervisor lets an attacker break out of their VM and access the host or other VMs |CompTIA Security plus |
| VM Sprawl | --- | ☁️/🔀 |---| Resource reuse, asset management, shadow IT | --- | 	VMs left running/not deprovisioned after they're no longer needed -Vulnerability - wastes resources and expands attack surface | CompTIA Security plus Security plus |
| Legacy Vulnerabilities | --- | 🏢/🔀|---| related terms | --- | Systems still running after the manufacturer has stopped supporting/patching them | CompTIA Security plus |
| Baseline Lifecycle| --- | 🌐 |---| 1. Baseline configuration(Establishing) ,2. Baseline deployment, 3. Baseline deviation/Drift (Maintaining), 4. Patch management(	Update)| tools/vendors | cycle: establish → deploy → maintain → update | CompTIA Security plus |
| Simple Network Management Protocol | SNMP | 🌐 |---| Network monitoring, MIB, traps, TCP/IP | SolarWinds, PRTG, Nagios | **Monitors**/manages network-attached devices | CompTIA Security plus |
| File Transfer Protocol | FTP | 🌐 |---| SFTP, FTPS, TCP port 21 | FileZilla, WinSCP | **Transfers** files - unencrypted by default, so it's often flagged as insecure vs SFTP/FTPS | CompTIA Security plus |
| Simple Mail Transfer Protocol | SMTP | 🌐 |---| Email security, SPF, DKIM, DMARC | Postfix, Exchange, Sendmail | **Sends/relays email** receiving uses different protocols (POP3/IMAP), a common exam trap| CompTIA Security plus |
| Domain Name System | DNS | 🌐 |---| DNS spoofing, DNS sinkholing, DNSSEC | BIND, Pi-hole, Route 53 | Translates/**Resolves** domain names to IP addresses frequently abused for spoofing/poisoning/tunneling attacks | CompTIA Security plus|
| Shadow IT | — | 🌐 | Risk/Practice | Insider threat, unauthorized workaround, BYOD | — | Employees using unapproved tech/workarounds outside IT-approved process — e.g. personal device instead of proper guest access | |
| Insider Threat | — | 🌐 | Threat Actor | Shadow IT, unauthorized access | — | Someone with legitimate access who creates risk, intentionally or not — broader category than shadow IT | |
| Unskilled Attacker | — | 🌐 | Threat Actor | Script kiddie, existing tools | — | Limited technical knowledge, relies on off-the-shelf tools — not the same as an employee workaround | |
| Rogue Access Point | — | 🏢🔀 | Hardware/Attack | Wireless security, evil twin | — | Unauthorized WAP physically connected to the network — different from a software/process workaround | |
| Black-Box Engagement | — | 🌐 | Testing Method | Pentesting, white-box, gray-box | — | Tester has zero prior knowledge of the target system — simulates an outside attacker | |
| SQL Injection | SQLi | 🌐 | Attack | OWASP Top 10, input validation | sqlmap, Burp Suite | Malicious SQL inserted via input fields to manipulate/access the database | |
| Data in Use | — | 🌐 | Data State | Data at rest, data in transit, memory protection | Confidential computing, TEE | Hardest to protect — must be decrypted and actively processed in memory | |
| Data in Transit | — | 🌐 | Data State | Data in use, data at rest | TLS, IPsec | Vulnerable during transmission — protect with strong encrypted protocols | |
| Data at Rest | — | 🌐 | Data State | Data in use, data in transit | Disk/storage encryption, DLP | Generally easiest to secure — encryption + access controls | |
| Session Replay | — | 🌐 | Attack | Session hijacking, authentication bypass | — | Intercepted communications replayed to potentially bypass authentication | |
| Typosquatting | — | 🌐 | Attack | Phishing, domain spoofing | — | Registering domains that closely resemble a legitimate site | |
| Watering Hole Attack | — | 🌐 | Attack | Social engineering, compromised sites, exploit code | — | Attacker compromises a site the victim already visits, injects exploit code to redirect them | |
| Pretexting | — | 🌐 | Attack/Social Engineering | Phishing, social engineering | — | Creating a fabricated scenario/situation to fool the target | |
| Signature-Based Monitoring | — | 🌐 | Detection Method | IDS/IPS, known threats| Snort, Suricata | Compares traffic against known attack patterns — lightweight but blind to zero-days until signature exists | |
| Zero-Day Attack | — | 🌐 | Attack/Vulnerability | unknown software flaw ,not a Signature-based detection or anomaly-based detection , Novel attack | — | Exploit for a vulnerability with no existing patch/signature — best mitigated with behavior/anomaly detection | |
| Anomaly-Based Detection | — | 🌐 | Detection Method | Baseline, behavior-based detection,zero-day | — | Flags behavior that deviates from an established baseline | |
| Stateless Firewall | — | 🌐 | Hardware/Software | ACL, IP,port filtering,connectionless| — | Filters based on static factors like port and IP, no connection context | |
| Stateful Firewall | — | 🌐 | Hardware/Software | connection tracking | — | Tracks the context/state of active connections | |
| Application Log Files | — | 🌐 | Data Source | SIEM, security monitoring, user activity | Splunk, ELK | Contains security events, errors, and user activity — key input for SOC monitoring | |
| System Baselining (CPU/Memory Monitoring) | — | 🌐 | Technique | Anomaly-based detection, performance monitoring | Nagios, Zabbix | Tracks normal CPU/memory usage to spot deviations indicating issues or attacks | |
---  

### Quick-Add Row (copy & fill)

```markdown
| Term Name | ACRONYM | ☁️/🏢/🔀/🌐 | is it a protocol,port, vulnerability,attack,hardware appliance, software,open source intelligence/knowleged/framework| related terms | tools/vendors | one-liner note | Comment here to revisit|
```
Disclaimer: This is just personal quick-reference notes, not an authoritative or exhaustive source, always cross-check against official documentation when it matters.
