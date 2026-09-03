# NIST SP 800-30 Vulnerability Assessment

## Executive Summary
This project outlines a risk assessment for a database server environment following the NIST SP 800-30 Rev. 1 guidelines[cite: 7]. The assessment evaluates server assets, system vulnerabilities, threat sources, and business operational risks over a three-month evaluation period (June 2026 to August 2026) to protect sensitive data and support business continuity[cite: 7].

---

## 🛠️ System Description & Scope
* **Hardware & OS:** High-performance Linux server hardware with 128GB RAM running the latest Linux distribution[cite: 7].
* **Database & Connectivity:** Hosted MySQL database management system with IPv4 network binding and SSL/TLS network encryption[cite: 7].
* **Scope:** Database server access controls and system infrastructure assessed under NIST SP 800-30 Rev. 1 guidelines[cite: 7].
* **Business Purpose:** Safeguard sensitive customer and organizational records against leaks, unauthorized modifications, or breaches that could trigger business operational disruption, financial impact, or reputational damage[cite: 7].

---

## 🔍 Risk Assessment (NIST SP 800-30 Rev. 1)

| Threat Source | Threat Event | Likelihood (1-3) | Severity (1-3) | Risk Score |
| :--- | :--- | :---: | :---: | :---: |
| **Competitors** | Exfiltrate and obtain sensitive information[cite: 7] | 1 | 3 | **3**[cite: 7] |
| **Disgruntled Employee** | Sell sensitive information for personal gain[cite: 7] | 1 | 3 | **3**[cite: 7] |
| **Malicious Hackers** | Exploit vulnerabilities to access database assets and customer data[cite: 7] | 2 | 3 | **6**[cite: 7] |

---

## 🛠️ Recommended Remediation Strategy

* **Authentication & Access Control:**
  * Implement robust Authentication, Authorization, and Auditing (AAA) mechanisms[cite: 7].
  * Enforce strict password requirements, Role-Based Access Control (RBAC), and Multi-Factor Authentication (MFA)[cite: 7].
* **Data Transit Security:**
  * Standardize on TLS encryption for data in transit and phase out obsolete SSL protocols[cite: 7].
* **Network Segmentation & Filtering:**
  * Restrict database access through corporate IP allow-listing to prevent unauthorized external connections from the public internet[cite: 7].

---

## 📄 Artifacts Included
* `Vulnerability_assessment_report.pdf` – Original NIST SP 800-30 Rev. 1 risk assessment report[cite: 7].

---

## 💡 Key Takeaways
* Applied NIST SP 800-30 Rev. 1 methodologies to calculate threat likelihood, severity, and risk scores[cite: 7].
* Balanced security enforcement against operational business needs[cite: 7].
* Selected defensive controls (TLS, MFA, RBAC, IP allow-listing) to protect backend database assets[cite: 7].