<div align="center">

![OverTheWire](https://img.shields.io/badge/OverTheWire-Bandit%20Wargame-2E8B57?style=for-the-badge&logo=linux&logoColor=white)

# ⚔️ Bandit Wargame

### Linux Fundamentals • Command-Line Proficiency • Problem Solving

![Platform](https://img.shields.io/badge/Platform-OverTheWire-2E8B57?style=for-the-badge)
![Wargame](https://img.shields.io/badge/Wargame-Bandit-2563EB?style=for-the-badge)
![Levels Completed](https://img.shields.io/badge/Levels%20Completed-21-16A34A?style=for-the-badge)
![Current Level](https://img.shields.io/badge/Current%20Level-20-EA580C?style=for-the-badge)
![Updated](https://img.shields.io/badge/Last%20Updated-July%202026-6B7280?style=for-the-badge)

</div>

---

## 📘 About Bandit

**Bandit** is the introductory wargame hosted on **OverTheWire**, purpose-built to teach Linux fundamentals and command-line proficiency through a sequence of progressively challenging levels. Each level is self-contained: solving it reveals a password used to authenticate into the next level via SSH, creating a natural, hands-on progression through increasingly advanced concepts.

Unlike guided tutorials, Bandit requires **active problem-solving** — reading man pages, experimenting with commands, and reasoning through unfamiliar output. This makes it one of the most effective entry points for building the terminal fluency that underpins nearly every other discipline in cybersecurity, from penetration testing to digital forensics.

---

## 🎯 Objectives

| Objective | Why It Matters |
|---|---|
| **Learn Linux command-line fundamentals** | The terminal is the primary interface for almost all security tooling. |
| **Understand the Linux file system** | Knowing where configuration, logs, and data live is essential for both offense and defense. |
| **Navigate directories efficiently** | Speed and accuracy in navigation directly impacts assessment efficiency. |
| **Search for files using different criteria** | Locating specific files by name, type, or content is a recurring task in real investigations. |
| **Understand Linux permissions** | Misconfigured permissions are a common real-world vulnerability class. |
| **Work with compressed and encoded data** | Attackers and defenders alike frequently encounter obfuscated or archived data. |
| **Practice SSH authentication** | SSH is the standard method for secure remote administration and is central to most labs. |
| **Develop logical problem-solving skills** | Bandit's puzzle-like structure builds the analytical habits needed for CTFs and real engagements. |
| **Build confidence using the terminal** | Repetition across 21+ levels turns command syntax into muscle memory. |

---

## 📊 Progress Overview

| Wargame | Range | Status |
|---|---|:---:|
| Bandit | Level 0 → Level 20 | ✅ Completed |

<p align="center">
<img src="https://img.shields.io/badge/Completion-21%20%2F%2034%20Levels-2563EB?style=flat-square" />
<img src="https://img.shields.io/badge/Progress-62%25-16A34A?style=flat-square" />
</p>

**Summary:** 21 of 34 total Bandit levels completed (Level 0 through Level 20), representing roughly 62% of the full wargame.

---

## 📚 Levels Completed

<details>
<summary><b>View full level breakdown (Level 0 – Level 20)</b></summary>

| Level | Status | Level | Status |
|---|:---:|---|:---:|
| Level 0 | ✅ | Level 11 | ✅ |
| Level 1 | ✅ | Level 12 | ✅ |
| Level 2 | ✅ | Level 13 | ✅ |
| Level 3 | ✅ | Level 14 | ✅ |
| Level 4 | ✅ | Level 15 | ✅ |
| Level 5 | ✅ | Level 16 | ✅ |
| Level 6 | ✅ | Level 17 | ✅ |
| Level 7 | ✅ | Level 18 | ✅ |
| Level 8 | ✅ | Level 19 | ✅ |
| Level 9 | ✅ | Level 20 | ✅ |
| Level 10 | ✅ | | |

</details>

---

## 🧠 Skills Developed

| Skill | Description |
|---|---|
| **Linux Navigation** | Confidently traversing the filesystem hierarchy using relative and absolute paths. |
| **Terminal Proficiency** | Comfortable, efficient use of the shell for everyday tasks. |
| **SSH Authentication** | Connecting to remote systems securely using password-based SSH login. |
| **File Enumeration** | Systematically identifying files and directories relevant to a task. |
| **Hidden Files** | Recognizing and working with dotfiles and other non-visible filesystem objects. |
| **File Permissions** | Interpreting and modifying read/write/execute permissions and ownership. |
| **Text Processing** | Filtering, transforming, and extracting meaning from raw text output. |
| **File Searching** | Locating files by name, content, or type across large directory trees. |
| **Data Encoding & Decoding** | Recognizing and reversing common encodings such as Base64 and hex. |
| **Compression & Extraction** | Working with archived and compressed file formats. |
| **Networking Basics** | Establishing and troubleshooting basic network connections. |
| **Port Communication** | Interacting directly with services over specific network ports. |
| **Linux Utilities** | Broad familiarity with the standard Linux toolset used across the industry. |
| **Problem Solving** | Breaking down ambiguous, multi-step challenges into solvable pieces. |

---

## 🛠️ Command Reference

### Navigation
```bash
pwd     # print current working directory
ls      # list directory contents
ls -la  # list all files, including hidden, with details
cd      # change directory
tree    # display directory structure as a tree
```

### File Operations
```bash
cat     # print file contents to the terminal
less    # paginated, scrollable file viewer
head    # display the first lines of a file
tail    # display the last lines of a file
touch   # create an empty file or update its timestamp
cp      # copy a file or directory
mv      # move or rename a file or directory
rm      # remove a file
```

### File Searching
```bash
find     # search for files matching specific criteria (name, size, permissions, etc.)
locate   # search a prebuilt file index for fast lookups
grep     # search text using patterns
file     # determine a file's type from its contents
strings  # extract readable text from a binary file
```

### Permissions
```bash
chmod   # change file permissions (read/write/execute)
chown   # change file ownership (user/group)
```

### Networking
```bash
ssh      # securely connect to a remote host
scp      # securely copy files between hosts
nc       # read/write data across network connections (Netcat)
telnet   # connect to a remote host over a raw TCP port
```

### Encoding & Compression
```bash
base64   # encode/decode data in Base64
xxd      # create or reverse a hex dump of a file
gzip     # compress a file using gzip
gunzip   # decompress a .gz file
tar      # archive (and optionally compress) multiple files
bzip2    # compress a file using bzip2
```

### Text Processing
```bash
sort   # sort lines of text
uniq   # filter out repeated adjacent lines
cut    # extract specific fields/columns from each line
awk    # pattern scanning and text-processing language
sed    # stream editor for filtering and transforming text
tr     # translate or delete specific characters
wc     # count lines, words, and characters
```

---

## 📖 Key Concepts Learned

| Concept | Explanation |
|---|---|
| **Linux Filesystem Hierarchy** | The standardized directory layout (`/`, `/home`, `/etc`, `/tmp`, etc.) that every Linux distribution follows. |
| **Hidden Files & Directories** | Files prefixed with a dot (`.`) that are excluded from default listings but often hold configuration or credential data. |
| **File Permissions & Ownership** | The read/write/execute model applied across user, group, and other, which governs who can access or modify a file. |
| **Standard Input/Output** | The default channels (`stdin`, `stdout`, `stderr`) through which programs receive and send data. |
| **Command Piping** | Chaining commands together with `\|` so the output of one becomes the input of the next. |
| **Text Manipulation** | Using tools like `awk`, `sed`, and `cut` to reshape and extract data from raw text. |
| **Secure Shell (SSH)** | A cryptographic protocol used to securely access and manage remote systems. |
| **Data Encoding Techniques** | Reversible transformations (Base64, hex) used to represent binary data as text, distinct from encryption. |
| **Compression Formats** | Methods such as gzip, bzip2, and tar that reduce file size or bundle multiple files together. |
| **Network Communication** | The basics of establishing, testing, and troubleshooting connections between hosts. |
| **Basic Privilege Concepts** | An early introduction to how access levels and permissions constrain or enable actions on a system. |

---

## 💡 Key Takeaways

- Enumeration is often the most important step when solving challenges.
- Simple Linux commands become extremely powerful when combined through piping.
- Understanding file permissions is essential in cybersecurity.
- Command-line efficiency significantly improves productivity.
- Reading command documentation (`man`) is a valuable habit to build early.
- Breaking problems into smaller steps makes complex challenges manageable.

---

## 📚 Resources

| Resource | Link |
|---|---|
| Platform | [overthewire.org](https://overthewire.org) |
| Bandit Wargame | [overthewire.org/wargames/bandit](https://overthewire.org/wargames/bandit/) |

---

## ⚠️ Ethical Use Disclaimer

All exercises documented here were completed within the official **OverTheWire** practice environment. The techniques and commands described are intended solely for educational purposes and authorized security training.

> *"Master the command line, and you'll master the foundation of cybersecurity."*

<div align="center">

---

**Last updated: July 2026**

</div>