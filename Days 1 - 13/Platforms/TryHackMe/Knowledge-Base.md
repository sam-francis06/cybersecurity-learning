<div align="center">

[<img src="https://cdn.simpleicons.org/tryhackme/DC2626" width="80" alt="TryHackMe Logo" />](https://tryhackme.com)

### A Structured Record of Hands-On Cybersecurity Training

[![Platform](https://img.shields.io/badge/Platform-TryHackMe-DC2626?style=for-the-badge&logo=tryhackme&logoColor=white)](https://tryhackme.com)
[![Rooms](https://img.shields.io/badge/Rooms%20Completed-33-16A34A?style=for-the-badge&logo=checkmarx&logoColor=white)]()
[![Focus](https://img.shields.io/badge/Focus-Offensive%20%26%20Defensive%20Security-2563EB?style=for-the-badge&logo=hackaday&logoColor=white)]()
[![Updated](https://img.shields.io/badge/Last%20Updated-July%202026-6B7280?style=for-the-badge&logo=clockify&logoColor=white)]()

</div>

---

## 📘 About This Repository

This repository is a personal knowledge base documenting my progression through **TryHackMe**, covering both **offensive** (red team) and **defensive** (blue team) disciplines. Each section below reflects a distinct domain of cybersecurity practice, including the rooms completed, the underlying concepts, the tools used in practice, real command syntax, and the core lessons taken away from each domain.

The goal of this document is twofold:
1. To serve as a **quick reference** for commands and concepts during future assessments, labs, or CTFs.
2. To demonstrate a **structured, evidence-based learning path** across the core pillars of cybersecurity.

---

## 📑 Table of Contents

| # | Domain | Description |
|---|---|---|
| 1 | [🌐 Web Security](#-1-web-security) | Web application vulnerabilities and testing methodology |
| 2 | [🐧 Linux](#-2-linux) | Linux fundamentals and command-line proficiency |
| 3 | [🌐 Networking](#-3-networking) | Core networking protocols and enumeration |
| 4 | [⚔️ Offensive Security](#️-4-offensive-security) | Red team tooling and exploitation basics |
| 5 | [🛡️ Defensive Security](#️-5-defensive-security) | Blue team monitoring, SOC, and threat hunting |
| 6 | [🔬 Digital Forensics](#-6-digital-forensics) | Evidence collection and incident investigation |
| 7 | [🔎 OSINT](#-7-open-source-intelligence-osint) | Open-source reconnaissance techniques |
| 8 | [⚠️ Ethical Use Disclaimer](#️-ethical-use-disclaimer) | Scope and responsible-use statement |

---

## 🌐 1. Web Security

<img src="https://img.shields.io/badge/Domain-Application%20Layer-DC2626?style=flat-square" />
<img src="https://img.shields.io/badge/Rooms-15-16A34A?style=flat-square" />

Web security focuses on identifying and understanding vulnerabilities that arise in the design, implementation, and deployment of web applications. This domain forms the practical foundation for most modern penetration testing engagements, since the majority of internet-facing attack surfaces are web-based.

### 📋 Completed Rooms

| # | Room | Focus Area |
|---|---|---|
| 1 | Web Application Basics | Core HTTP request/response concepts |
| 2 | Web Application Security | Introductory vulnerability classes |
| 3 | Web Security Essentials | Foundational secure-by-design principles |
| 4 | Guided Pentesting | End-to-end guided assessment methodology |
| 5 | HTTP in Detail | Headers, methods, status codes |
| 6 | Content Discovery | Hidden endpoint and directory enumeration |
| 7 | SQL Injection Introduction | Database-layer injection attacks |
| 8 | Vulnerabilities 101 | Common web vulnerability classes |
| 9 | Basic Pentesting | Applied enumeration and exploitation |
| 10 | Pickle Rick | CTF-style web exploitation |
| 11 | Glitch | CTF-style web exploitation |
| 12 | Dev Diaries | CTF-style web exploitation |
| 13 | U.A. High School | CTF-style web exploitation |
| 14 | Merry XSSMas | Cross-Site Scripting exploitation |
| 15 | Santa's Little IDOR | Insecure Direct Object Reference exploitation |

### 🎯 Core Concepts

| Concept | Description |
|---|---|
| **HTTP & HTTPS** | The request/response protocol underpinning the web; HTTPS adds a TLS encryption layer to protect data in transit. |
| **Cookies & Sessions** | Mechanisms used to maintain state across otherwise stateless HTTP requests, often the target of session-hijacking attacks. |
| **Authentication vs. Authorization** | Authentication verifies *who* a user is; authorization determines *what* that user is allowed to do. Confusing the two is a common source of vulnerabilities. |
| **Content Discovery** | The process of enumerating hidden files, directories, and endpoints not linked from the visible UI, often using wordlists. |
| **SQL Injection (SQLi)** | Occurs when untrusted input is inserted into a SQL query without proper sanitization, allowing an attacker to read, modify, or delete database data. |
| **Cross-Site Scripting (XSS)** | Occurs when untrusted input is reflected or stored in a web page without proper encoding, allowing an attacker to execute arbitrary JavaScript in a victim's browser. |
| **Insecure Direct Object Reference (IDOR)** | Occurs when an application exposes a direct reference (e.g., an ID in a URL) to an internal object without verifying the requester is authorized to access it. |
| **Security Misconfiguration** | Vulnerabilities introduced by default credentials, verbose error messages, unnecessary services, or improperly hardened server configurations. |

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

**Directory & content discovery** — enumerate hidden paths using a wordlist
```bash
gobuster dir -u <URL> -w <WORDLIST>       # brute-force directories/files over HTTP
ffuf -u http://target/FUZZ -w wordlist.txt # fast web fuzzer, replaces FUZZ keyword
```

**Reconnaissance** — gather headers and mirror site content
```bash
curl -I <URL>          # fetch only the response headers
wget --mirror <URL>    # download a full local copy of a site for offline review
```

**Local search / flag hunting**
```bash
grep -R "flag" .       # recursively search all files in the current directory
```

### 📖 Key Takeaways

- Understand how HTTP requests and responses work before attempting exploitation.
- Enumerate a web application thoroughly to map its attack surface before testing.
- Always identify the attack surface first — don't jump straight to exploitation.
- Authentication and authorization are distinct concepts and fail in different ways.
- Practice identifying common web vulnerabilities using safe, legal lab environments.

---

## 🐧 2. Linux

<img src="https://img.shields.io/badge/Domain-Operating%20Systems-16A34A?style=flat-square" />
<img src="https://img.shields.io/badge/Rooms-2-16A34A?style=flat-square" />

A strong command of Linux is a prerequisite for nearly every security discipline — the majority of security tooling, servers, and lab environments (including TryHackMe itself) run on Linux.

### 📋 Completed Rooms

- Linux Fundamentals Part 1
- Linux CLI

### 🎯 Core Concepts

| Concept | Description |
|---|---|
| **Filesystem Hierarchy** | The standardized directory structure (`/etc`, `/var`, `/home`, etc.) used across Linux distributions. |
| **Shell Navigation** | Moving through the filesystem and executing commands via a shell such as Bash. |
| **File & Directory Management** | Creating, copying, moving, and deleting files and directories. |
| **File Permissions** | The read/write/execute permission model, and ownership by user, group, and other. |
| **User & Group Management** | Creating and managing accounts and privilege boundaries. |
| **Process Management** | Viewing, monitoring, and terminating running processes. |
| **Package Management** | Installing and updating software via a distribution's package manager. |
| **Text Processing** | Searching, filtering, and transforming text streams — essential for log analysis. |

### 🛠️ Tool Categories & Commands

<details>
<summary><b>Navigation</b></summary>

```bash
pwd     # print current working directory
ls -la  # list all files, including hidden, with details
cd      # change directory
tree    # display directory structure as a tree
```
</details>

<details>
<summary><b>File Management</b></summary>

```bash
touch   # create an empty file
mkdir   # create a directory
cp      # copy files/directories
mv      # move or rename files/directories
rm      # remove files
rmdir   # remove empty directories
cat     # print file contents
less    # paginated file viewer
head    # show first lines of a file
tail    # show last lines of a file
```
</details>

<details>
<summary><b>File Searching</b></summary>

```bash
find      # search for files matching criteria
locate    # search a prebuilt file index
which     # show the path of an executable
whereis   # locate binary, source, and manual files
```
</details>

<details>
<summary><b>Text Processing</b></summary>

```bash
grep    # search text using patterns
sort    # sort lines of text
uniq    # filter duplicate adjacent lines
wc      # count lines, words, characters
cut     # extract sections from each line
awk     # pattern scanning and text processing language
sed     # stream editor for filtering/transforming text
```
</details>

<details>
<summary><b>Permissions</b></summary>

```bash
chmod   # change file permissions
chown   # change file owner
chgrp   # change group ownership
umask   # set default permission mask for new files
```
</details>

<details>
<summary><b>Process Management</b></summary>

```bash
ps       # snapshot of running processes
top      # real-time process monitor
htop     # enhanced interactive process viewer
kill     # terminate a process by PID
killall  # terminate processes by name
jobs     # list background jobs in the current shell
```
</details>

<details>
<summary><b>Networking</b></summary>

```bash
ip a       # show network interfaces and addresses
ifconfig   # legacy interface configuration tool
ping       # test host reachability
netstat    # show network connections/statistics
ss         # modern socket statistics tool
curl       # transfer data from/to a URL
wget       # download files from the web
```
</details>

<details>
<summary><b>Archives</b></summary>

```bash
tar     # archive multiple files into one
gzip    # compress files
gunzip  # decompress .gz files
zip     # create zip archives
unzip   # extract zip archives
```
</details>

### 📖 Key Takeaways

- Linux is the foundation of many cybersecurity tools and environments.
- Efficient command-line usage improves productivity during security assessments.
- Understanding file permissions is essential for privilege management.
- Mastering text-processing commands helps analyze logs and system data.
- Networking utilities are valuable for troubleshooting and reconnaissance.

---

## 🌐 3. Networking

<img src="https://img.shields.io/badge/Domain-Infrastructure-2563EB?style=flat-square" />
<img src="https://img.shields.io/badge/Rooms-2-16A34A?style=flat-square" />

Networking knowledge underpins nearly every other security domain: understanding how hosts communicate is essential for reconnaissance, exploitation, monitoring, and forensics alike.

### 📋 Completed Rooms

- What is Networking?
- Network Discovery

### 🎯 Core Concepts

| Concept | Description |
|---|---|
| **OSI Model** | A seven-layer conceptual model describing how data moves from physical transmission up to the application layer. |
| **TCP/IP Model** | The practical four-layer model (Link, Internet, Transport, Application) that underlies real-world networking. |
| **IP Addressing** | The logical addressing scheme (IPv4/IPv6) used to identify hosts on a network. |
| **MAC Addresses** | Hardware-level addresses used for communication within a local network segment. |
| **DNS** | The system that resolves human-readable domain names into IP addresses. |
| **Common Protocols** | HTTP/HTTPS, FTP, and SSH, each serving distinct purposes for data transfer and remote access. |
| **Port Scanning** | The process of probing a host to determine which network ports are open and what services are listening. |
| **Network Discovery** | Techniques used to identify live hosts and map a network's topology. |

### 🛠️ Tools Used

<p>
<img src="https://img.shields.io/badge/Nmap-1F2937?style=flat-square" />
<img src="https://img.shields.io/badge/Netcat-374151?style=flat-square" />
<img src="https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white" />
<img src="https://img.shields.io/badge/curl-073551?style=flat-square&logo=curl&logoColor=white" />
<img src="https://img.shields.io/badge/wget-4A4A4A?style=flat-square&logo=gnu&logoColor=white" />
</p>

### 💻 Command Reference

**Host discovery** — identify live systems on a network
```bash
ping <target>   # check if a host is reachable
arp -a          # list known hosts on the local network segment
ip a            # display local network interface details
```

**DNS resolution** — resolve and inspect domain records
```bash
nslookup <domain>   # query DNS records interactively
dig <domain>        # detailed DNS lookup utility
host <domain>        # simple DNS lookup utility
```

**Network information**
```bash
ifconfig    # display/configure network interfaces (legacy)
ip addr     # display IP address information (modern)
ip route    # display the routing table
hostname    # display the system's hostname
```

**Port scanning** — determine open ports and running services
```bash
nmap <target>       # default TCP scan
nmap -sV <target>   # detect service versions
nmap -A <target>    # aggressive scan (OS detection, versions, scripts)
nmap -Pn <target>   # skip host discovery (treat host as online)
```

**Connectivity testing**
```bash
telnet <host> <port>   # test raw TCP connectivity to a port
nc -lvnp 4444           # start a listener on port 4444
curl <URL>               # send an HTTP request
wget <URL>               # download a file over HTTP(S)
```

### 🔑 Common Ports Reference

| Port | Protocol | Service |
|------|----------|---------|
| 20/21 | TCP | FTP |
| 22 | TCP | SSH |
| 23 | TCP | Telnet |
| 25 | TCP | SMTP |
| 53 | TCP/UDP | DNS |
| 80 | TCP | HTTP |
| 110 | TCP | POP3 |
| 143 | TCP | IMAP |
| 443 | TCP | HTTPS |
| 445 | TCP | SMB |
| 3389 | TCP | RDP |

### 📖 Key Takeaways

- Networking forms the foundation of cybersecurity.
- Understanding protocols is essential for identifying security issues.
- Enumeration should always be the first step during an assessment.
- DNS can reveal valuable information about a target.
- Port scanning helps identify exposed services.
- Service enumeration provides insight into potential attack surfaces.

---

## ⚔️ 4. Offensive Security

<img src="https://img.shields.io/badge/Domain-Red%20Team-DC2626?style=flat-square" />
<img src="https://img.shields.io/badge/Rooms-5-16A34A?style=flat-square" />

Offensive security (red teaming) simulates the tactics, techniques, and procedures of real-world attackers in order to identify weaknesses before malicious actors can exploit them.

### 📋 Completed Rooms

- Offensive Security Intro
- Hydra
- CyberChef: The Basics
- Search Skills
- Exploitation with cURL

### 🎯 Core Concepts

| Concept | Description |
|---|---|
| **Ethical Hacking Fundamentals** | The legal and procedural framework (scope, authorization, rules of engagement) that governs offensive testing. |
| **Information Gathering** | The initial phase of any engagement: collecting data about a target to inform later exploitation. |
| **Enumeration** | Actively probing a target to extract detailed information about services, users, and configurations. |
| **Password Attacks** | Techniques such as brute-forcing and credential stuffing used to compromise authentication mechanisms. |
| **HTTP Request Crafting** | Manually building and modifying HTTP requests to test application behavior and bypass restrictions. |
| **CTF Methodology** | A systematic, repeatable approach to solving Capture The Flag challenges — recon, enumerate, exploit, escalate. |

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

**Hydra** — automated credential brute-forcing
```bash
hydra -l admin -P rockyou.txt ssh://<target>
hydra -L users.txt -P passwords.txt ftp://<target>
hydra -l admin -P passwords.txt http-post-form "/login:user=^USER^&pass=^PASS^:Invalid"
```

**cURL** — crafting and sending HTTP requests
```bash
curl http://example.com                                   # basic GET request
curl -I http://example.com                                 # headers only
curl -X POST http://example.com/login                      # send a POST request
curl -H "Authorization: Bearer <TOKEN>" http://example.com/api  # authenticated request
```

**Enumeration**
```bash
nmap -A <target>
gobuster dir -u http://<target> -w wordlist.txt
ffuf -u http://target/FUZZ -w wordlist.txt
```

### 📖 Key Takeaways

- Enumeration is the foundation of offensive security.
- Always understand the target before attempting exploitation.
- Password attacks should only be performed in authorized environments.
- HTTP requests can be crafted and modified using tools like cURL and Burp Suite.
- Small pieces of information gathered during reconnaissance often lead to successful exploitation.

---

## 🛡️ 5. Defensive Security

<img src="https://img.shields.io/badge/Domain-Blue%20Team-2563EB?style=flat-square" />
<img src="https://img.shields.io/badge/Rooms-10-16A34A?style=flat-square" />

Defensive security (blue teaming) focuses on detecting, analyzing, and responding to threats — the counterpart discipline to offensive testing, centered on protecting systems rather than attacking them.

### 📋 Completed Rooms

- Defensive Security Intro
- Junior Security Analyst Intro
- Threat Hunting: Introduction
- Splunk Basics
- Preparation
- Intro to Digital Forensics
- Registry Forensics
- Malware Analysis
- Web Attack Forensics
- YARA Rules

### 🎯 Core Concepts

| Concept | Description |
|---|---|
| **Security Operations Center (SOC)** | The centralized team and function responsible for continuous monitoring and incident response. |
| **Threat Hunting** | Proactively searching for threats that have evaded existing automated detection. |
| **Incident Response** | The structured process of detecting, containing, eradicating, and recovering from a security incident. |
| **SIEM Fundamentals** | Security Information and Event Management platforms that centralize and correlate log data (e.g., Splunk). |
| **Malware Analysis** | Examining suspicious files/binaries to understand their behavior and impact. |
| **Windows Registry Analysis** | Investigating the Windows Registry for artifacts of user or attacker activity. |
| **YARA Rule Development** | Writing pattern-matching rules to identify and classify malware samples. |

### 🛠️ Tools Used

<p>
<img src="https://img.shields.io/badge/Splunk-000000?style=flat-square&logo=splunk&logoColor=white" />
<img src="https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white" />
<img src="https://img.shields.io/badge/YARA-4B5563?style=flat-square" />
<img src="https://img.shields.io/badge/Windows%20Event%20Viewer-0078D4?style=flat-square&logo=windows&logoColor=white" />
<img src="https://img.shields.io/badge/Sysinternals-0078D4?style=flat-square&logo=windows&logoColor=white" />
<img src="https://img.shields.io/badge/CyberChef-1E90FF?style=flat-square" />
<img src="https://img.shields.io/badge/VirusTotal-394EFF?style=flat-square" />
<img src="https://img.shields.io/badge/Kali%20Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white" />
</p>

### 💻 Command Reference

**Windows event logs**
```powershell
Get-WinEvent -LogName Security   # query the Security event log
Get-EventLog -LogName System     # query the System event log
```

**Linux log analysis**
```bash
cat /var/log/auth.log            # view authentication log
tail -f /var/log/syslog          # follow the system log in real time
grep "Failed" /var/log/auth.log  # filter for failed login attempts
journalctl                       # query the systemd journal
```

**YARA** — malware pattern matching
```bash
yara rule.yar sample.exe    # scan a single file against a rule
yara -r rules/ samples/     # recursively scan a directory
```

**Network analysis**
```bash
tcpdump -i eth0    # capture live traffic on interface eth0
netstat -tulnp     # show listening TCP/UDP ports and owning processes
ss -tuln           # modern replacement for netstat
```

### 📖 Key Takeaways

- Defensive security focuses on detecting, analyzing, and responding to cyber threats.
- Log analysis is one of the most valuable skills for identifying malicious activity.
- Threat hunting requires understanding attacker behavior and indicators of compromise (IOCs).
- SIEM platforms centralize logs to improve visibility and incident detection.
- Digital forensics helps determine the timeline and impact of security incidents.
- YARA rules assist in identifying malware based on known patterns.

---

## 🔬 6. Digital Forensics

<img src="https://img.shields.io/badge/Domain-Incident%20Investigation-7C3AED?style=flat-square" />
<img src="https://img.shields.io/badge/Rooms-3-16A34A?style=flat-square" />

Digital forensics is the discipline of identifying, preserving, analyzing, and reporting on digital evidence in a manner that maintains its integrity and admissibility.

### 📋 Completed Rooms

- Intro to Digital Forensics
- Registry Forensics
- Web Attack Forensics

### 🎯 Core Concepts

| Concept | Description |
|---|---|
| **Chain of Custody** | The documented, unbroken trail proving how evidence was collected, handled, and preserved. |
| **Windows Registry Analysis** | Examining registry hives for evidence of program execution, user activity, or persistence mechanisms. |
| **Browser Forensics** | Analyzing browser history, cache, and cookies to reconstruct user activity. |
| **Timeline Analysis** | Correlating timestamped artifacts across systems to reconstruct the sequence of an incident. |
| **Indicators of Compromise (IOCs)** | Observable artifacts (file hashes, IPs, domains) that indicate malicious activity has occurred. |
| **Digital Evidence Preservation** | Techniques (e.g., hashing) used to prove evidence has not been altered since collection. |

### 🛠️ Tools Used

<p>
<img src="https://img.shields.io/badge/Autopsy-2563EB?style=flat-square" />
<img src="https://img.shields.io/badge/FTK%20Imager-6B7280?style=flat-square" />
<img src="https://img.shields.io/badge/Registry%20Explorer-0078D4?style=flat-square&logo=windows&logoColor=white" />
<img src="https://img.shields.io/badge/CyberChef-1E90FF?style=flat-square" />
<img src="https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white" />
<img src="https://img.shields.io/badge/Volatility-4B5563?style=flat-square" />
<img src="https://img.shields.io/badge/Kali%20Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white" />
</p>

### 💻 Command Reference

**Linux log analysis**
```bash
cat /var/log/auth.log
tail -f /var/log/syslog
grep "Failed" /var/log/auth.log
journalctl
```

**File integrity verification**
```bash
sha256sum file    # generate a SHA-256 hash of a file
md5sum file       # generate an MD5 hash of a file
file filename     # identify a file's type from its contents
```

**Windows event logs (PowerShell)**
```powershell
Get-WinEvent -LogName Security
Get-EventLog -LogName System
```

**Network investigation**
```bash
tcpdump -i eth0
netstat -tulnp
ss -tuln
```

### 📖 Key Takeaways

- Digital forensics focuses on identifying, preserving, analyzing, and reporting digital evidence.
- Evidence integrity must always be maintained during an investigation.
- Hash values are used to verify that evidence has not been modified.
- Windows Registry artifacts provide valuable information about user activity and system changes.
- Log analysis helps reconstruct attack timelines and identify malicious behavior.
- Browser artifacts can reveal user actions and web-based attacks.

---

## 🔎 7. Open Source Intelligence (OSINT)

<img src="https://img.shields.io/badge/Domain-Reconnaissance-EAB308?style=flat-square" />
<img src="https://img.shields.io/badge/Rooms-3-16A34A?style=flat-square" />

OSINT is the practice of collecting and analyzing information from publicly available sources to build a profile of a target — a technique used by both attackers during reconnaissance and defenders during investigations.

### 📋 Completed Rooms

- Missing Person
- Digital Footprint
- Water Bottle

### 🎯 Core Concepts

| Concept | Description |
|---|---|
| **Information Gathering** | Collecting publicly accessible data points relevant to a target individual or organization. |
| **Search Engine Techniques** | Using advanced operators ("Google Dorking") to surface hard-to-find indexed information. |
| **Digital Footprinting** | Mapping the traces an individual or organization leaves across the internet over time. |
| **Username Enumeration** | Correlating a single username across multiple platforms to build a broader profile. |
| **Domain Intelligence** | Gathering ownership, hosting, and infrastructure data about a domain. |
| **Metadata Analysis** | Extracting hidden data embedded in files (e.g., GPS coordinates in image EXIF data). |
| **Geolocation** | Determining a physical location from images, posts, or metadata. |

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

**DNS enumeration**
```bash
whois example.com     # retrieve domain registration details
nslookup example.com  # resolve domain to IP
dig example.com       # detailed DNS query tool
```

**Network information**
```bash
ping example.com
traceroute example.com   # trace the network path to a host
```

**Email harvesting**
```bash
theHarvester -d example.com -b all   # gather emails/subdomains from public sources
```

**Username enumeration**
```bash
sherlock username    # search a username across many platforms
```

**Metadata analysis**
```bash
exiftool image.jpg   # extract embedded metadata from a file
```

### 📖 Key Takeaways

- OSINT relies entirely on publicly available information.
- Effective reconnaissance helps build a complete understanding of a target before any security assessment.
- Search engines are powerful OSINT tools when combined with advanced search operators.
- Metadata can reveal valuable hidden information.
- Digital footprints can expose sensitive information unintentionally.
- Always verify information using multiple reliable sources.

---

## ⚠️ Ethical Use Disclaimer

All techniques, tools, and commands documented in this repository were practiced exclusively in authorized environments such as **TryHackMe**, Capture The Flag (CTF) platforms, and personal lab environments. This material is intended solely for educational purposes and responsible cybersecurity learning. Using any of these techniques against systems without explicit, written authorization is unethical and may be illegal under applicable computer misuse laws.

> *"Good intelligence comes from asking the right questions, verifying the evidence, and connecting the pieces together. Good security comes from understanding both sides of the fight — offense and defense."*

<div align="center">

---

**Last updated: July 2026**

</div>