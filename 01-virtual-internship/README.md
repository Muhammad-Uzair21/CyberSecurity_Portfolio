# Virtual Cybersecurity Internship Overview

This directory contains all technical deliverables, lab exercises, and vulnerability reports completed during the Virtual Cybersecurity Internship. The focus of this module spans network reconnaissance, protocol analysis, web application security assessments, and hands-on vulnerability exploitation across real-world virtual lab environments.

---

## 📂 Subdirectory Structure
```text

01-virtual-internship/
├── README.md
├── task-2-networking-recon/
│   └── README.md
├── task-3-vulnerability-assessment/
│   └── README.md
└── task-4-web-app-security/
    └── README.md

```
---

## 🛠️ Module Breakdown & Key Deliverables

### [Task 2: Networking, Reconnaissance & Traffic Analysis](./task-2-networking-recon/)
* **Objective:** Map network targets, identify open ports and active services, capture live packet traffic, and analyze security vulnerabilities[cite: 2].
* **Core Tools:** `Nmap`, `Wireshark`, `ping`, Linux CLI[cite: 2].
* **Key Achievements:**
  * Executed host discovery (`-sn`), service version detection (`-sV`), OS fingerprinting (`-O`), and aggressive scans (`-A`) across target host environments[cite: 2].
  * Captured ICMP echo requests/replies and analyzed HTTP network traffic streams saved to `.pcapng` format[cite: 2].
  * Mapped discovered vulnerabilities to CVE identifiers, evaluated CVSS severity metrics, and aligned threat actor behaviors to the MITRE ATT&CK framework[cite: 2].

---

### [Task 3: Web Vulnerability Assessment & Server Scanning](./task-3-vulnerability-assessment/)
* **Objective:** Deploy vulnerable web targets, inspect HTTP request/response pipelines, and identify security flaws in web application infrastructure[cite: 1].
* **Core Tools:** `OWASP Juice Shop`, `Burp Suite` (Proxy, Repeater, Intruder, Decoder), `Nikto`, `Nmap`[cite: 1].
* **Key Achievements:**
  * Hosted OWASP Juice Shop locally and intercepted web traffic using Burp Suite Proxy[cite: 1].
  * Conducted web server vulnerability scans with Nikto to uncover server configuration risks[cite: 1].
  * Documented high-severity security findings, including SQL Injection (Authentication Bypass) and Broken Access Control (Unauthorized Direct File Access)[cite: 1].

---

### [Task 4: Web Application Security & OWASP Top 10](./task-4-web-app-security/)
* **Objective:** Perform hands-on manual penetration testing and automated scanning against OWASP Top 10 web application vulnerabilities[cite: 3].
* **Core Tools:** `DVWA` (Damn Vulnerable Web Application), `OWASP ZAP`, `Burp Suite`[cite: 3].
* **Key Achievements:**
  * Environment setup and target configuration using DVWA set to Low Security mode[cite: 3].
  * Manually exploited core web vulnerabilities:
    * **SQL Injection (SQLi):** Extracted backend database information[cite: 3].
    * **Reflected XSS:** Injected arbitrary JavaScript payloads into web inputs[cite: 3].
    * **Command Injection:** Executed system-level commands on the underlying target system[cite: 3].
    * **Local File Inclusion (LFI):** Read sensitive server files (`/etc/passwd`)[cite: 3].
    * **Cross-Site Request Forgery (CSRF):** Crafting unauthorized state-changing requests[cite: 3].
  * Conducted automated vulnerability scans using OWASP ZAP and inspected modified HTTP headers/payloads in Burp Suite[cite: 3].

---

## 📈 Key Takeaways & Competencies

* **Reconnaissance Mastery:** Proficient in using `Nmap` for host discovery, port scanning, and service enumeration while analyzing traffic flows in `Wireshark`[cite: 2].
* **Web Pentesting & Interception:** Deep understanding of HTTP request manipulation using `Burp Suite` to identify and exploit common OWASP Top 10 flaws[cite: 1, 3].
* **Vulnerability & Risk Analysis:** Ability to analyze target security postures using automated scanners (`Nikto`, `OWASP ZAP`) and document actionable remediation strategies[cite: 1, 3].