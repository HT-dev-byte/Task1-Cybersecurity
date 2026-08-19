# Task 1: Foundation Environment & Cybersecurity Basics

Welcome to the **Task 1 Foundation Environment** repository. This repository contains foundational cybersecurity notes, an essential Linux command cheat sheet, networking & cryptography reference guides, security tool documentation, and complete lab setup documentation for a virtual penetration testing environment.

---

## 🎯 Objectives
* Establish a clean, well-structured repository for cybersecurity foundational concepts.
* Master core command-line Linux operations and essential security tools (Nmap, Wireshark, Burp Suite, Netcat).
* Configure and document an isolated virtual lab environment using VirtualBox, Kali Linux, and Metasploitable 2.
* Verify inter-VM connectivity, conduct service scans, and capture network packets in real time.

---

## 🏗️ Repository Architecture

```text
Task-1-Foundation-Environment/
│
├── README.md                           # Main repository landing page & documentation index
│
├── cybersecurity-basics/
│   └── notes.md                        # CIA triad, phishing, malware, DDoS, SQLi, ransomware, etc.
│
├── linux/
│   └── linux-cheat-sheet.md            # Command line operations (files, permissions, networking, packages)
│
├── networking/
│   └── notes.md                        # OSI & TCP/IP models, TCP vs UDP, DNS, HTTP/S, CIDR subnetting
│
├── cryptography/
│   └── notes.md                        # Symmetric/Asymmetric, Hashing, SSL/TLS, OpenSSL experiment
│
├── tools/
│   └── notes.md                        # Wireshark, Nmap, Burp Suite, Netcat overview & command usage
│
├── lab-setup/
│   ├── lab-report.md                   # Full virtual environment lab build and test report
│   └── screenshots/                    # Verification screenshots
│       ├── kali-linux.png
│       ├── target-machine.png
│       ├── host-only-network.png
│       ├── connectivity-test.png
│       └── wireshark-capture.png
│
└── video/
    └── walkthrough-link.md             # Walkthrough video link and summary
```

---

## 🛠️ Lab Setup & Technologies Used
* **Hypervisor:** Oracle VM VirtualBox
* **Attacker VM:** Kali Linux (`192.168.56.102`)
* **Target VM:** Metasploitable 2 / DVWA (`192.168.56.101`)
* **Networking:** VirtualBox Host-Only Adapter (`192.168.56.0/24`)
* **Core Security Tools:** `nmap`, `wireshark`, `openssl`, `ping`, `ss`, `netcat`, `burpsuite`

---

## 📖 Quick Links & Navigation

* 🛡️ **[Cybersecurity Basics](cybersecurity-basics/notes.md)** – Detailed notes on fundamental security concepts & threats.
* 🐧 **[Linux Cheat Sheet](linux/linux-cheat-sheet.md)** – Command-line reference guide for system management & troubleshooting.
* 🌐 **[Networking Notes](networking/notes.md)** – OSI/TCP-IP models, protocols, IP addressing, and NAT.
* 🔐 **[Cryptography Notes](cryptography/notes.md)** – Encryption, hashing, PKI, and OpenSSL practical commands.
* 🧰 **[Security Tools Reference](tools/notes.md)** – Manual & commands for Wireshark, Nmap, Burp Suite, and Netcat.
* 🔬 **[Lab Documentation Report](lab-setup/lab-report.md)** – Complete setup guide, network architecture, and scan/capture results.
* 🎥 **[Video Walkthrough](video/walkthrough-link.md)** – Link and overview of the video walkthrough.
