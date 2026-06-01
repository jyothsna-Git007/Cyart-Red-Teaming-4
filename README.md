# Advanced Red Teaming & Adversary Emulation Framework

Welcome to the **Advanced Red Teaming Lab**. This repository serves as a comprehensive operational syllabus and practical implementation framework for simulating high-tier threat actors (APTs), attacking cloud infrastructure, abusing native binaries, and developing evasive Command and Control (C2) channels.

## 🎯 Core Objectives
* **C2 Operations**: Deploy persistent, stealthy infrastructure using advanced application layer protocol beaconing.
* **Cloud Infrastructure Exploitation**: Identify misconfigurations, escalate IAM privileges, and execute covert data exfiltration.
* **Adversary Emulation**: Programmatically replicate known threat actor TTPs (e.g., APT29, Volt Typhoon, Sandworm).
* **Evasion & Living off the Land**: Bypass EDR/AV solutions using native binaries (LOLBAS) and process injection techniques.

---

## 🧠 Theoretical Knowledge Mapping

### 1. Advanced Command and Control (C2) Frameworks
* **Architecture**: Framework deployment for compromised host session management (**ATT&CK: T1071**).
* **Stealth Communications**: Covert channels using customized HTTPS and DNS profiles.
* **Payload Customization**: Generating stageless, environment-specific operational implants.
* **Resources**: [Cobalt Strike Docs](https://cobaltstrike.com) | [PoshC2 GitHub](https://github.com) | CISA Volt Typhoon Reports.

### 2. Cloud Environment Attacks
* **Cloud Reconnaissance**: Mapping AWS/Azure/GCP infrastructure vulnerabilities (**ATT&CK: T1580**).
* **Privilege Escalation**: Exploiting IAM role trust relationships and over-privileged service principals (**ATT&CK: T1078.004**).
* **Exfiltration**: Covert asset removal via cloud CLI tools (**ATT&CK: T1537**).
* **Resources**: [Rhino Security Labs CloudGoat](https://github.com) | Pacu Framework.

### 3. Adversary Emulation & Threat Simulation
* **Emulation Chains**: Mimicking specific state-sponsored TTPs (e.g., Cozy Bear phishing/persistence).
* **Orchestration**: Automating threat playbooks to stress-test blue team monitoring pipelines.
* **Resources**: [MITRE ATT&CK Navigator](https://github.io) | [MITRE Caldera](https://mitre.org).

### 4. Native Tool Abuse (Living off the Land)
* **Execution**: Fileless malware deployment leveraging native interpreters (PowerShell, WMI, CMD) (**ATT&CK: T1059**).
* **Injection**: Injecting payload threads into legitimate system processes like `explorer.exe` (**ATT&CK: T1055**).
* **Harvesting**: In-memory OS credential dumping using system tooling (**ATT&CK: T1003**).
* **Resources**: [LOLBAS Project](https://github.io) | PowerSploit.

### 5. Advanced Reporting & Debriefing
* **Technical Metrics**: Calculating phishing click-through metrics, CVSS risk ratings, and PTES compliance standards.
* **Executive Translation**: Distilling deeply technical attack chains into business risk remediation briefs.

---

## 🧪 Practical Application Labs & Logs

### Lab 1: Advanced C2 Lab
* **Tools**: Cobalt Strike, PoshC2, Metasploit.
* **Actions**: Configured an HTTPS beaconing profile; established stable sessions on a hardened Windows target environment using stageless loaders.


| Session ID | Target IP     | Payload Type | Notes             |
|------------|---------------|--------------|-------------------|
| SID001     | 192.168.1.50  | PowerShell   | Beacon established|

### Lab 2: Cloud Attack Lab
* **Tools**: Pacu, awscli, CloudGoat.
* **Actions**: Leveraged over-privileged user tokens to enumerate exposed storage backends and successfully escalated low-privilege keys to administrative roles.


| Asset ID | Service | Misconfiguration     | Notes              |
|----------|---------|---------------------|--------------------|
| AID001   | S3      | Public read access  | Vulnerable bucket  |

### Lab 3: Adversary Emulation Lab
* **Tools**: Caldera, Metasploit, Evilginx2.
* **Actions**: Automated multi-stage phishing, credential harvesting, and domain persistence playbooks. Evaluated detection gaps by checking telemetry in Wazuh SIEM logs.


| Phase       | TTP                | Tool Used | Notes               |
|-------------|--------------------|-----------|---------------------|
| Phishing    | T1566.001          | Evilginx2 | Credential harvest  |

### Lab 4: Advanced Evasion Lab
* **Tools**: msfvenom, Veil, proxychains.
* **Actions**: Evaded signature-based endpoint scanners via custom payload encoding. Obfuscated operational network source addresses by forcing traffic through proxy arrays.


| Payload ID | Type         | AV Detection | Notes             |
|------------|--------------|--------------|-------------------|
| PID001     | Meterpreter  | Bypassed     | Obfuscated payload|

### Lab 5: Cloud Privilege Abuse Simulation
* **Tools**: Pacu, awscli, ScoutSuite.
* **Actions**: Analyzed multi-tenant cross-account permissions. Exploited misconfigured service principal profiles to control cloud infrastructure nodes.


| Attack ID | Service | Misconfiguration      | Notes              |
|-----------|---------|----------------------|--------------------|
| AID002    | IAM     | Overprivileged role  | Escalated to admin |

### Lab 6: Automated Attack Orchestration
* **Tools**: Caldera, Red Team Automation (RTA).
* **Actions**: Orchestrated hands-free exploitation chains. Executed an automated pipeline spanning initial remote code execution up to persistence drop.


| Phase       | TTP                | Tool Used | Notes               |
|-------------|--------------------|-----------|---------------------|
| Exploitation| T1190              | Caldera   | Automated RCE       |

### Lab 7: Living-of-the-Land Lab
* **Tools**: PowerShell, WMI, Mimikatz.
* **Actions**: Extracted cached endpoint secrets directly out of volatile memory without generating files on disk, utilizing system configuration utilities.


| Attack ID | Tool       | Action            | Notes             |
|-----------|------------|-------------------|-------------------|
| LID001    | PowerShell | Fileless execution| Bypassed AV       |

---
⚠️ **Disclaimer**: The material inside this repository is intended purely for authorized security testing, educational purposes, and defensive defensive engineering validation.

