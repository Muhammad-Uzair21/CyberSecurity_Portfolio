# Google Cybersecurity Certificate Overview

This directory contains portfolio projects, lab documentation, incident analysis reports, and risk assessments completed as part of the Google Cybersecurity Professional Certificate. The work here focuses on applied security frameworks, network traffic analysis, threat modeling, and incident response procedures aligned with industry standards.

---

## 📂 Subdirectory Structure
```text

02-google-cybersecurity/
├── README.md
├── threat-modeling-pasta/
│   └── README.md
├── vulnerability-assessments/
│   └── README.md
└── incident-response/
    └── README.md

```

---

## 🛠️ Module Breakdown & Key Deliverables

### [PASTA Threat Modeling Framework](./threat-modeling-pasta/)
* **Objective:** Conduct a comprehensive 7-stage threat modeling analysis using the Process for Attack Simulation and Threat Analysis (PASTA) methodology for a sample e-commerce application[cite: 4].
* **Core Frameworks:** PASTA Stages I–VII, PCI-DSS Compliance[cite: 4].
* **Key Achievements:**
  * Defined business objectives, sensitive transaction flows, and technical scope prioritizing key application programming interfaces (APIs)[cite: 4].
  * Mapped system components via Data Flow Diagrams (DFDs) and evaluated vulnerabilities such as lack of prepared statements and broken API tokens[cite: 4].
  * Built attack trees and recommended security risk controls including SHA-256 hashing, password policies, incident response procedures, and the principle of least privilege[cite: 4].

---

### [NIST SP 800-30 Vulnerability Assessment](./vulnerability-assessments/)
* **Objective:** Assess organizational security risks and evaluate database server access controls based on the NIST SP 800-30 Rev. 1 framework[cite: 7].
* **Core Frameworks:** NIST SP 800-30 Rev. 1, Risk Assessment Matrix[cite: 7].
* **Key Achievements:**
  * Evaluated server hardware, Linux OS configurations, and MySQL database assets carrying sensitive customer and business data[cite: 7].
  * Calculated risk scores by analyzing threat sources (competitors, disgruntled employees, malicious hackers) against likelihood and severity metrics[cite: 7].
  * Developed a remediation strategy prioritizing TLS encryption in transit, strict Role-Based Access Controls (RBAC), Multi-Factor Authentication (MFA), and corporate IP allow-listing[cite: 7].

---

### [Incident Response & Network Traffic Analysis](./incident-response/)
* **Objective:** Investigate security events, triage network protocol logs, isolate threat vectors, and document response plans aligned with the NIST Cybersecurity Framework (CSF)[cite: 5, 6, 8, 9, 10].
* **Core Tools & Frameworks:** NIST CSF (Identify, Protect, Detect, Respond, Recover), `tcpdump`, `Wireshark`, `VirusTotal`, SIEM, Phishing Playbook[cite: 5, 6, 8, 9, 10].
* **Key Achievements:**
  * **Phishing & Malware Triage:** Investigated suspicious emails carrying malicious attachments (`bfsvc.exe`, SHA-256 hash `54e6ea...7f6b`), performed file hash analysis on VirusTotal, and created escalated L2 SOC tickets[cite: 5, 10].
  * **Ransomware Investigation:** Documented incident handler notes on phishing-based ransomware outbreaks impacting healthcare systems and evaluated recovery strategies[cite: 5].
  * **DDoS & ICMP Flood Mitigation:** Applied NIST CSF stages to mitigate ICMP flood attacks by establishing firewall rate-limiting rules, IDS/IPS filtering, and IP spoof verification[cite: 9].
  * **DNS & Web Redirection Analysis:** Diagnosed DNS lookup failures (UDP Port 53 unreachable) and captured `tcpdump` logs to analyze unauthorized web browser redirects caused by compromised administrator credentials[cite: 6, 8].

---

## 📈 Key Takeaways & Competencies

* **Framework Alignment:** Practical application of NIST CSF, NIST SP 800-30 Rev. 1, and the PASTA threat modeling methodology to evaluate risk postures[cite: 4, 7, 9].
* **Incident Handling & SOC Operations:** Experience analyzing malware hashes, isolating malicious email payloads, and updating SIEM/IDS escalation tickets[cite: 5, 10].
* **Protocol & Packet Analysis:** Proficiency in using command-line (`tcpdump`) and GUI (`Wireshark`) packet analyzers to diagnose network protocol errors and traffic anomalies[cite: 5, 6, 8].