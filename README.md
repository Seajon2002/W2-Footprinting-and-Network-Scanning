# 🔐 Footprinting & Network Scanning

### Cybersecurity Internship Project | Networkwalks | Week 02

<p align="center">
  <img src="https://img.shields.io/badge/Domain-Cybersecurity-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Program-Networkwalks-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Batch-B084-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Week-02-purple?style=for-the-badge" />
</p>

## 📌 Project Overview

This repository documents my hands-on cybersecurity internship activities focused on **Footprinting, Reconnaissance, OSINT, DNS Enumeration, Web Technology Fingerprinting, and Local Network Discovery**.

The project demonstrates the practical use of industry-standard cybersecurity tools to gather publicly available domain information, identify web technologies, enumerate DNS records, analyze HTTP response headers, detect Web Application Firewalls, visualize domain relationships, and discover active hosts within a local network.

The activities were completed as part of the **Networkwalks Cybersecurity Internship Program – Week 02**.

---

## 🎯 Project Objectives

- Understand the fundamentals of footprinting and reconnaissance.
- Gather publicly available domain registration information.
- Identify website technologies and server information.
- Perform DNS resolution and DNS record enumeration.
- Analyze HTTP response headers.
- Detect Web Application Firewall technologies.
- Perform OSINT-based domain relationship mapping.
- Discover active devices within a local network.
- Visualize network topology using Zenmap.
- Document security observations and provide recommendations.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Cybersecurity testing environment |
| WHOIS | Domain registration information gathering |
| WhatWeb | Website technology fingerprinting |
| Nslookup | DNS resolution |
| Curl | HTTP response header analysis |
| Wafw00f | Web Application Firewall detection |
| DNSRecon | DNS record enumeration |
| Maltego | OSINT and relationship mapping |
| Nmap | Network discovery |
| Zenmap | Graphical network scanning and topology visualization |

---

## 📚 Practical Modules

| Module | Description |
|---|---|
| W2-PM1 | Footprinting & Reconnaissance using Kali Linux tools |
| W2-PM3 | OSINT and Domain Relationship Mapping using Maltego |
| W2-PM5 | Local Network Discovery using Zenmap |

---

## 🔎 Practical Tasks & Execution

### 1. WHOIS – Domain Information Gathering

**Command:**

```bash
whois networkwalks.com
```

**Key Observations:**
- Registrar: GoDaddy.com, LLC
- Domain Creation Date: 06 November 2019
- Name Servers: HostGator
- Domain Privacy: Domains By Proxy, LLC
- Domain status information collected.

**Objective:** Gather publicly available domain registration and infrastructure-related information.

### 2. WhatWeb – Website Technology Fingerprinting

**Command:**

```bash
whatweb networkwalks.com
```

**Key Observations:**
- Web Server: Apache
- CMS: WordPress
- WordPress Version: 7.1.4 (as detected by WhatWeb)
- Detected Plugin: WP Download Manager 3.3.76
- JavaScript Library: jQuery 3.7.1
- Website IP: `192.232.216.135`
- HTTP Response: 200 OK

**Objective:** Identify publicly detectable website technologies, CMS information, and related components.

### 3. Nslookup – DNS Resolution

**Command:**

```bash
nslookup networkwalks.com
```

**Key Observations:**
- DNS Server: `8.8.8.8`
- Resolved IP Address: `192.232.216.135`
- Response Type: Non-authoritative Answer

**Objective:** Resolve the target domain into its corresponding IP address.

### 4. Curl – HTTP Header Analysis

**Command:**

```bash
curl -I https://networkwalks.com
```

**Key Observations:**
- HTTP Response: HTTP/2 200
- Server: Apache
- Content-Type: text/html; charset=UTF-8
- WordPress REST API endpoint: `/wp-json/`
- HTTP response and security-related headers identified.

**Objective:** Inspect HTTP response headers and identify publicly exposed application information.

### 5. Wafw00f – WAF Detection

**Command:**

```bash
wafw00f networkwalks.com
```

**Key Observations:**
- WAF Detected: Yes
- Identified WAF: ModSecurity (SpiderLabs)
- Tool Version: 2.4.2
- Number of Requests: 2

**Objective:** Identify the presence and type of Web Application Firewall.

### 6. DNSRecon – DNS Enumeration

**Command:**

```bash
dnsrecon -d networkwalks.com
```

**Key Observations:**
- SOA Records identified.
- NS Records identified.
- MX Record identified.
- A Record identified.
- TXT Records identified.
- SRV Records identified.
- Total Records Found: 8.

**Objective:** Enumerate DNS records and understand publicly visible domain and email infrastructure.

### 7. Maltego – OSINT & Relationship Mapping

**Tool:** Maltego Desktop 4.11.3

