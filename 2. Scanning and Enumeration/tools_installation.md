**🧰 Open Source Tools – Installation & Usage**

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

