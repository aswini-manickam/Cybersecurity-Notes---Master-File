# Personal quick-reference table

Cybersecurity has countless terms, tools, and acronyms - with new ones surfacing constantly. 
So, this is a personal quick-reference table, filled in gradually as I come across new terms, so entries build up naturally over time rather than all at once. 
Updated regularly.

**Model key:** ☁️ Cloud | 🏢 On-Prem | 🔀 Hybrid | 🌐 Common

| Term | Acronym | Model | Talk About It With | Tools | Note | Comment |
|---|---|---|---|---|---|---|
| Identity & Access Management | IAM | 🌐 | AAA, SSO, MFA, PAM, RBAC | CyberArk, Okta, Entra ID | Umbrella term — PAM/CyberArk is only for privileged accounts, not all identities |-|
| Security Information & Event Management | SIEM | 🌐 | Log aggregation, correlation, SOC, SOAR | Splunk, Wazuh, Sentinel, QRadar | Collects/correlates logs but doesn't respond on its own - that's SOAR | - |
| Resource Reuse | --- | ☁️ | Data remanence, disk sanitization, multi-tenancy | --- | 	Cloud provider reassigns disks/storage to new tenants without wiping them-->vulnerability - old customer's sensitive data can leak to the new one |CompTIA Security plus security+|
| VM Escape | --- | ☁️/🔀 | 	Hypervisor, resource reuse, multi-tenancy | ---| Vulnerability in the hypervisor lets an attacker break out of their VM and access the host or other VMs |CompTIA Security plus security+|
| VM Sprawl | --- | ☁️/🔀 | Resource reuse, asset management, shadow IT | --- | 	VMs left running/not deprovisioned after they're no longer needed -Vulnerability - wastes resources and expands attack surface | CompTIA Security plus Security plus |
| Legacy Vulnerabilities | --- | 🏢/🔀| related terms | --- | Systems still running after the manufacturer has stopped supporting/patching them | CompTIA Security plus |
| Baseline Lifecycle| --- | 🌐 | 1. Baseline configuration(Establishing) ,2. Baseline deployment, 3. Baseline deviation/Drift (Maintaining), 4. Patch management(	Update)| tools/vendors | cycle: establish → deploy → maintain → update | CompTIA Security plus |
| Simple Network Management Protocol | SNMP | 🌐 | Network monitoring, MIB, traps, TCP/IP | SolarWinds, PRTG, Nagios | Monitors/manages network-attached devices | CompTIA Security plus |
| File Transfer Protocol | FTP | 🌐 | SFTP, FTPS, TCP port 21 | FileZilla, WinSCP | Transfers files - unencrypted by default, so it's often flagged as insecure vs SFTP/FTPS | CompTIA Security plus |
| Simple Mail Transfer Protocol | SMTP | 🌐 | Email security, SPF, DKIM, DMARC | Postfix, Exchange, Sendmail | Sends/relays email — receiving uses different protocols (POP3/IMAP), a common exam trap| CompTIA Security plus |
| Domain Name System | DNS | ☁️/🏢/🔀/🌐 | DNS spoofing, DNS sinkholing, DNSSEC | BIND, Pi-hole, Route 53 | Translates domain names to IP addresses — frequently abused for spoofing/poisoning/tunneling attacks | CompTIA Security plus|
---

### Quick-Add Row (copy & fill)

```markdown
| Term Name | ACRONYM | ☁️/🏢/🔀/🌐 | related terms | tools/vendors | one-liner note | Comment here to revisit|
```
Disclaimer: This is just personal quick-reference notes, not an authoritative or exhaustive source, always cross-check against official documentation when it matters.