**Activities:**
- Domain-related entity analysis.
- Registrar relationship identification.
- Registry and WHOIS service mapping.
- Visualization of publicly available domain relationships.

**Objective:** Understand relationships between domain-related entities through visual OSINT analysis.

### 8. Zenmap – Local Network Discovery

**Target Subnet:**

```text
192.168.1.0/24
```

**Scan Profile:** Ping Scan

**Nmap Command:**

```bash
nmap -sn 192.168.1.0/24
```

**Scan Results:**

| Metric | Result |
|---|---|
| Total IP Addresses Scanned | 256 |
| Live Hosts Discovered | 3 |
| Scan Duration | 3.07 seconds |
| Nmap Version | 7.99 |

**Discovered Hosts:**

| IP Address | MAC Address | Identification |
|---|---|---|
| 192.168.1.1 | 52:55:C0:A8:01:01 | Unknown |
| 192.168.1.3 | 08:00:27:E1:CE:C7 | Oracle VirtualBox Virtual NIC |
| 192.168.1.6 | Not available | Not identified |

**Objective:**
- Identify active devices within the local LAN.
- Collect available IP and MAC address information.
- Visualize discovered devices using Zenmap topology.

---

## 📊 Key Findings & Security Observations

The assessment produced the following preliminary security observations:

| # | Security Observation | Risk Level |
|---|---|---|
| 01 | Publicly available domain registration information | Low |
| 02 | Website technology information exposed | Medium |
| 03 | Publicly identifiable server IP | Low |
| 04 | HTTP technical information exposed | Low |
| 05 | WAF technology identifiable | Low |
| 06 | DNS infrastructure information exposed | Medium |
| 07 | Domain relationship information visible through OSINT | Low |
| 08 | Multiple active devices visible on local network | Medium |

**Note:** These are preliminary observations, not confirmed exploitable vulnerabilities. No exploitation or vulnerability validation was performed.

---

## 🛡️ Security Recommendations

1. Regularly review publicly exposed domain information.
2. Keep CMS platforms, plugins, and website components updated.
3. Review unnecessary server information exposed through HTTP headers.
4. Apply appropriate security configurations to HTTP response headers.
5. Maintain and monitor Web Application Firewall configurations.
6. Review DNS records and email infrastructure regularly.
7. Maintain an updated inventory of internal network devices.
8. Investigate unidentified devices discovered during network scanning.
9. Document network topology and asset information.
10. Conduct further authorized vulnerability assessments when required.

---

## 📁 Repository Structure

```text
W2-Footprinting-and-Network-Scanning/
│
├── README.md
│
├── report/
│   └── W2-PM-FINAL-Penetration-Testing-Report.pdf
│
├── evidence/
│   ├── 01-WHOIS/
│   ├── 02-WhatWeb/
│   ├── 03-DNS-Resolution/
│   ├── 04-HTTP-Headers/
│   ├── 05-WAF-Detection/
│   ├── 06-DNS-Enumeration/
│   ├── 07-Maltego/
│   └── 08-Zenmap/
│
├── commands/
│   └── reconnaissance-commands.md
│
└── .gitignore
```

---

## 📄 Detailed Project Report

The complete penetration testing report includes:

- Introduction and assessment scope.
- Tools and methodologies.
- Practical execution details.
- Actual observations and scan outputs.
- Preliminary risk analysis.
- Security recommendations.
- Screenshot-based evidence.

📥 **[View / Download Penetration Testing Report](report/W2-PM-FINAL-Penetration-Testing-Report.pdf)**

---

## ⚠️ Disclaimer

This repository documents educational cybersecurity activities performed as part of an internship practical assessment.

Website reconnaissance was conducted within the authorized assessment scope, and network scanning was performed against my own local LAN.

No exploitation, unauthorized access, or destructive testing was conducted.

All techniques and commands documented here must only be used on systems and networks for which appropriate authorization has been obtained.

The findings represent observations from the practical exercises and should not be interpreted as confirmed security vulnerabilities.

---

## 👨‍💻 Author

**Md Ektearul Haque Seajon**

Cybersecurity Intern | Networkwalks | Batch B084

🔗 **LinkedIn:** [Md Ektearul Haque Seajon](https://www.linkedin.com/in/ektearulhaque/)


---

## 📌 Internship Project Information

| Detail | Information |
|---|---|
| Program | Networkwalks Cybersecurity Program |
| Batch | B084 |
| Week | 02 |
| Project | Footprinting & Network Scanning |
| Modules | W2-PM1, W2-PM3, W2-PM5 |
| Documentation | Penetration Testing Report |

---

<p align="center">
  <b>Learning Through Practice. Building Skills Through Security. 🔐</b>
</p>
