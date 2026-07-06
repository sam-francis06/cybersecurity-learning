<div align="center">

[<img src="https://cdn.simpleicons.org/tryhackme/DC2626" width="80" alt="TryHackMe Logo" />](https://tryhackme.com)

# TryHackMe Knowledge Base

### A Structured Record of Hands-On Cybersecurity Training and Practical Learning

[![Platform](https://img.shields.io/badge/Platform-TryHackMe-DC2626?style=for-the-badge\&logo=tryhackme\&logoColor=white)](https://tryhackme.com)
[![Total Rooms](https://img.shields.io/badge/Total%20Rooms%20Completed-76-16A34A?style=for-the-badge\&logo=checkmarx\&logoColor=white)]()
[![Challenge Rooms](https://img.shields.io/badge/Challenge%20Rooms-26-EA580C?style=for-the-badge\&logo=target\&logoColor=white)]()
[![Focus](https://img.shields.io/badge/Focus-Offensive%20%26%20Defensive%20Security-2563EB?style=for-the-badge\&logo=hackaday\&logoColor=white)]()
[![Updated](https://img.shields.io/badge/Last%20Updated-July%202026-6B7280?style=for-the-badge\&logo=clockify\&logoColor=white)]()

</div>

---

## 📘 About This Knowledge Base

This knowledge base documents my hands-on cybersecurity learning and practical experience gained through completing **76 TryHackMe rooms**, including **26 Challenge Rooms**.

Rather than maintaining an exhaustive room-by-room record of every completed activity, this document organizes the most important knowledge, techniques, tools, commands, methodologies, and lessons learned into core cybersecurity domains.

The knowledge base currently covers:

* Web Security
* Linux
* Networking
* Offensive Security
* Defensive Security
* Digital Forensics
* Open Source Intelligence (OSINT)

The rooms listed within each section represent selected rooms that contributed significantly to my understanding of that domain. They are **not intended to represent all 76 completed TryHackMe rooms**.

Some rooms may contribute knowledge to multiple cybersecurity domains. For example, a single challenge may involve web exploitation, Linux enumeration, networking, privilege escalation, and digital forensics. Therefore, domain-specific room lists should be interpreted as learning references rather than a cumulative progress total.

### 🎯 Objectives

1. Maintain a structured reference of cybersecurity concepts and methodologies learned through practical training.
2. Document useful commands and tools for future labs, CTF competitions, and authorized security assessments.
3. Track the development of practical skills across offensive and defensive security domains.
4. Reinforce knowledge by converting hands-on experience into organized technical documentation.
5. Demonstrate continuous and structured cybersecurity learning.

> **Progress Note:** As of July 2026, I have completed **76 TryHackMe rooms**, including **26 Challenge Rooms**. This knowledge base contains selected and categorized learning records rather than an exhaustive list of every completed room.

---

## 📑 Table of Contents

| # | Domain                                                 | Description                                              |
| - | ------------------------------------------------------ | -------------------------------------------------------- |
| 1 | [🌐 Web Security](#-1-web-security)                    | Web application vulnerabilities and testing methodology  |
| 2 | [🐧 Linux](#-2-linux)                                  | Linux fundamentals and command-line proficiency          |
| 3 | [🌐 Networking](#-3-networking)                        | Core networking protocols and enumeration                |
| 4 | [⚔️ Offensive Security](#️-4-offensive-security)       | Red team tooling and exploitation methodology            |
| 5 | [🛡️ Defensive Security](#️-5-defensive-security)      | Blue team monitoring, SOC operations, and threat hunting |
| 6 | [🔬 Digital Forensics](#-6-digital-forensics)          | Evidence collection and incident investigation           |
| 7 | [🔎 OSINT](#-7-open-source-intelligence-osint)         | Open-source reconnaissance and intelligence gathering    |
| 8 | [⚠️ Ethical Use Disclaimer](#️-ethical-use-disclaimer) | Scope and responsible-use statement                      |

---

# 🌐 1. Web Security

<img src="https://img.shields.io/badge/Domain-Application%20Security-DC2626?style=flat-square" />

Web security focuses on identifying and understanding vulnerabilities that arise in the design, implementation, and deployment of web applications.

This domain forms an important foundation for modern penetration testing because many internet-facing attack surfaces are web applications and APIs.

### 📋 Selected Completed Rooms

| Room                       | Focus Area                                     |
| -------------------------- | ---------------------------------------------- |
| Web Application Basics     | Core HTTP request and response concepts        |
| Web Application Security   | Introductory web vulnerability classes         |
| Web Security Essentials    | Foundational web security principles           |
| Guided Pentesting          | End-to-end guided assessment methodology       |
| HTTP in Detail             | Headers, methods, cookies, and status codes    |
| Content Discovery          | Hidden endpoint and directory enumeration      |
| SQL Injection Introduction | Database-layer injection vulnerabilities       |
| Vulnerabilities 101        | Common application vulnerability classes       |
| Basic Pentesting           | Applied enumeration and exploitation           |
| Pickle Rick                | CTF-style web exploitation                     |
| Glitch                     | Web application investigation and exploitation |
| Dev Diaries                | CTF-style web exploitation                     |
| U.A. High School           | Enumeration and exploitation                   |
| Merry XSSMas               | Cross-Site Scripting exploitation              |
| Santa's Little IDOR        | Insecure Direct Object Reference exploitation  |

### 🎯 Core Concepts

| Concept                                     | Description                                                                                                  |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| **HTTP & HTTPS**                            | Protocols used for communication between clients and web servers. HTTPS uses TLS to protect data in transit. |
| **Cookies & Sessions**                      | Mechanisms used to maintain application state and authenticated user sessions.                               |
| **Authentication vs. Authorization**        | Authentication verifies identity, while authorization determines permitted actions and resources.            |
| **Content Discovery**                       | Enumerating hidden files, directories, endpoints, and application resources.                                 |
| **SQL Injection (SQLi)**                    | Manipulating database queries through improperly handled user input.                                         |
| **Cross-Site Scripting (XSS)**              | Injecting client-side scripts into web pages viewed by other users.                                          |
| **Insecure Direct Object Reference (IDOR)** | Accessing resources without sufficient authorization validation.                                             |
| **Security Misconfiguration**               | Vulnerabilities caused by insecure defaults, exposed services, or improper application configurations.       |

### 🛠️ Tools Used

<p>
<img src="https://img.shields.io/badge/Burp%20Suite-FF6633?style=flat-square&logo=burpsuite&logoColor=white" />
<img src="https://img.shields.io/badge/Gobuster-1F2937?style=flat-square" />
<img src="https://img.shields.io/badge/ffuf-374151?style=flat-square" />
<img src="https://img.shields.io/badge/curl-073551?style=flat-square&logo=curl&logoColor=white" />
<img src="https://img.shields.io/badge/wget-4A4A4A?style=flat-square&logo=gnu&logoColor=white" />
<img src="https://img.shields.io/badge/Browser%20DevTools-4285F4?style=flat-square&logo=googlechrome&logoColor=white" />
</p>

### 💻 Command Reference

**Directory and Content Discovery**

```bash
gobuster dir -u <URL> -w <WORDLIST>
ffuf -u http://target/FUZZ -w wordlist.txt
```

**HTTP Reconnaissance**

```bash
curl -I <URL>
curl -v <URL>
wget --mirror <URL>
```

**Local Search and Flag Hunting**

```bash
grep -R "flag" .
find . -type f
```

### 📖 Key Takeaways

* Understand HTTP communication before attempting web exploitation.
* Thoroughly enumerate applications before testing vulnerabilities.
* Map the complete attack surface before attempting exploitation.
* Authentication and authorization vulnerabilities require different testing approaches.
* Web exploitation requires combining technical knowledge with structured investigation.

---

# 🐧 2. Linux

<img src="https://img.shields.io/badge/Domain-Operating%20Systems-16A34A?style=flat-square" />

Linux knowledge is fundamental to cybersecurity because many servers, security tools, CTF environments, and penetration testing distributions operate on Linux-based systems.

### 📋 Selected Completed Rooms

* Linux Fundamentals Part 1
* Linux CLI

### 🎯 Core Concepts

| Concept                  | Description                                                                      |
| ------------------------ | -------------------------------------------------------------------------------- |
| **Filesystem Hierarchy** | Standard Linux directory structures such as `/etc`, `/var`, `/home`, and `/tmp`. |
| **Shell Navigation**     | Navigating filesystems and executing commands through shells such as Bash.       |
| **File Management**      | Creating, copying, moving, modifying, and deleting files and directories.        |
| **File Permissions**     | Managing read, write, and execute permissions for users and groups.              |
| **User Management**      | Understanding accounts, groups, privileges, and access controls.                 |
| **Process Management**   | Monitoring and controlling running system processes.                             |
| **Package Management**   | Installing, updating, and managing system software.                              |
| **Text Processing**      | Searching, filtering, and transforming data from files and command output.       |

### 🛠️ Command Reference

<details>
<summary><b>Navigation</b></summary>

```bash
pwd
ls -la
cd
tree
```

</details>

<details>
<summary><b>File Management</b></summary>

```bash
touch
mkdir
cp
mv
rm
rmdir
cat
less
head
tail
```

</details>

<details>
<summary><b>File Searching</b></summary>

```bash
find
locate
which
whereis
```

</details>

<details>
<summary><b>Text Processing</b></summary>

```bash
grep
sort
uniq
wc
cut
awk
sed
```

</details>

<details>
<summary><b>Permissions</b></summary>

```bash
chmod
chown
chgrp
umask
```

</details>

<details>
<summary><b>Process Management</b></summary>

```bash
ps
top
htop
kill
killall
jobs
```

</details>

<details>
<summary><b>Networking</b></summary>

```bash
ip a
ping
netstat
ss
curl
wget
```

</details>

<details>
<summary><b>Archives</b></summary>

```bash
tar
gzip
gunzip
zip
unzip
```

</details>

### 📖 Key Takeaways

* Linux command-line proficiency improves efficiency during security assessments.
* File permissions are fundamental to system security and privilege escalation.
* Text-processing tools are valuable for log analysis and data extraction.
* Understanding processes and services helps identify suspicious activity.
* Linux networking utilities are essential for troubleshooting and reconnaissance.

---

# 🌐 3. Networking

<img src="https://img.shields.io/badge/Domain-Network%20Security-2563EB?style=flat-square" />

Networking knowledge supports almost every cybersecurity discipline, including reconnaissance, exploitation, monitoring, incident response, and digital forensics.

### 📋 Selected Completed Rooms

* What is Networking?
* Network Discovery

### 🎯 Core Concepts

| Concept               | Description                                                    |
| --------------------- | -------------------------------------------------------------- |
| **OSI Model**         | Seven-layer conceptual model describing network communication. |
| **TCP/IP Model**      | Practical networking model used for internet communication.    |
| **IP Addressing**     | Logical addressing using IPv4 and IPv6.                        |
| **MAC Addresses**     | Hardware-level addresses used for local network communication. |
| **DNS**               | Resolves domain names into IP addresses.                       |
| **Common Protocols**  | HTTP, HTTPS, FTP, SSH, DNS, SMTP, and other network protocols. |
| **Port Scanning**     | Identifying open ports and exposed network services.           |
| **Network Discovery** | Identifying live hosts and understanding network topology.     |

### 🛠️ Tools Used

<p>
<img src="https://img.shields.io/badge/Nmap-1F2937?style=flat-square" />
<img src="https://img.shields.io/badge/Netcat-374151?style=flat-square" />
<img src="https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white" />
<img src="https://img.shields.io/badge/curl-073551?style=flat-square&logo=curl&logoColor=white" />
<img src="https://img.shields.io/badge/wget-4A4A4A?style=flat-square&logo=gnu&logoColor=white" />
</p>

### 💻 Command Reference

**Host Discovery**

```bash
ping <target>
arp -a
ip a
```

**DNS Enumeration**

```bash
nslookup <domain>
dig <domain>
host <domain>
```

**Network Information**

```bash
ip addr
ip route
hostname
```

**Port Scanning**

```bash
nmap <target>
nmap -sV <target>
nmap -A <target>
nmap -Pn <target>
```

**Connectivity Testing**

```bash
telnet <host> <port>
nc -lvnp 4444
curl <URL>
wget <URL>
```

### 🔑 Common Ports Reference

| Port  | Protocol | Service |
| ----- | -------- | ------- |
| 20/21 | TCP      | FTP     |
| 22    | TCP      | SSH     |
| 23    | TCP      | Telnet  |
| 25    | TCP      | SMTP    |
| 53    | TCP/UDP  | DNS     |
| 80    | TCP      | HTTP    |
| 110   | TCP      | POP3    |
| 143   | TCP      | IMAP    |
| 443   | TCP      | HTTPS   |
| 445   | TCP      | SMB     |
| 3389  | TCP      | RDP     |

### 📖 Key Takeaways

* Networking forms a technical foundation for cybersecurity.
* Understanding protocols helps identify potential attack surfaces.
* Enumeration should occur before exploitation.
* DNS can reveal valuable information about target infrastructure.
* Port scanning identifies exposed services and potential entry points.

---

# ⚔️ 4. Offensive Security

<img src="https://img.shields.io/badge/Domain-Offensive%20Security-DC2626?style=flat-square" />

Offensive security involves identifying and exploiting security weaknesses within authorized environments to understand attack techniques and improve system security.

### 📋 Selected Completed Rooms

* Offensive Security Intro
* Hydra
* CyberChef: The Basics
* Search Skills
* Exploitation with cURL

### 🎯 Core Concepts

| Concept                          | Description                                                                              |
| -------------------------------- | ---------------------------------------------------------------------------------------- |
| **Ethical Hacking Fundamentals** | Understanding authorization, scope, and responsible security testing.                    |
| **Information Gathering**        | Collecting information about targets before active testing.                              |
| **Enumeration**                  | Actively identifying services, users, endpoints, and configurations.                     |
| **Password Attacks**             | Testing authentication security using authorized password attack techniques.             |
| **HTTP Request Crafting**        | Modifying requests to investigate application behavior.                                  |
| **CTF Methodology**              | Applying systematic reconnaissance, enumeration, exploitation, and escalation workflows. |

### 🛠️ Tools Used

<p>
<img src="https://img.shields.io/badge/Hydra-1F2937?style=flat-square" />
<img src="https://img.shields.io/badge/CyberChef-1E90FF?style=flat-square" />
<img src="https://img.shields.io/badge/curl-073551?style=flat-square&logo=curl&logoColor=white" />
<img src="https://img.shields.io/badge/Burp%20Suite-FF6633?style=flat-square&logo=burpsuite&logoColor=white" />
<img src="https://img.shields.io/badge/Nmap-1F2937?style=flat-square" />
<img src="https://img.shields.io/badge/Gobuster-374151?style=flat-square" />
<img src="https://img.shields.io/badge/ffuf-4B5563?style=flat-square" />
<img src="https://img.shields.io/badge/Netcat-6B7280?style=flat-square" />
<img src="https://img.shields.io/badge/Kali%20Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white" />
</p>

### 💻 Command Reference

**Hydra**

```bash
hydra -l admin -P rockyou.txt ssh://<target>
hydra -L users.txt -P passwords.txt ftp://<target>
hydra -l admin -P passwords.txt http-post-form "/login:user=^USER^&pass=^PASS^:Invalid"
```

**cURL**

```bash
curl http://example.com
curl -I http://example.com
curl -X POST http://example.com/login
curl -H "Authorization: Bearer <TOKEN>" http://example.com/api
```

**Enumeration**

```bash
nmap -A <target>
gobuster dir -u http://<target> -w wordlist.txt
ffuf -u http://target/FUZZ -w wordlist.txt
```

### 📖 Key Takeaways

* Enumeration is one of the most important phases of offensive security.
* Understand the target before attempting exploitation.
* Security testing must remain within authorized environments.
* HTTP requests can be inspected and modified to investigate application behavior.
* Information discovered during reconnaissance often contributes to successful exploitation.

---

# 🛡️ 5. Defensive Security

<img src="https://img.shields.io/badge/Domain-Defensive%20Security-2563EB?style=flat-square" />

Defensive security focuses on detecting, investigating, responding to, and preventing cyber threats.

### 📋 Selected Completed Rooms

* Defensive Security Intro
* Junior Security Analyst Intro
* Threat Hunting: Introduction
* Splunk Basics
* Preparation
* Intro to Digital Forensics
* Registry Forensics
* Malware Analysis
* Web Attack Forensics
* YARA Rules

### 🎯 Core Concepts

| Concept                              | Description                                                                   |
| ------------------------------------ | ----------------------------------------------------------------------------- |
| **Security Operations Center (SOC)** | Centralized security monitoring and incident response operations.             |
| **Threat Hunting**                   | Proactively searching systems and networks for undetected threats.            |
| **Incident Response**                | Detecting, containing, eradicating, and recovering from security incidents.   |
| **SIEM Fundamentals**                | Centralizing and analyzing security logs from multiple sources.               |
| **Malware Analysis**                 | Investigating suspicious files and software behavior.                         |
| **Windows Registry Analysis**        | Examining Registry artifacts for evidence of activity.                        |
| **YARA Rules**                       | Creating pattern-matching rules for identifying suspicious files and malware. |

### 🛠️ Tools Used

<p>
<img src="https://img.shields.io/badge/Splunk-000000?style=flat-square&logo=splunk&logoColor=white" />
<img src="https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white" />
<img src="https://img.shields.io/badge/YARA-4B5563?style=flat-square" />
<img src="https://img.shields.io/badge/Windows%20Event%20Viewer-0078D4?style=flat-square&logo=windows&logoColor=white" />
<img src="https://img.shields.io/badge/Sysinternals-0078D4?style=flat-square&logo=windows&logoColor=white" />
<img src="https://img.shields.io/badge/CyberChef-1E90FF?style=flat-square" />
<img src="https://img.shields.io/badge/VirusTotal-394EFF?style=flat-square" />
</p>

### 💻 Command Reference

**Windows Event Logs**

```powershell
Get-WinEvent -LogName Security
Get-EventLog -LogName System
```

**Linux Log Analysis**

```bash
cat /var/log/auth.log
tail -f /var/log/syslog
grep "Failed" /var/log/auth.log
journalctl
```

**YARA**

```bash
yara rule.yar sample.exe
yara -r rules/ samples/
```

**Network Analysis**

```bash
tcpdump -i eth0
netstat -tulnp
ss -tuln
```

### 📖 Key Takeaways

* Defensive security focuses on detecting, investigating, and responding to threats.
* Log analysis is essential for identifying malicious activity.
* Threat hunting requires understanding attacker behavior and indicators of compromise.
* SIEM platforms improve security visibility by centralizing logs.
* Digital forensics helps reconstruct incidents and determine their impact.

---

# 🔬 6. Digital Forensics

<img src="https://img.shields.io/badge/Domain-Digital%20Forensics-7C3AED?style=flat-square" />

Digital forensics focuses on identifying, preserving, examining, analyzing, and reporting digital evidence.

### 📋 Selected Completed Rooms

* Intro to Digital Forensics
* Registry Forensics
* Web Attack Forensics

### 🎯 Core Concepts

| Concept                             | Description                                                                  |
| ----------------------------------- | ---------------------------------------------------------------------------- |
| **Chain of Custody**                | Documenting how evidence was collected, transferred, handled, and preserved. |
| **Windows Registry Analysis**       | Investigating Registry artifacts for evidence of system and user activity.   |
| **Browser Forensics**               | Examining browser history, cookies, cache, and related artifacts.            |
| **Timeline Analysis**               | Correlating timestamps to reconstruct incident activity.                     |
| **Indicators of Compromise (IOCs)** | Observable evidence that may indicate malicious activity.                    |
| **Evidence Preservation**           | Protecting evidence integrity throughout an investigation.                   |

### 🛠️ Tools Used

<p>
<img src="https://img.shields.io/badge/Autopsy-2563EB?style=flat-square" />
<img src="https://img.shields.io/badge/FTK%20Imager-6B7280?style=flat-square" />
<img src="https://img.shields.io/badge/Registry%20Explorer-0078D4?style=flat-square&logo=windows&logoColor=white" />
<img src="https://img.shields.io/badge/CyberChef-1E90FF?style=flat-square" />
<img src="https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white" />
<img src="https://img.shields.io/badge/Volatility-4B5563?style=flat-square" />
</p>

### 💻 Command Reference

**Log Analysis**

```bash
cat /var/log/auth.log
tail -f /var/log/syslog
grep "Failed" /var/log/auth.log
journalctl
```

**File Integrity Verification**

```bash
sha256sum file
md5sum file
file filename
```

**Windows Event Logs**

```powershell
Get-WinEvent -LogName Security
Get-EventLog -LogName System
```

**Network Investigation**

```bash
tcpdump -i eth0
netstat -tulnp
ss -tuln
```

### 📖 Key Takeaways

* Evidence integrity must be maintained throughout investigations.
* Cryptographic hashes help verify that evidence has not been modified.
* Windows Registry artifacts provide information about system and user activity.
* Log analysis helps reconstruct attack timelines.
* Browser artifacts may provide valuable evidence during investigations.

---

# 🔎 7. Open Source Intelligence (OSINT)

<img src="https://img.shields.io/badge/Domain-Open%20Source%20Intelligence-EAB308?style=flat-square" />

OSINT involves collecting and analyzing publicly available information to support reconnaissance, cybersecurity assessments, and investigations.

### 📋 Selected Completed Rooms

* Missing Person
* Digital Footprint
* Water Bottle

### 🎯 Core Concepts

| Concept                      | Description                                                                     |
| ---------------------------- | ------------------------------------------------------------------------------- |
| **Information Gathering**    | Collecting publicly available information relevant to an investigation.         |
| **Search Engine Techniques** | Using advanced search operators to locate specific information.                 |
| **Digital Footprinting**     | Identifying information left by individuals and organizations online.           |
| **Username Enumeration**     | Investigating usernames across multiple online platforms.                       |
| **Domain Intelligence**      | Gathering registration, hosting, DNS, and infrastructure information.           |
| **Metadata Analysis**        | Extracting information embedded within digital files.                           |
| **Geolocation**              | Determining physical locations using images and publicly available information. |

### 🛠️ Tools Used

<p>
<img src="https://img.shields.io/badge/Google%20Search-4285F4?style=flat-square&logo=google&logoColor=white" />
<img src="https://img.shields.io/badge/WHOIS-6B7280?style=flat-square" />
<img src="https://img.shields.io/badge/theHarvester-374151?style=flat-square" />
<img src="https://img.shields.io/badge/Sherlock-1F2937?style=flat-square" />
<img src="https://img.shields.io/badge/Shodan-DC2626?style=flat-square" />
<img src="https://img.shields.io/badge/VirusTotal-394EFF?style=flat-square" />
<img src="https://img.shields.io/badge/Have%20I%20Been%20Pwned-2563EB?style=flat-square" />
<img src="https://img.shields.io/badge/Wayback%20Machine-000000?style=flat-square&logo=internetarchive&logoColor=white" />
</p>

### 💻 Command Reference

**DNS and Domain Enumeration**

```bash
whois example.com
nslookup example.com
dig example.com
```

**Network Information**

```bash
ping example.com
traceroute example.com
```

**Email and Domain Intelligence**

```bash
theHarvester -d example.com -b all
```

**Username Enumeration**

```bash
sherlock username
```

**Metadata Analysis**

```bash
exiftool image.jpg
```

### 📖 Key Takeaways

* OSINT relies on publicly available information.
* Effective reconnaissance helps build an understanding of a target.
* Advanced search techniques improve information discovery.
* Metadata may reveal information not immediately visible within files.
* Digital footprints can unintentionally expose sensitive information.
* Information should be verified using multiple reliable sources.

---

# 📈 Learning Progress

| Metric                          |              Progress |
| ------------------------------- | --------------------: |
| Total TryHackMe Rooms Completed |                **76** |
| Challenge Rooms Completed       |                **26** |
| Easy Challenge Rooms            |                **25** |
| Medium Challenge Rooms          |                 **1** |
| Hard Challenge Rooms            |                 **0** |
| Primary Learning Approach       | **Hands-On Practice** |
| Documentation Status            |           **Ongoing** |

> The statistics above represent overall TryHackMe progress. The room lists within individual knowledge domains contain selected learning records and should not be added together to calculate total progress.

---

# 🎯 Current Learning Focus

My current cybersecurity learning focuses on strengthening practical problem-solving capabilities through:

* Web application security
* Browser and JavaScript security
* Network reconnaissance and enumeration
* Linux command-line proficiency
* Offensive security methodology
* CTF challenge solving
* Digital forensics and investigation
* Defensive security fundamentals

The primary objective is to progress from guided cybersecurity training toward increasingly independent challenge solving and practical security analysis.

---

# 📖 Overall Key Takeaways

* Strong cybersecurity skills require consistent hands-on practice.
* Enumeration and information gathering are fundamental across multiple security disciplines.
* Understanding underlying technologies is more valuable than memorizing tools.
* Offensive and defensive security knowledge complement each other.
* CTF challenges improve analytical thinking and independent problem-solving.
* Technical documentation reinforces learning and creates a reusable knowledge base.
* Progress should be measured not only by completed rooms but also by increasing independence and technical capability.

---

# ⚠️ Ethical Use Disclaimer

All techniques, tools, commands, and methodologies documented in this knowledge base were practiced exclusively within authorized environments such as TryHackMe, Capture The Flag competitions, and personal cybersecurity labs.

This material is intended solely for cybersecurity education, authorized security testing, responsible research, and professional skill development.

Using cybersecurity techniques against systems, networks, applications, or infrastructure without explicit authorization may be unethical and illegal under applicable computer misuse and cybersecurity laws.

> *"Progress in cybersecurity is not measured only by the number of challenges completed, but by the ability to investigate unfamiliar problems, apply the right methodology, and continuously learn from every assessment."*

<div align="center">

---

### TryHackMe Progress

**76 Total Rooms Completed | 26 Challenge Rooms Completed**

**25 Easy | 1 Medium | 0 Hard**

**Last updated: July 2026**

</div>
