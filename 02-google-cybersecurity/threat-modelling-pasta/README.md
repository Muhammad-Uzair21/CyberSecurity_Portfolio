# PASTA Threat Modeling Framework

## Executive Summary
This project applies the Process for Attack Simulation and Threat Analysis (PASTA) risk-centric threat modeling methodology to evaluate an e-commerce sneaker application[cite: 4]. By stepping through all 7 PASTA stages, security controls were aligned with business goals, technology stacks were profiled, attack vectors were mapped, and risk mitigations were established to safeguard sensitive data and financial transactions[cite: 4].

---

## 🛠️ Framework & Methodology
* **Framework:** PASTA (Process for Attack Simulation and Threat Analysis) Stages I–VII[cite: 4]
* **Compliance Target:** PCI-DSS Compliance[cite: 4]
* **Application Focus:** E-commerce / Sneaker Platform (User Profiles, Financial Transactions, External APIs)[cite: 4]

---

## 🔍 The 7 PASTA Stages & Findings

### Stage I: Define Business Objectives
* Identified core business drivers: member profile management (internal or connected via external accounts) and processing financial transactions[cite: 4].
* Highlighted compliance targets, specifically establishing PCI-DSS alignment to protect payment data[cite: 4].

### Stage II: Define the Technical Scope
* Documented key technologies: Application Programming Interfaces (APIs), Public Key Infrastructure (PKI), SHA-256 hashing, and SQL databases[cite: 4].
* Prioritized APIs due to their role in data exchange between customers, partners, and employees, noting their large attack surface and elevated vulnerability risk[cite: 4].

### Stage III: Decompose Application
* Analyzed system interaction points and mapping dependencies using a Data Flow Diagram (DFD)[cite: 4].
* Identified entry points where sensitive user and payment data traverse system boundaries[cite: 4].

### Stage IV: Threat Analysis
* Evaluated probable threat vectors targeting the application's attack surface[cite: 4].
* Key threats identified: Injection attacks and Session Hijacking[cite: 4].

### Stage V: Vulnerability Analysis
* Audited technical scope for software vulnerabilities and missing defensive controls[cite: 4].
* Key vulnerabilities identified: Lack of prepared statements in database calls and broken API token validation[cite: 4].

### Stage VI: Attack Modeling
* Constructed sample attack tree diagrams to visualize potential exploit pathways threat actors could take to reach critical system assets[cite: 4].

### Stage VII: Risk Analysis and Impact
* Calculated overall business impact and mapped defensive counter-measures[cite: 4].
* Selected risk controls: Implementation of SHA-256 hashing, formal incident response procedures, strict password policies, and enforcing the principle of least privilege[cite: 4].

---

## 📄 Artifacts Included
* `PASTA_worksheet.pdf` – Completed PASTA threat modeling worksheet[cite: 4].

---

## 💡 Key Takeaways
* Learned how to align cybersecurity controls directly with business objectives and compliance requirements (PCI-DSS)[cite: 4].
* Gained experience using attack trees and Data Flow Diagrams (DFDs) to systematically decompose applications[cite: 4].
* Developed skills in mapping technical vulnerabilities to real-world threats and establishing effective remediation strategies[cite: 4].