# Task 2: Networking, Reconnaissance & Traffic Analysis

## Executive Summary
This project focuses on basic network reconnaissance, protocol analysis, and threat mapping[cite: 2]. Using industry-standard networking tools, network hosts were discovered, active services were enumerated, and network traffic was captured to analyze protocol behaviors[cite: 2]. Discovered findings were mapped against known vulnerability databases (CVE, CVSS) and standard attack frameworks (MITRE ATT&CK)[cite: 2].

---

## 🛠️ Tools & Technologies Used
* **Network Discovery & Scanning:** `Nmap`, `ping`[cite: 2]
* **Traffic Capture & Analysis:** `Wireshark`[cite: 2]
* **Environment:** Linux CLI / Virtual Lab Environment[cite: 2]
* **Frameworks:** CVE, CVSS, MITRE ATT&CK[cite: 2]

---

## 🔍 Key Activities & Methodology

### 1. Network Discovery & Enumeration
* **Subnet & Range Analysis:** Identified public and private IP address ranges within the virtual lab topology[cite: 2].
* **Host Reachability:** Used ICMP `ping` testing to confirm host reachability across internal network segments[cite: 2].
* **Port & Service Scanning (`Nmap`):**
  * **Host Discovery (`-sn`):** Located active hosts on the target subnet without executing port scans[cite: 2].
  * **Service Version Detection (`-sV`):** Enumerated open ports and determined running service versions on target machines[cite: 2].
  * **OS Fingerprinting (`-O`):** Identified target operating systems based on TCP/IP stack behavior[cite: 2].
  * **Aggressive Scan (`-A`):** Combined OS detection, version detection, script scanning, and traceroute for detailed host profiling[cite: 2].

### 2. Traffic Analysis & Packet Capture
* **Wireshark Capture Execution:** Captured live network traffic on active network interfaces during active scans[cite: 2].
* **ICMP Protocol Analysis:** Monitored ICMP echo request and reply flows to verify connection latency and packet loss[cite: 2].
* **HTTP Traffic Inspection:** Analyzed unencrypted HTTP requests and responses saved to `.pcapng` format to observe header structures and data transmission[cite: 2].

### 3. Vulnerability & Threat Mapping
* **CVE & CVSS Assessment:** Mapped identified service vulnerabilities to Common Vulnerabilities and Exposures (CVE) IDs and evaluated risk severity scores via CVSS metrics[cite: 2].
* **MITRE ATT&CK Framework:** Correlated reconnaissance activities and initial access vectors to specific MITRE ATT&CK Tactics, Techniques, and Procedures (TTPs)[cite: 2].

---

## 📄 Artifacts Included
* `Task_2_Networking_Reconnaissance.pdf` – Original internship report[cite: 2].

---

## 💡 Key Takeaways
* Mastered command-line parameters in `Nmap` for network reconnaissance[cite: 2].
* Developed skills in inspecting packet captures via `Wireshark`[cite: 2].
* Applied standardized frameworks (CVE/CVSS/MITRE ATT&CK) to contextualize raw reconnaissance findings into actionable threat intelligence[cite: 2].