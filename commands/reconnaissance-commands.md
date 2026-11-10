# 🔍 Reconnaissance & Footprinting Commands

## Project Information

| Detail | Information |
|---|---|
| Project | Footprinting & Network Scanning |
| Organization | Networkwalks |
| Internship Batch | B084 |
| Week | 02 |
| Environment | Kali Linux |
| Target Domain | networkwalks.com |
| Documentation Type | Practical Command Reference |

---

## 1. WHOIS – Domain Information Gathering

**Command:**

```bash
whois networkwalks.com
```

**Purpose:**

To retrieve publicly available domain registration information, including registrar details, registration dates, name servers, and domain status.

**Observed Information:**

- Registrar: GoDaddy.com, LLC
- Domain Creation Date: 06 November 2019
- Domain Expiration Date: 06 November 2027
- Name Servers: NS6135.HOSTGATOR.COM and NS6136.HOSTGATOR.COM
- Registrant Privacy Provider: Domains By Proxy, LLC

---

## 2. WhatWeb – Website Technology Fingerprinting

**Command:**

```bash
whatweb networkwalks.com
```

**Purpose:**

To identify publicly detectable web technologies, server information, CMS platforms, and related components.

**Observed Information:**

- Web Server: Apache
- CMS: WordPress
- Detected WordPress Version: 7.1.4
- Detected Plugin: WP Download Manager 3.3.76
- JavaScript Library: jQuery 3.7.1
- Resolved IP: 192.232.216.135
- HTTP Status: 200 OK

---

## 3. Nslookup – DNS Resolution

**Command:**

```bash
nslookup networkwalks.com
```

**Purpose:**

To resolve a domain name into its corresponding IP address using a DNS server.

**Observed Information:**

- DNS Server: 8.8.8.8
- DNS Server Address: 8.8.8.8#53
- Resolved Domain: networkwalks.com
- Resolved IP Address: 192.232.216.135
- Response: Non-authoritative Answer

---

## 4. Curl – HTTP Response Header Analysis

**Command:**

```bash
curl -I https://networkwalks.com
```

**Purpose:**

To retrieve and inspect HTTP response headers from the target website.

**Observed Information:**

- HTTP Protocol: HTTP/2
- Response Status: 200
- Server: Apache
- Content-Type: text/html; charset=UTF-8
- WordPress REST API Link: /wp-json/
- Additional response headers were identified and documented.

---

## 5. Wafw00f – Web Application Firewall Detection

**Command:**

```bash
wafw00f networkwalks.com
```

**Purpose:**

To identify whether the target website is protected by a Web Application Firewall.

**Observed Information:**

- Tool: Wafw00f
- Version: 2.4.2
- WAF Detection: Positive
- Identified WAF: ModSecurity (SpiderLabs)
- Number of Requests: 2

---

## 6. DNSRecon – DNS Enumeration

**Command:**

```bash
dnsrecon -d networkwalks.com
```

**Purpose:**

To enumerate publicly available DNS records and identify domain-related infrastructure information.

**Observed Information:**

- SOA Records
- NS Records
- A Records
- MX Records
- TXT Records
- SRV Records
- Total Records Found: 8

---

## 7. Maltego – OSINT Relationship Mapping

**Application:** Maltego Desktop 4.11.3

**Activity:**

Domain relationship analysis and OSINT visualization.

**Purpose:**

To visualize relationships between domain-related entities and publicly available registration information.

**Observed Entities:**

- networkwalks.com
- GoDaddy.com, LLC
- VeriSign
- WHOIS
- RDAP Service
- Related contact entities

**Result:**

A visual relationship graph was generated to demonstrate connections between the domain and related entities.

---

## 8. Nmap / Zenmap – Local Network Discovery

**Target Subnet:**

```text
192.168.1.0/24
```

**Command:**

```bash
nmap -sn 192.168.1.0/24
```

**Scan Profile:** Ping Scan

**Purpose:**

To discover active hosts within the local network without performing a port scan.

**Observed Results:**

| Metric | Result |
|---|---|
| Total IP Addresses Scanned | 256 |
| Live Hosts | 3 |
| Scan Duration | 3.07 seconds |
| Nmap Version | 7.99 |

**Discovered Hosts:**

| IP Address | MAC Address | Identification |
|---|---|---|
| 192.168.1.1 | 52:55:C0:A8:01:01 | Unknown |
| 192.168.1.3 | 08:00:27:E1:CE:C7 | Oracle VirtualBox Virtual NIC |
| 192.168.1.6 | Not available | Not identified |

**Result:**

Three active hosts were discovered within the scanned local subnet. The results were visualized using Zenmap.

---

## Summary

The practical exercises covered the following reconnaissance and network discovery activities:

1. Domain registration information gathering.
2. Website technology fingerprinting.
3. DNS resolution.
4. HTTP response header inspection.
5. Web Application Firewall detection.
6. DNS record enumeration.
7. OSINT relationship visualization.
8. Local network host discovery.

These exercises provided practical exposure to commonly used cybersecurity reconnaissance tools and techniques.

---

## Disclaimer

This documentation is intended for educational and authorized cybersecurity assessment purposes only.

Website reconnaissance must only be performed within an approved assessment scope. Network scanning documented in this project was conducted against the author's local network.

No exploitation or unauthorized access was performed.
