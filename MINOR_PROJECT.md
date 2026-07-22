# INTERNSHIP MINOR PROJECT – CYBER SECURITY

## Project Information

**Submitted By:**
- Name: Anil Kumar
- Roll No: CS-T9/March-9349
- Course: B.Tech 3rd Year, Computer Science and Engineering
- Institute: Rajkiya Engineering College, Sonbhadra

**Internship Details:**
- Company Name: InternsElite
- Program: Cyber Security Program
- Duration: March 2026 – May 2026
- Mentor: Mr. Aman Guta
- Date: April 2026

---

## CERTIFICATE

This is to certify that Anil Kumar (Roll No: CS-T9/March-9349) has successfully completed the Minor Project in Cyber Security as part of the Internship Program conducted by InternsElite during March 2026 – May 2026.

The work submitted is original and carried out under the guidance of the assigned mentor.

**Mentor Signature:** Mr. Aman Guta

---

## ACKNOWLEDGEMENT

I would like to express my sincere gratitude to InternsElite for providing me the opportunity to complete this Cyber Security Minor Project.

I am also thankful to my mentor Mr. Aman Guta for his continuous support, guidance, and encouragement throughout this project.

This project helped me gain practical knowledge of cybersecurity tools and techniques.

---

## ABSTRACT

Cyber Security is a critical field that protects systems, networks, and data from unauthorized access and attacks. This minor project focuses on understanding various cyber threats and security tools used in ethical hacking.

The project includes study and practical understanding of:
- Network scanning
- Reconnaissance
- Malware types
- Password attacks
- Sniffing
- Penetration testing tools

All experiments were performed in a controlled lab environment for educational purposes only.

---

## TABLE OF CONTENTS

