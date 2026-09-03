# Task 4: Web Application Security & OWASP Top 10

## Executive Summary
This project focused on practical web application penetration testing using Damn Vulnerable Web Application (DVWA) to analyze, exploit, and remediate high-risk web vulnerabilities[cite: 3]. By combining manual exploitation techniques with automated vulnerability scanning, common application-layer security flaws were evaluated against the OWASP Top 10 framework[cite: 3].

---

## 🛠️ Tools & Technologies Used
* **Web Target:** `DVWA` (Damn Vulnerable Web Application - Low Security)[cite: 3]
* **Automated Scanner:** `OWASP ZAP`[cite: 3]
* **Traffic Interception & Analysis:** `Burp Suite`[cite: 3]
* **Operating System:** Linux CLI[cite: 3]

---

## 🔍 Key Activities & Exploitation Scenarios

### 1. Target Configuration & Environment Setup
* Deployed and configured DVWA locally, establishing a security level setting of **Low** for controlled vulnerability verification[cite: 3].
* Configured local proxy routing through `Burp Suite` and mapped application endpoints using `OWASP ZAP`[cite: 3].

### 2. Manual Vulnerability Exploitation
* **SQL Injection (SQLi):**
  * **Method:** Injected SQL control characters into user entry fields to bypass database queries[cite: 3].
  * **Result:** Successfully extracted hidden backend database schema and user records[cite: 3].
* **Reflected Cross-Site Scripting (XSS):**
  * **Method:** Crafted and submitted arbitrary client-side JavaScript payloads into unvalidated input fields[cite: 3].
  * **Result:** Executed inline scripts directly within the user context, demonstrating session hijacking risks[cite: 3].
* **Command Injection:**
  * **Method:** Appended shell command separators (`|`, `;`) to input parameters on diagnostic utilities (e.g., Ping)[cite: 3].
  * **Result:** Executed arbitrary host-level system commands directly on the web server[cite: 3].
* **Local File Inclusion (LFI):**
  * **Method:** Manipulated file path parameters using directory traversal sequences (`../../`)[cite: 3].
  * **Result:** Read sensitive system files including `/etc/passwd` directly from the server backend[cite: 3].
* **Cross-Site Request Forgery (CSRF):**
  * **Method:** Analyzed application state-changing requests lacking anti-CSRF tokens[cite: 3].
  * **Result:** Constructed external request triggers capable of performing unauthorized actions on behalf of authenticated users[cite: 3].

### 3. Automated Vulnerability Scanning & Verification
* Executed automated web application scans using `OWASP ZAP` to discover unlinked assets and flag security header deficiencies[cite: 3].
* Validated automated scanner alerts using `Burp Suite` to inspect raw HTTP request and response headers[cite: 3].

---

## 📄 Artifacts Included
* `Task_4_Web_App_Security.pdf` – Original internship testing report[cite: 3].

---

## 💡 Key Takeaways
* Strengthened manual penetration testing skills across core OWASP Top 10 risk vectors[cite: 3].
* Learned how to combine automated scanning tools (`OWASP ZAP`) with manual proxy analysis (`Burp Suite`) to verify security vulnerabilities[cite: 3].
* Understood the underlying coding mistakes that allow injection, directory traversal, and session-based attacks to succeed[cite: 3].