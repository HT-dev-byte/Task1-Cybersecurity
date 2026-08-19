# Networking Fundamentals

## OSI Model (Open Systems Interconnection)
The OSI model standardizes communication functions into 7 distinct layers:

1. **Layer 7 - Application:** User-facing protocols (HTTP, HTTPS, FTP, SSH, DNS).
2. **Layer 6 - Presentation:** Data format, translation, encryption, and compression (SSL/TLS, JPEG, ASCII).
3. **Layer 5 - Session:** Manages sessions between applications (RPC, NetBIOS).
4. **Layer 4 - Transport:** End-to-end transport and flow control (TCP, UDP).
5. **Layer 3 - Network:** Logical routing and packet addressing (IP, ICMP, IPsec).
6. **Layer 2 - Data Link:** Framing and physical MAC addressing (Ethernet, Switches, ARP).
7. **Layer 1 - Physical:** Transmission of raw bit streams over physical media (Cables, Fiber, Hubs).

---

## TCP/IP Model
A practical 4-layer network model used across the Internet:
* **Application Layer:** Corresponds to OSI Layers 5, 6, 7 (HTTP, DNS, SSH).
* **Transport Layer:** Corresponds to OSI Layer 4 (TCP, UDP).
* **Internet Layer:** Corresponds to OSI Layer 3 (IP, ICMP, ARP).
* **Network Access Layer:** Corresponds to OSI Layers 1 & 2 (Ethernet, Wi-Fi).

---

## TCP vs. UDP

| Feature | TCP (Transmission Control Protocol) | UDP (User Datagram Protocol) |
| :--- | :--- | :--- |
| **Connection Type** | Connection-oriented (3-Way Handshake) | Connectionless |
| **Reliability** | High (Acknowledgements, retransmissions) | Best-effort (No delivery guarantee) |
| **Speed** | Slower due to header overhead & checks | Fast and low latency |
| **Header Size** | 20-60 Bytes | 8 Bytes |
| **Use Cases** | Web browsing (HTTP/S), SSH, File Transfer (FTP) | Streaming video, Gaming, DNS queries, VoIP |

---

## DNS (Domain Name System)
Translates human-readable domain names (e.g., `example.com`) into machine-readable IP addresses (e.g., `93.184.216.34`).
* **Key Record Types:**
  * `A`: IPv4 host record
  * `AAAA`: IPv6 host record
  * `CNAME`: Canonical name (alias)
  * `MX`: Mail exchange server
  * `TXT`: Text record (used for SPF, DKIM verification)

---

## HTTP vs. HTTPS
* **HTTP (Hypertext Transfer Protocol):** Port 80, transmits data in cleartext (vulnerable to eavesdropping).
* **HTTPS (HTTP Secure):** Port 443, encrypts traffic using TLS/SSL to provide confidentiality and authentication.

---

## IP Addressing & Subnetting

### IPv4 vs IPv6
* **IPv4:** 32-bit address space represented in dotted decimal format (e.g., `192.168.1.1`). Total addresses ~4.3 billion.
* **IPv6:** 128-bit address space represented in hexadecimal format (e.g., `fe80::1`).

### Subnetting & CIDR
Subnetting divides a network into smaller subnetworks.
* **CIDR Notation:** Specifies network mask bits (e.g., `192.168.1.0/24`).
* `/24` subnet mask is `255.255.255.0` (256 addresses, 254 usable hosts).

---

## Network Address Translation (NAT)
Translates private IPv4 addresses within a local area network (LAN) into a public IPv4 address before forwarding traffic to the public Internet.
* **Types:** Static NAT, Dynamic NAT, PAT (Port Address Translation / NAT Overload).
