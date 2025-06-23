🔍 Phase 2: Scanning & Enumeration

🎯 Objective

To actively scan the target for open ports, services, directories, parameters, and possible vulnerabilities. This phase is crucial for mapping the real attack surface and identifying exploitable components.

🔎 What Happens in This Phase?

| Category                | Description                                              |
|-------------------------|----------------------------------------------------------|
| Port Scanning           | Identify open TCP/UDP ports and services                 |
| Service Enumeration     | Detect versions of services like Apache, MySQL, etc.     |
| Directory Brute Force   | Find hidden folders like `/admin`, `/uploads`, etc.      |
| Parameter Enumeration   | Find GET/POST parameters, cookies, etc.                  |
| Vulnerability Scanning  | Automated scanning for known CVEs or weaknesses          |


🧠 Key Concepts

- Enumeration helps in identifying assets like login panels, file uploads, or APIs.
- Scanning helps detect known misconfigurations or unpatched services.
- It's often noisy — requires proper authorization in professional assessments.


🧰 Tools Used in This Phase

| Tool            | What It Does                                               | Why It's Important                                                                      |
| --------------- | ---------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| **Nmap**        | Scans open ports, detects services and versions            | Identifies exposed ports and services, builds the foundation for attack surface mapping |
| **Masscan**     | Performs lightning-fast port scanning                      | Useful for large-scale IP/port scanning where speed is crucial                          |
| **FFUF**        | Brute-forces directories and files on web servers          | Helps discover hidden endpoints like `/admin`, `/login`, `/backup.zip`                  |
| **Dirsearch**   | Recursively enumerates paths and extensions                | Allows filtered and targeted directory discovery with extension support                 |
| **ParamSpider** | Crawls URLs and JS files to find parameters                | Extracts potential attack vectors from deeply embedded or undocumented locations        |
| **Nuclei**      | Scans for known CVEs and misconfigurations using templates | Enables fast, automated vulnerability assessment with real-time CVE checks              |
| **Nikto**       | Detects outdated software and insecure server settings     | Good for baseline server misconfigurations and weak SSL/TLS setups                      |
| **WhatWeb**     | Fingerprints technologies used by the application          | Helps prioritize based on known-vulnerable tech like outdated CMS, PHP versions         |


For tools installation and usage, refer to the Installation.md
