# Cybersecurity Basics

## CIA Triad
The **CIA Triad** is the foundational model for information security policy and strategy:
* **Confidentiality:** Ensures sensitive information is accessible only to authorized individuals, entities, or processes. (e.g., Encryption, Access Control Lists, MFA).
* **Integrity:** Guarantees that data remains accurate, complete, and untampered during storage, transit, or processing. (e.g., Hashing, Digital Signatures, Version Control).
* **Availability:** Ensures information and critical systems are accessible and operational when needed by authorized users. (e.g., Redundancy, Load Balancing, DDoS Mitigation, Backups).

---

## Common Security Concepts & Threats

### 1. Phishing
Social engineering attacks where attackers impersonate trustworthy entities (via email, SMS, or websites) to trick users into revealing sensitive information like credentials or credit card numbers.
* *Types:* Spear phishing (targeted), Whaling (executive-targeted), Vishing (voice), Smishing (SMS).

### 2. Malware
Malicious software designed to infiltrate, damage, or compromise computer systems without consent.
* *Types:* Viruses, Worms, Trojans, Spyware, Keyloggers, Adware, Rootkits.

### 3. Distributed Denial of Service (DDoS)
An attempt to make an online service unavailable by overwhelming it with massive traffic from multiple compromised sources (botnets).
* *Common Types:* SYN floods, HTTP floods, UDP amplification.

### 4. SQL Injection (SQLi)
A code injection vulnerability occurring when untrusted user input is directly concatenated into SQL database queries without validation or sanitization, allowing attackers to read, alter, or delete database contents.
* *Mitigation:* Prepared statements (parameterized queries), input validation, ORMs.

### 5. Brute Force
An automated attack method consisting of systematically trying all possible combinations of passwords or keys until the correct one is found.
* *Mitigation:* Strong password policies, rate limiting, account lockouts, multi-factor authentication (MFA).

### 6. Ransomware
Malicious software that encrypts a victim's data or locks the system, demanding a ransom payment in exchange for decryption keys.
* *Mitigation:* Offline backups, regular security patching, endpoint detection and response (EDR).

### 7. Social Engineering
Psychological manipulation techniques used to trick individuals into divulging confidential information or executing actions that compromise security.
* *Techniques:* Baiting, Pretexting, Tailgating, Quid Pro Quo.

### 8. Wireless Attacks
Threats directed at wireless networks to intercept traffic or breach network security.
* *Examples:* Evil Twin attacks, Rogue Access Points, WPA2/WPA3 cracking, Deauthentication attacks, Man-in-the-Middle (MitM) sniffing.

### 9. Insider Threats
Security risks originating from within the organization—such as current or former employees, contractors, or business associates who misuse authorized access to data or systems.
* *Categories:* Malicious insiders, negligent users, compromised accounts.
