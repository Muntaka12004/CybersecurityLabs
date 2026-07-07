Network Scanning Using NMAP(Network Mapper)
______________________________________________________________________________
Overview
This project demonstrates the fundamentals of network reconnaissance using Nmap one of the most widely used network scanning tools in cybersecurity. The lab focuses on discovering live hosts, identifying open ports, detecting running services, performing operating system detection, and conducting basic vulnerability mapping in a controlled virtual lab environment.
______________________________________________________________________________
Disclaimer
All scans in this project were performed in a personal lab environment using intentionally vulnerable machines (Metasploitable 2). This repository is for educational purposes only.
______________________________________________________________________________
Objectives
	Perform host discovery on a local network.
	Identify active hosts.
	Discover open TCP ports.
	Detect running services and their versions.
	Identify the target operating system.
	Perform basic vulnerability assessment using the Nmap Scripting Engine (NSE).
	Understand the role of network reconnaissance in penetration testing.
______________________________________________________________________________
Tools Used
	Kali Linux
	Nmap
	VMware Workstation
	Metasploitable
______________________________________________________________________________
Phase 1: Host Discovery
 
Command:- nmap -sn 192.168.0.186
Purpose :-This scan identifies active hosts on the network without performing a port scan.
Findings
•	Successfully discovered active hosts on the network.
•	Identified the IP addresses of the vulnerable machine used during the assessment.
______________________________________________________________________________
Phase 2: TCP SYN Scan
Command:- nmap -sS -T4 192.168.0.186
Purpose :-Performs a stealth SYN scan to identify open TCP ports while minimizing detection.
Findings
•	Identified multiple open TCP ports.
•	Confirmed accessible network services running on the target.
______________________________________________________________________________
Phase 3: Service Version Detection
Command:- nmap -sV 192.168.0.186
Purpose:- Detects services running on open ports and determines their version numbers.
 Findings
The scan identified services including:
•	FTP
•	SSH
•	SMB
•	HTTP
•	HTTPS
•	Telnet
•	Postgresql
Version detection helps identify outdated software that may contain known vulnerabilities.
______________________________________________________________________________
Phase 4: Operating System Detection
Command:- nmap -O 192.168.0.186
Purpose:- Attempts to identify the operating system of the target host.
Findings
Successfully estimated the operating system of the target based on TCP/IP fingerprinting.
______________________________________________________________________________

Phase 5: Vulnerability Scanning with NSE
Command:- nmap --script vuln 192.168.0.186
Purpose:- Uses the Nmap Scripting Engine (NSE) to identify known vulnerabilities and security misconfigurations.
Findings
The vulnerability scan identified several security issues including:
•	VSFTPD Backdoor
•	RMI-Vuln-Classloader
•	HTTP Slowloris Vulnerability
______________________________________________________________________________
Repository Structure
Network-Scanning-with-Nmap/
│
├── README.md
├── LICENSE
├── screenshots/
│ ├── host-discovery.png
│ ├── syn-scan.png
│ ├── service-version.png
│ ├── os-detection.png
│ └── vulnerability-scan.png
│
└── reports/
└── Network-Scanning-with-Nmap.pdf
______________________________________________________________________________
Author

Badamasi Muntaka Muhammad
Aspiring SOC analyst and cybersecurity student
Linkedln:- www.linkedin.com/in/muntaka-muhammad-aaab02374
Github:- https://github.com/Muntaka12004
______________________________________________________________________________





