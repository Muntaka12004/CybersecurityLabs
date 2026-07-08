# Network Scanning with Nmap

A hands-on cybersecurity project demonstrating network reconnaissance, service enumeration, operating system detection, and vulnerability assessment using **Nmap** against a **Metasploitable 2** virtual machine.

> **Disclaimer:** All scans were conducted in a personal lab environment using Metasploitable 2, an intentionally vulnerable virtual machine designed for cybersecurity training. This project is intended for educational purposes only.

---

# Objectives

- Perform host discovery on a local network.
- Identify active hosts.
- Discover open TCP ports.
- Detect running services and their versions.
- Identify the target operating system.
- Perform vulnerability assessment using the Nmap Scripting Engine (NSE).
- Understand the role of network reconnaissance in penetration testing.

---

# Tools Used

- Kali Linux
- Nmap
- VMware Workstation
- Metasploitable 2

---

# Phase 1 – Host Discovery

## Command

```bash
nmap -sn 192.168.0.117/24
```

## Purpose

Identify active hosts on the network without performing a port scan.


## Findings

- Successfully discovered the active host on the network.
- Confirmed the IP address of the Metasploitable 2 virtual machine before further enumeration.

---

# Phase 2 – TCP SYN Scan

## Command

```bash
nmap -sS -T4 192.168.0.186
```

## Purpose

Perform a TCP SYN (Stealth) scan to identify open TCP ports.


## Findings

- Identified multiple open TCP ports.
- Confirmed accessible network services running on the target.

---

# Phase 3 – Service Version Detection

## Command

```bash
nmap -sV 192.168.0.186
```

## Purpose

Detect running services and determine their version numbers.


## Findings

The scan detected services including:

- FTP
- SSH
- SMB
- HTTP
- HTTPS
- Telnet
- PostgreSQL

Service version detection helps identify outdated software that may contain known vulnerabilities.

---

# Phase 4 – Operating System Detection

## Command

```bash
nmap -O 192.168.0.186
```

## Purpose

Attempt to identify the operating system of the target.


## Findings

- Successfully estimated the operating system using TCP/IP fingerprinting.

---

# Phase 5 – Vulnerability Assessment

## Command

```bash
nmap --script vuln 192.168.0.186
```

## Purpose

Use the Nmap Scripting Engine (NSE) to identify known vulnerabilities and security misconfigurations.


## Findings

The scan identified vulnerabilities including:

- VSFTPD Backdoor
- RMI-Vuln-Classloader
- HTTP Slowloris Vulnerability

---

# Results Summary

The assessment successfully identified:

- Active hosts on the network
- Open TCP ports
- Running network services
- Service versions
- Operating system information
- Potential security vulnerabilities

This project demonstrates how Nmap can be used during the reconnaissance and enumeration phases of a penetration test.

---

# Skills Demonstrated

- Network Reconnaissance
- Host Discovery
- TCP SYN Scanning
- Port Scanning
- Service Enumeration
- Operating System Fingerprinting
- Vulnerability Assessment
- Nmap Scripting Engine (NSE)
- Basic Security Analysis

---

# Lessons Learned

This project enhanced my understanding of:

- Network reconnaissance techniques
- Port scanning methodologies
- Service enumeration
- Operating system fingerprinting
- Vulnerability assessment using NSE scripts
- Ethical considerations when performing security assessments
- The importance of minimizing unnecessary network exposure

---
# Documentation

A detailed report containing the complete methodology, scan outputs, screenshots, and findings is available in the `reports` directory.

- **Report:** `reports/Network-Scanning-with-Nmap.pdf`
# Repository Structure

```text
Network-Scanning-with-Nmap/
│
├── README.md
├── LICENSE
├── screenshots/
│   ├── host-discovery.png
│   ├── syn-scan.png
│   ├── service-version.png
│   ├── os-detection.png
│   └── vulnerability-scan.png
│
└── reports/
    └── Network-Scanning-with-Nmap.pdf
```

---

# Author

**Badamasi Muntaka Muhammad**

Aspiring SOC Analyst and Cybersecurity Student

- **GitHub:** https://github.com/Muntaka12004
- **LinkedIn:** https://www.linkedin.com/in/muntaka-muhammad-aaab02374
