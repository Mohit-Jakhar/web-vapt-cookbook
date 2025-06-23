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


| Category                    | Tool                                           | Description                                   | Type                    |
| --------------------------- | ---------------------------------------------- | --------------------------------------------- | ----------------------- |
| **Network Scan**            | **Nmap**, **Masscan**                          | Standard for port & service discovery         | Open Source             |
|                             | **RustScan**                                   | Blazingly fast scanner with Nmap integration  | Open Source             |
|                             | **ZMap**                                       | Internet-scale port scanning                  | Open Source             |
| **Subdomain Discovery**     | **Amass**, **Subfinder**, **Assetfinder**      | Find large attack surface                     | Open Source             |
|                             | **SecurityTrails**, **Censys**, **Shodan**     | Passive OSINT on infra & ports                | Mixed (Free + Paid API) |
| **Web Enumeration**         | **FFUF**, **Dirsearch**, **Gobuster**          | Find hidden endpoints                         | Open Source             |
|                             | **Burp Suite Pro**                             | Spider, content discovery, active scanning    | ⚠️ Paid                 |
|                             | **Feroxbuster**                                | Fast recursive content discovery (Rust-based) | Open Source             |
| **Parameter Discovery**     | **Arjun**, **ParamSpider**, **GF + grep**      | Extract parameters for fuzzing                | Open Source             |
|                             | **Burp Param Miner (Ext)**                     | Guess hidden parameters via cache probing     | Burp Plugin             |
| **Tech Stack Detection**    | **WhatWeb**, **Wappalyzer CLI**, **WebTech**   | CMS, JS libs, plugins                         | Open Source             |
|                             | **BuiltWith**, **Netcraft**                    | Web fingerprinting services                   | Paid                    |
| **CVE Detection**           | **Nuclei**, **Vulners**, **OpenVAS**           | Template or signature-based scanning          | Open Source             |
|                             | **Burp Pro Active Scan**, **Nessus**           | Commercial-grade CVE detection                | ⚠️ Paid                 |
| **JS Analysis**             | **LinkFinder**, **JSParser**, **SecretFinder** | Scrape API keys, URLs, endpoints              | Open Source             |
|                             | **GitLeaks**, **TruffleHog**                   | Secret discovery in JS, Git, etc.             | Open Source             |
| **DNS / VHOST Enumeration** | **dnsx**, **vhostscan**, **massdns**           | Subdomain + VHost fuzzing                     | Open Source             |
|                             | **Burp Turbo Intruder**, **Custom Wordlists**  | Bypass rate-limits, virtual host hijack       | Mixed                   |
| **Crawlers**                | **Hakrawler**, **Katana**, **Crawlcat**        | Crawl web apps for inputs                     | Open Source             |
| **Automation Suites**       | **ReconFTW**, **LazyRecon**, **BugHunter**     | Toolchains for automation                     | Open Source             |