1. [Introduction to Cyber Security](#introduction)
2. [Types of Hackers and Hacking](#hackers-and-hacking)
3. [Consequences of Hacking in Corporate Sector](#consequences)
4. [Network Scanning (Angry IP Scanner)](#network-scanning)
5. [Footprinting Techniques](#footprinting)
6. [Reconnaissance using Recon-ng](#reconnaissance)
7. [Vulnerability Scanning using Nmap](#vulnerability-scanning)
8. [Proxy Server and VPN](#proxy-vpn)
9. [Types of Malwares](#malware)
10. [TOR Network](#tor)
11. [Password Attacks](#password-attacks)
12. [DoS & DDoS Attacks](#dos-ddos)
13. [Sniffing and Types](#sniffing)
14. [Kali Linux & Metasploit](#kali-metasploit)
15. [Conclusion](#conclusion)

---

## INTRODUCTION {#introduction}

In today's digital world, cyber threats are increasing rapidly. Organizations face risks such as:
- Hacking
- Data theft
- Malware attacks

Cyber Security helps in protecting systems and ensuring data:
- **Confidentiality** – Only authorized users can access data
- **Integrity** – Data is not modified without permission
- **Availability** – Data and systems are accessible when needed

This project focuses on basic cybersecurity concepts and tools used in ethical hacking and penetration testing.

---

## TOPIC 1: TYPES OF HACKERS AND HACKING {#hackers-and-hacking}

### Types of Hacker

| Type | Description |
|------|-------------|
| **White Hat Hacker** | Ethical security expert who protects systems legally |
| **Black Hat Hacker** | Malicious attacker who exploits systems for personal gain |
| **Grey Hat Hacker** | Mix of ethical and unethical hacking without permission |
| **Script Kiddie** | Beginner hacker using pre-made tools without deep knowledge |
| **Hacktivist** | Hacker driven by political or social causes |
| **State-Sponsored Hacker** | Government-backed hacker for cyber warfare and espionage |
| **Cyber Terrorist Hacker** | Uses cyber attacks to spread fear and achieve political goals |

### Types of Hacking

1. **Network Hacking**
   - Target: Networks, servers
   - Example: Sniffing, DoS attacks

2. **Web Application Hacking**
   - Target: Websites & apps
   - Example: SQL Injection, XSS

3. **System Hacking**
   - Target: Operating systems
   - Example: Password cracking, privilege escalation

4. **Social Engineering**
   - Target: Humans
   - Example: Phishing, pretexting

5. **Wireless Hacking**
   - Target: Wi-Fi networks
   - Example: WPA cracking, rogue access points

6. **Malware Attacks**
   - Target: Devices via malicious software
   - Example: Ransomware, Trojans

### Consequences of Hacking in Corporate Sector {#consequences}

Hacking can severely impact organizations:

- **Financial Loss**
  - Theft of funds
  - Cost of recovery, legal fees, fines

- **Data Breach**
  - Exposure of customer data, intellectual property
  - Compliance violations (GDPR, HIPAA)

- **Reputation Damage**
  - Loss of customer trust
  - Negative media coverage

- **Operational Disruption**
  - Systems downtime
  - Business interruption (e.g., ransomware)

- **Legal Consequences**
  - Lawsuits from customers/partners
  - Regulatory penalties

- **Intellectual Property Theft**
  - Loss of trade secrets
  - Competitive disadvantage

- **Employee Impact**
  - Job loss, stress, internal distrust

---

## TOPIC 2: NETWORK SCANNING AND FOOTPRINTING {#network-scanning}

### Network Scanning via Angry IP Scanner

**What is it?**
- Tool used to scan IP ranges
- Finds active hosts and open ports
- Fast and simple network scanning

**Usage:** Identify active devices on a network

---

### Footprinting (Commands & IP Websites) {#footprinting}

**What is it?**
- Process of collecting target information
- Gathering intelligence before an attack

**Common Commands:**
- `ping` – Test connectivity to a host
- `nslookup` – Query DNS information
- `whois` – Get domain registration details
- `traceroute` – Trace path to a host

**Useful Websites:**
- ipinfo.io – IP geolocation
- geoiptool – IP location tracking
- whois.domaintools.com – Domain information

**Information Obtained:**
- IP addresses
- Location
- ISP details
- Domain information

---

### Reconnaissance via Recon-ng {#reconnaissance}

**What is it?**
- Tool for information gathering (OSINT - Open Source Intelligence)
- Uses modules to collect domains, emails, subdomains
- Automates reconnaissance process

**Uses:**
- Gather intelligence before penetration testing
- Find subdomains
- Collect email addresses

---

### Vulnerability Scanning using Nmap {#vulnerability-scanning}

**What is it?**
- Tool for network scanning & security analysis
- Finds open ports, services, vulnerabilities
- Uses scripts (--script vuln) for detection

**Capabilities:**
- Port scanning
- Service detection
- Vulnerability detection
- OS fingerprinting

---

## TOPIC 3: PROXY SERVER & VPN {#proxy-vpn}

### Proxy Server

**Definition:** Acts as an intermediary between user and internet

**Request Flow:** User → Proxy → Website

**Features:**
- Hides user's IP address
- No encryption (in most cases)
- Less secure

**Uses:**
- Anonymous browsing
- Bypassing restrictions
- Web testing (Burp Suite)

### VPN (Virtual Private Network)

**Definition:** Creates a secure encrypted tunnel

**Connection:** User → VPN → Internet

**Features:**
- Hides IP and encrypts data
- Highly secure
- ISP cannot see user activity

**Uses:**
- Secure browsing
- Privacy protection
- Public WiFi safety

### Key Differences

| Feature | Proxy | VPN |
|---------|-------|-----|
| Encryption | No | Yes |
| Security Level | Low | High |
| Speed | Faster | Slightly slower |
| Scope | App-level | System-wide |

### Conclusion

- **Proxy** → Basic anonymity
- **VPN** → Security + Privacy
- **VPN is more secure than proxy**

---

## TOPIC 4: TYPES OF MALWARES {#malware}

**Definition:** Malware is any software designed to harm, exploit, or gain unauthorized access to a computer system.

### Historical Context: Creeper Virus

- First computer virus (1971)
- Created by Bob Thomas
- Infected ARPANET systems (early internet)

### Types of Malware

#### 1. **Virus**
- Attaches itself to files or programs
- Spreads when infected file is executed
- Can corrupt or delete data
- Example: File-infecting virus

#### 2. **Worm**
- Self-replicating malware
- Spreads automatically over networks
- Does not need user action
- Slows down systems and networks

#### 3. **Trojan Horse**
- Disguised as legitimate software
- Tricks users into installing it
- Creates backdoor access for attackers
- Example: Fake apps, cracked software

#### 4. **Ransomware**
- Encrypts user data
- Demands payment (ransom) to unlock files
- Very dangerous for organizations
- Example: WannaCry

#### 5. **Spyware**
- Secretly monitors user activity
- Collects sensitive data (passwords, browsing habits)
- Sends data to attacker

#### 6. **Adware**
- Displays unwanted advertisements
- Tracks user behavior for marketing
- Slows down system performance

#### 7. **Keylogger**
- Records keystrokes (keyboard input)
- Steals passwords, credit card details
- Works silently in background

### Malware Summary

| Type | Purpose | Spread Method |
|------|---------|---------------|
| Virus | Corruption | File execution |
| Worm | Replication | Network |
| Trojan | Backdoor | User download |
| Ransomware | Extortion | Email/Web |
| Spyware | Surveillance | Bundled software |
| Adware | Revenue | Bundled software |
| Keylogger | Theft | Installation |

---

## TOPIC 5: TOR NETWORK {#tor}

### Definition

TOR is a privacy-focused network that allows users to browse the internet anonymously. It hides the user's identity by routing traffic through multiple servers (nodes).

### How TOR Works

Uses **onion routing** (multi-layer encryption)

**Data passes through 3 main nodes:**
1. **Entry Node** – knows your IP
2. **Relay Node** – passes data
3. **Exit Node** – sends request to internet

### Features of TOR

- Provides anonymity & privacy
- Bypasses censorship
- Access to .onion (dark web) sites
- Free and open-source

### Uses

- Secure communication
- Research and OSINT
- Bypassing restrictions
- Protecting identity (journalists, researchers)

### "Creating Identities" in TOR

**Important Notes:**
- This does NOT mean creating fake illegal identities
- It means maintaining anonymous digital presence

**Key Idea:**
- TOR helps create anonymous sessions, not fake people
- Identity = online pseudonym + hidden IP

### Conclusion

TOR is a powerful tool for privacy and anonymity. It uses multi-layer encryption to hide user identity. "Creating identities" means maintaining anonymous profiles safely, not illegal impersonation.

---

## TOPIC 6: PASSWORD ATTACKS {#password-attacks}

**Definition:** Password attacks are techniques used by attackers to steal, guess, or crack user passwords to gain unauthorized access to systems.

### Types of Password Attacks

#### 1. **Brute Force Attack**
- Tries all possible password combinations
- Uses automated tools
- Time-consuming but effective

#### 2. **Dictionary Attack**
- Uses a predefined list of common passwords
- Faster than brute force
- Example: "123456", "password"

#### 3. **Phishing Attack**
- Tricks users into giving passwords
- Uses fake emails or websites
- Example: Fake login page

#### 4. **Keylogger Attack**
- Records keyboard input
- Captures passwords secretly
- Runs in background

#### 5. **Shoulder Surfing**
- Observing someone typing password
- Done in public places

#### 6. **Credential Stuffing**
- Uses leaked usernames/passwords
- Tries them on multiple websites
- Works because people reuse passwords

#### 7. **Rainbow Table Attack**
- Uses precomputed hash tables
- Cracks encrypted passwords quickly

### Prevention Methods

- Use strong passwords (mix of letters, numbers, symbols)
- Enable 2-Factor Authentication (2FA)
- Avoid password reuse
- Use password managers
- Beware of phishing links

### Conclusion

Password attacks are common methods to break security. Strong passwords and security practices help prevent unauthorized access.

---

## TOPIC 7: DoS & DDoS ATTACKS {#dos-ddos}

### 1. DoS (Denial of Service) Attack

**Definition:** An attempt to make a system or website unavailable to users.

**How it works:**
- Flooding the server with too many requests
- Comes from a single system (attacker)

**Result:**
- Server becomes slow or crashes
- Legitimate users cannot access the service

### 2. DDoS (Distributed Denial of Service) Attack

**Definition:** Similar to DoS but more powerful, uses multiple systems.

**How it works:**
- Uses multiple systems (botnet) to attack a target
- Traffic comes from many sources at the same time

**Result:**
- Server is overloaded quickly
- Very difficult to stop

### How They Work

1. Attackers send a huge number of requests
2. Server resources (CPU, bandwidth) get exhausted
3. System becomes unavailable

### Key Differences

| Feature | DoS Attack | DDoS Attack |
|---------|-----------|------------|
| Source | Single system | Multiple systems |
| Power | Less | Very high |
| Detection | Easier | Difficult |
| Example | One attacker | Botnet (many devices) |

### Prevention Methods

- Use firewalls & IDS/IPS
- Rate limiting
- Load balancing
- Use CDN (Content Delivery Network)
- Monitor unusual traffic

### Conclusion

DoS and DDoS attacks aim to disrupt services. DDoS is more dangerous due to multiple attacking sources.

---

## TOPIC 8: SNIFFING {#sniffing}

### What is Sniffing?

**Definition:** The process of capturing and monitoring network traffic (data packets).

**Uses:**
- Analyze data flowing in a network
- Can be legitimate (for security) or malicious (for stealing data)

### How Sniffing Works

1. Data travels in the form of packets over a network
2. A sniffer tool captures these packets
3. Attacker or admin can read sensitive information:
   - Passwords
   - Emails
   - Login data

### Types of Sniffing

#### 1. **Active Sniffing**
- Used in switched networks
- Attacker interacts with network to capture data
- Techniques used:
  - ARP spoofing
  - MAC flooding
- More complex

#### 2. **Passive Sniffing**
- Used in hub-based networks
- Attacker just listens to traffic
- No interaction needed
- Easier to perform

### Prevention Methods

- Use encryption (HTTPS, VPN)
- Use secure protocols (SSH instead of Telnet)
- Network security tools (IDS/IPS)
- Avoid public WiFi

### Conclusion

Sniffing is a technique to capture network traffic. It can be useful for security or dangerous if misused. Proper security measures can prevent data theft.

---

## TOPIC 9: KALI LINUX & METASPLOIT {#kali-metasploit}

### Kali Linux

**Definition:** A Debian-based Linux distribution used for penetration testing and security auditing.

**Developer:** Offensive Security

#### Features

- Comes with 600+ security tools pre-installed
- Open-source and free
- Supports wireless attacks, web testing, forensics
- Regular updates

#### Common Tools in Kali

| Tool | Purpose |
|------|---------|
| Nmap | Network scanning |
| Wireshark | Packet analysis |
| Burp Suite | Web testing |
| Metasploit | Exploitation |

#### Uses

- Ethical hacking
- Vulnerability assessment
- Digital forensics
- Security research

### Metasploit Framework

**Definition:** A powerful penetration testing framework used to find, exploit, and validate vulnerabilities.

#### Components

| Component | Description |
|-----------|-------------|
| **Exploit** | Code to take advantage of vulnerability |
| **Payload** | Code executed after exploitation |
| **Auxiliary** | Scanning and other functions |
| **Encoder** | Evades detection |

#### Types of Payloads

- **Singles** – Independent payload
- **Staged** – Sent in parts (more flexible)

#### Uses

- Exploiting system vulnerabilities
- Testing security of networks
- Gaining access (for ethical testing)
- Post-exploitation activities

### Conclusion

Kali Linux is a complete platform for security testing. Metasploit is one of its most powerful tools for exploitation. Both are widely used in ethical hacking and cybersecurity.

---

## CONCLUSION {#conclusion}

This minor project provided practical understanding of cybersecurity concepts, tools, and techniques. It helped in learning how attackers exploit vulnerabilities and how organizations can protect systems.

All activities were performed in a controlled lab environment for educational purposes only.

---

## REFERENCES

- Kali Linux Official Documentation
- OWASP Top 10 Security Guide
- Nmap Documentation
- Metasploit Framework Guide
- Cyber Security Academic Materials
