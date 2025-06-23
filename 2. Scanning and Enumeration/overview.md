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

  Open-Source Tools Summary

  | Tool            | Purpose & Importance                                                                                                                            |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nmap**        | Industry-standard for scanning open ports and fingerprinting services. Crucial for identifying live hosts, exposed ports, and service versions. |
| **Masscan**     | Ultra-fast port scanner to identify open ports at scale. Used when speed is critical and you're scanning large IP ranges.                       |
| **FFUF**        | Web fuzzer used for directory and file brute-forcing. Helps discover hidden endpoints like `/admin`, `/api`, or misconfigured directories.      |
| **Dirsearch**   | Python-based web path discovery tool. Useful for recursive directory busting and filtering status codes or extensions.                          |
| **ParamSpider** | Crawls target domains and JS files to extract URL parameters. Helps in identifying overlooked or undocumented parameters for fuzzing.           |
| **Nuclei**      | Powerful template-based vulnerability scanner. Quickly detects known CVEs, misconfigurations, and common security issues in web apps.           |
| **Nikto**       | Lightweight web server scanner. Finds outdated server software, exposed files, and insecure HTTP headers.                                       |
| **WhatWeb**     | Detects technologies, frameworks, and plugins used by a web app. Useful for determining if known-vulnerable tech is in use.                     |

