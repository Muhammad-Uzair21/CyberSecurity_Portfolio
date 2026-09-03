# Incident Response & Network Traffic Analysis

## Executive Summary
This folder aggregates incident handler journals, packet captures, and triage activities completed as part of the Google Cybersecurity Certificate. Scenarios cover phishing investigations, malware hash analysis, DDoS mitigation using the NIST Cybersecurity Framework (CSF), and DNS/HTTP packet analysis via CLI log inspection.

---

## 🛠️ Tools & Frameworks Used
* **Frameworks:** NIST Cybersecurity Framework (Identify, Protect, Detect, Respond, Recover)
* **Traffic & Log Analysis Tools:** `tcpdump`, `Wireshark`, Linux CLI
* **Threat Intelligence & SIEM:** `VirusTotal`, SIEM Alert Logs, Incident Escalation Ticketing Systems

---

## 🔍 Incident Summaries & Handlers' Journals

### 1. Phishing & Malware Escalation Triage
* **Scenario:** Investigation of a suspicious email containing a malicious attachment executable (`bfsvc.exe`).
* **Analysis:** Extracted the file payload's SHA-256 hash (`54e6ea...7f6b`) and cross-referenced threat intelligence using VirusTotal to verify malicious indicators.
* **Action:** Generated an L2 SOC escalation ticket detailing the IOCs (Indicators of Compromise) and initiated quarantine procedures.

### 2. Healthcare Ransomware Analysis
* **Scenario:** Reviewed a ransomware outbreak impacting healthcare system availability via email-based initial access.
* **Analysis:** Documented incident handler notes evaluating how unpatched endpoint software and lack of network segmentation accelerated payload propagation.
* **Action:** Formulated recovery strategies prioritizing offline backup validation and domain credential resets.

### 3. DDoS Incident Mitigation (NIST CSF)
* **Scenario:** High-volume ICMP flood attack targeting internal web server infrastructure, disrupting normal network availability.
* **Application of NIST CSF:**
  * **Identify:** Flagged degraded network performance and mapped critical target assets.
  * **Protect:** Implemented firewall rate-limiting policies and strict ICMP packet filtering rules.
  * **Detect:** Configured IDS/IPS alert triggers for anomalous traffic spikes.
  * **Respond:** Isolated target segments and initiated traffic scrubbing protocols.
  * **Recover:** Verified normal traffic flow, restored service availability, and documented post-incident lessons learned.

### 4. DNS & Malicious Web Redirection Analysis
* **Scenario:** Investigated user reports regarding unreachable external domains and unexpected browser redirects.
* **Traffic Analysis:**
  * Analyzed network logs revealing DNS lookup failures on **UDP Port 53** (Destination Unreachable).
  * Inspected packet traces via `tcpdump` to trace unauthorized URL redirection streams targeting `greatrecipesforme.com` caused by compromised admin credentials.
* **Action:** Restored DNS resolution settings, revoked compromised credentials, and implemented strict egress firewall filtering.

---

## 📄 Artifacts Included
* `Incident_handler's_journal.pdf`
* `Incident_analysis_Network.pdf`
* `Incident_response_DDoS.pdf`
* `Incident_report_Phising.pdf`

---

## 💡 Key Takeaways
* Applied the NIST Cybersecurity Framework stages to contain and recover from active network attacks.
* Developed skills in extracting threat intelligence (IOCs, hashes) to triage phishing and malware threats.
* Used command-line traffic tools (`tcpdump`) to isolate network protocol failures and malicious redirects.