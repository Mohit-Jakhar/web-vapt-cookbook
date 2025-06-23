****Open Source Tools – Installation & Usage****

This document provides step-by-step instructions for installing and using open-source tools required in Phase 2 of Web Application VAPT.

1. **Nmap**
- **Description**: Network port scanner that detects open ports, services, versions, and OS.
- **Install**:
  
  ```bash
  sudo apt update
  sudo apt install nmap
- **Basic Nmap Scan**: Scan top 1000 ports with default settings.
  
  ```bash
  nmap example.com
- **Scan All 65535 Ports**: Scans all TCP ports.

  ```bash
  nmap -p- example.com
- **Service Detection**:
  ```bash
  nmap -sC -sV -T4 -Pn example.com
- **Flags**:

    -sC – Run default scripts (e.g., banner grabbing)

    -sV – Detect service versions

    -T4 – Speed (1 to 5; 4 is fast and safe)

    -Pn – Skip pinging (treat host as up)


2. **Masscan**
- **Description**: Ultra-fast port scanner (like Nmap, but faster, no service detection).
- **Install**:
  
  ```bash
  sudo apt install masscan
- **Fast All-Port Scan**:
  ```bash
  masscan -p1-65535 <ip> --rate=1000
- **Flags**:

    -p1-65535 – Port Range

    --rate – Packets per Second

3. **FFUF**
- **Description**: Fast web fuzzer for directories, files, and parameters.
- **Install**:
  
  ```bash
  go install github.com/ffuf/ffuf/v2@latest
- **Usage**:
  ```bash
  ffuf -u https://example.com/FUZZ -w /usr/share/seclists/Discovery/Web-Content/common.txt
- **Use SecLists for wordlists with FFUF:**
  ```bash
  sudo apt update
  sudo apt install seclists


4. **DIRSEARCH**
- **Description**: Web path scanner to find hidden files and folders.
- **Install**:
  
  ```bash
  git clone https://github.com/maurosoria/dirsearch.git
  cd dirsearch
  pip3 install -r requirements.txt
- **Usage**:
  ```bash
  python3 dirsearch.py -u https://example.com -e php,html,js -x 403,404
- **Flags**:

    -e – Extensions to try
  
    -x – Exclude responses with these status codes
5. **PARAMSPIDER**
- **Description**: Extracts parameter names from web URLs and JS files.
- **Install**:
  
  ```bash
  git clone https://github.com/devanshbatham/paramspider.git
  cd paramspider
  pip3 install -r requirements.txt
- **Usage**:
  ```bash
  python3 paramspider.py --domain example.com

6. **Nuclei**
- **Description**: Template-based scanner for CVEs, misconfigs, and vulnerabilities.
- **Install**:
  
  ```bash
  go install -v github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest
  nuclei -update-templates
- **Usage**:
  ```bash
  nuclei -u https://example.com

7. **Nikto**
- **Description**: Web server scanner for outdated software and insecure configurations.
- **Install**:
  
  ```bash
  sudo apt install nikto
- **Usage**:
  ```bash
  nikto -h https://example.com

8. **WhatWeb**
- **Description**: Web technology fingerprinting tool.
- **Install**:
  
  ```bash
  sudo apt install whatweb
- **Usage**:
  ```bash
  whatweb https://example.com
