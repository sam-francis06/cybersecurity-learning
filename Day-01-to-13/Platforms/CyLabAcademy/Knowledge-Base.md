<div align="center">

# 📘 Knowledge Base

### Consolidated Concepts, Tools, and Techniques from CyLab Security Academy

![Type](https://img.shields.io/badge/Type-Reference%20Document-2563EB?style=for-the-badge)
![Domains](https://img.shields.io/badge/Domains%20Covered-8-16A34A?style=for-the-badge)
![Updated](https://img.shields.io/badge/Last%20Updated-July%202026-6B7280?style=for-the-badge)

</div>

---

## 📖 Purpose

This document serves as a consolidated reference of the concepts, tools, commands, and techniques learned while solving challenges on **CyLab Security Academy**. Unlike a challenge-by-challenge write-up, this knowledge base is organized around **reusable, transferable knowledge** — the kind that applies across future Capture The Flag (CTF) challenges and real-world cybersecurity assessments, regardless of which specific challenge originally taught it.

---

## 🌐 Web Exploitation

### Topics Covered

| Topic | Explanation |
|---|---|
| **HTTP Methods** | The verbs (GET, POST, PUT, DELETE, etc.) that define the action an HTTP request intends to perform. |
| **Request & Response Analysis** | Inspecting raw HTTP traffic to understand how an application processes input and returns output. |
| **Cookies & Sessions** | Mechanisms used to maintain state across otherwise stateless HTTP requests. |
| **Authentication vs. Authorization** | Authentication confirms identity; authorization determines permitted actions — the two fail differently. |
| **Client-Side Validation** | Input checks enforced in the browser, which can typically be bypassed since they don't run server-side. |
| **Directory Enumeration** | Discovering hidden files and endpoints not linked from the visible application. |
| **SQL Injection (SQLi)** | Inserting malicious input into a SQL query to read, modify, or delete database data. |
| **Cross-Site Scripting (XSS)** | Injecting client-side scripts into a trusted context so they execute in a victim's browser. |
| **Server-Side Template Injection (SSTI)** | Injecting input that is evaluated by a server-side templating engine, potentially leading to code execution. |
| **Source Code Analysis** | Reviewing exposed or leaked source code to identify logic flaws or hardcoded secrets. |
| **File Inclusion** | Exploiting an application's file-loading logic to read or execute unintended files. |
| **Web Reconnaissance** | Mapping an application's structure and technology stack before testing begins. |

### Tools

<p>
<img src="https://img.shields.io/badge/Burp%20Suite-FF6633?style=flat-square&logo=burpsuite&logoColor=white" />
<img src="https://img.shields.io/badge/Browser%20DevTools-4285F4?style=flat-square&logo=googlechrome&logoColor=white" />
<img src="https://img.shields.io/badge/curl-073551?style=flat-square&logo=curl&logoColor=white" />
<img src="https://img.shields.io/badge/wget-4A4A4A?style=flat-square&logo=gnu&logoColor=white" />
<img src="https://img.shields.io/badge/Gobuster-374151?style=flat-square" />
<img src="https://img.shields.io/badge/ffuf-4B5563?style=flat-square" />
</p>

### Command Reference

```bash
curl -I http://target                          # fetch response headers only
curl -X POST http://target                     # send a POST request
wget --mirror http://target                    # download a full local copy of a site
gobuster dir -u http://target -w wordlist.txt   # brute-force hidden directories
ffuf -u http://target/FUZZ -w wordlist.txt      # fast web fuzzing
```

---

## 🔐 Cryptography

### Topics Covered

| Topic | Explanation |
|---|---|
| **Caesar Cipher** | A substitution cipher that shifts each letter by a fixed number of positions. |
| **ROT13** | A special case of the Caesar cipher using a fixed shift of 13. |
| **Base64** | An encoding scheme that represents binary data as printable ASCII text — reversible, not encryption. |
| **Hex Encoding** | Representing byte values as pairs of hexadecimal digits. |
| **RSA Basics** | An asymmetric cryptographic scheme relying on the difficulty of factoring large numbers. |
| **Hash Functions** | One-way functions that produce a fixed-size digest from arbitrary input, used for integrity checks. |
| **Encoding vs. Encryption** | Encoding is reversible without a key; encryption requires a key to reverse. |
| **Frequency Analysis** | Using letter frequency patterns to break classical substitution ciphers. |
| **Classical Ciphers** | Pre-modern encryption schemes (substitution, transposition) often used as an introduction to cryptanalysis. |

### Tools

<p>
<img src="https://img.shields.io/badge/CyberChef-1E90FF?style=flat-square" />
<img src="https://img.shields.io/badge/OpenSSL-721412?style=flat-square&logo=openssl&logoColor=white" />
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
</p>

### Command Reference

```bash
base64 -d file.txt              # decode a Base64-encoded file
openssl dgst -sha256 file.txt   # generate a SHA-256 hash digest
xxd file                        # produce a hex dump of a file
```

---

## 🔍 Digital Forensics

### Topics Covered

| Topic | Explanation |
|---|---|
| **File Analysis** | Determining a file's true type and structure, regardless of its extension. |
| **Metadata Analysis** | Extracting hidden data embedded within a file, such as EXIF fields in images. |
| **Disk Forensics** | Examining disk images to recover files, partitions, and deleted data. |
| **Packet Analysis** | Inspecting captured network traffic to reconstruct communications or extract data. |
| **Registry Analysis** | Investigating the Windows Registry for artifacts of user or system activity. |
| **Hidden Files** | Identifying files or data intentionally concealed from normal view. |
| **Image Analysis** | Detecting steganography or manipulated content within image files. |
| **Log Investigation** | Reviewing system or application logs to reconstruct a timeline of events. |

### Tools

<p>
<img src="https://img.shields.io/badge/Autopsy-2563EB?style=flat-square" />
<img src="https://img.shields.io/badge/Sleuthkit-374151?style=flat-square" />
<img src="https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white" />
<img src="https://img.shields.io/badge/CyberChef-1E90FF?style=flat-square" />
<img src="https://img.shields.io/badge/ExifTool-4B5563?style=flat-square" />
</p>

### Command Reference

```bash
file filename        # identify a file's type from its contents
strings filename      # extract readable text from a binary file
exiftool image.jpg     # extract embedded metadata from an image
sha256sum file          # generate a hash to verify file integrity
```

---

## ⚙️ Reverse Engineering

### Topics Covered

| Topic | Explanation |
|---|---|
| **Binary Analysis** | Examining a compiled program's structure to understand its behavior. |
| **Decompiled Code** | Higher-level pseudocode generated from a binary to aid human analysis. |
| **Strings Analysis** | Extracting embedded readable text from a binary, often revealing hardcoded logic or secrets. |
| **Program Logic** | Tracing the control flow and decision points within a program. |
| **Input Validation** | Identifying how (or whether) a program checks and sanitizes user-supplied input. |
| **Assembly Basics** | Reading low-level CPU instructions to understand exact program behavior. |

### Tools

<p>
<img src="https://img.shields.io/badge/Ghidra-9CCC65?style=flat-square" />
<img src="https://img.shields.io/badge/strings-4B5563?style=flat-square" />
<img src="https://img.shields.io/badge/objdump-374151?style=flat-square" />
<img src="https://img.shields.io/badge/GDB-1F2937?style=flat-square" />
</p>

### Command Reference

```bash
strings binary       # extract readable text from a binary
objdump -d binary    # disassemble a binary into assembly instructions
file binary          # identify the binary's format and architecture
```

---

## 💣 Binary Exploitation

### Topics Covered

| Topic | Explanation |
|---|---|
| **Buffer Overflow Basics** | Writing more data to a buffer than it can hold, corrupting adjacent memory. |
| **Stack Memory** | The region storing local variables and return addresses — a common exploitation target. |
| **Heap Memory** | Dynamically allocated memory, exploitable through corruption of its management structures. |
| **Format String Vulnerabilities** | Exploiting improper use of format functions (e.g., `printf`) to read or write memory. |
| **Memory Corruption** | Any unintended modification of memory that alters a program's behavior. |
| **Input Validation** | Assessing whether a program properly checks input length and type before processing it. |

### Tools

<p>
<img src="https://img.shields.io/badge/GDB-1F2937?style=flat-square" />
<img src="https://img.shields.io/badge/pwndbg-374151?style=flat-square" />
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/checksec-4B5563?style=flat-square" />
</p>

### Command Reference

```bash
checksec binary   # inspect a binary's security mitigations (ASLR, NX, PIE, etc.)
gdb binary        # launch the GNU Debugger against a binary
```

---

## 🤖 Artificial Intelligence Security

### Topics Covered

| Topic | Explanation |
|---|---|
| **Prompt Injection** | Crafting input designed to override or manipulate an AI system's intended instructions. |
| **AI Security** | The broader discipline of identifying and mitigating risks specific to AI-driven systems. |
| **LLM Behavior** | Understanding how large language models interpret and respond to varied input. |
| **Model Manipulation** | Techniques used to alter a model's output in unintended ways. |
| **Prompt Engineering** | Structuring input deliberately to achieve a specific, reliable model response. |

### Skills Practiced

- Prompt analysis
- AI-specific threat identification
- Prompt manipulation techniques

---

## ⛓️ Blockchain

### Topics Covered

| Topic | Explanation |
|---|---|
| **Smart Contracts** | Self-executing code deployed on a blockchain, immutable once published. |
| **Integer Overflow** | A vulnerability where a numeric value exceeds its storage limit and wraps unexpectedly. |
| **Blockchain Security Basics** | Foundational risks specific to decentralized, contract-driven systems. |

---

## 🧩 General Skills — Linux

### Topics Covered

| Topic | Explanation |
|---|---|
| **File Management** | Creating, moving, copying, and deleting files and directories. |
| **Permissions** | The read/write/execute model governing access to files and directories. |
| **Networking** | Basic connectivity, testing, and troubleshooting between hosts. |
| **SSH** | Secure remote access and file transfer between systems. |
| **File Searching** | Locating files by name, content, or type across the filesystem. |

### Command Reference

```bash
ls -la    # list all files, including hidden, with details
pwd       # print current working directory
find      # search for files matching specific criteria
grep      # search text using patterns
cat       # print file contents
chmod     # change file permissions
ssh       # securely connect to a remote host
scp       # securely copy files between hosts
```

---

## 🛠️ Frequently Used Tools

| Category | Tools |
|---|---|
| **Web** | Burp Suite, curl, wget, Gobuster, ffuf |
| **Cryptography** | CyberChef, OpenSSL |
| **Forensics** | Autopsy, Sleuthkit, Wireshark, ExifTool |
| **Reverse Engineering** | Ghidra, strings, objdump, GDB |
| **Binary Exploitation** | GDB, pwndbg, checksec |
| **Linux** | grep, find, cat, ssh |

---

## 📖 Key Takeaways

- Enumeration is the foundation of every successful assessment.
- Small pieces of information often lead to larger discoveries.
- Understanding the underlying technology is more valuable than memorizing solutions.
- Documenting commands and observations improves long-term retention.
- Consistent practice across different challenge categories strengthens analytical thinking and technical confidence.

---

## 📚 References

| Resource | Purpose |
|---|---|
| [OWASP Top 10](https://owasp.org/www-project-top-ten/) | Industry-standard reference for critical web application security risks. |
| [MITRE ATT&CK Framework](https://attack.mitre.org/) | A knowledge base of adversary tactics and techniques observed in the real world. |
| CyberChef | Browser-based tool for encoding, decoding, and data analysis. |
| Ghidra | Free software reverse-engineering suite. |
| Wireshark | Network protocol analyzer for packet-level inspection. |
| Burp Suite Documentation | Reference for web application security testing workflows. |
| Linux Manual Pages (`man`) | The authoritative reference for command-line utilities. |
| Python Documentation | Reference for scripting and automation used throughout multiple domains. |

---

<div align="center">

> *"Knowledge gained through hands-on practice becomes a reusable skill. This knowledge base serves as a long-term cybersecurity reference, built through solving real challenges on CyLab Security Academy."*

**Last updated: July 2026**

</div>