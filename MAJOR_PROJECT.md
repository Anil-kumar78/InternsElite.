# INTERNSHIP MAJOR PROJECT – CYBER SECURITY

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

This is to certify that Anil Kumar (CS-T9/March-9349) has successfully completed the Cyber Security Internship under InternsElite during March 2026 – May 2026.

This project work is submitted in partial fulfillment of the requirements for the internship program.

**Mentor Signature:** Mr. Aman Guta

---

## ACKNOWLEDGEMENT

I would like to express my sincere gratitude to InternsElite for providing me the opportunity to complete this Cyber Security Internship.

I would also like to thank my mentor Mr. Aman Guta for his continuous guidance and support throughout the internship period.

This internship helped me understand real-world cybersecurity concepts and practical network security tools.

---

## TABLE OF CONTENTS

1. [Introduction](#introduction)
2. [Objectives](#objectives)
3. [Tools Used](#tools-used)
4. [Project Modules](#project-modules)
5. [Observations](#observations)
6. [Security Findings](#security-findings)
7. [Conclusion](#conclusion)
8. [References](#references)

---

## INTRODUCTION {#introduction}

Cybersecurity is the practice of protecting systems, networks, and data from digital attacks. These attacks aim to:
- Access sensitive information
- Change or destroy data
- Disrupt services

This internship focuses on understanding different types of cyber attacks and their prevention techniques in a controlled laboratory environment.

---

## OBJECTIVES {#objectives}

- To understand common cyber security attacks
- To learn penetration testing basics
- To analyze network traffic behavior
- To identify system vulnerabilities
- To study defense mechanisms

---

## TOOLS USED {#tools-used}

| Tool | Purpose |
|------|---------|
| Kali Linux | Penetration testing platform |
| Wireshark | Network packet analyzer |
| Apache Web Server | Target web server |
| Python HTTP Server | Simple server setup |
| HTTrack Website Copier | Website cloning |
| Hydra / Medusa | Password cracking |
| Hashdeep | File integrity verification |
| Nmap | Network scanning |

---

## PROJECT MODULES {#project-modules}

### Module 1: Phishing Attack via Kali Linux

#### Objective
Understand how phishing attacks work and how to defend against them.

#### Method 1: Using Zphisher

**Step 1: Get the Tool**
```bash
git clone https://github.com/htr-tech/zphisher.git
cd zphisher
bash zphisher.sh
```

**Step 2: Choose Attack Template**
- Zphisher shows options like Facebook, Instagram, Google, etc.
- Select any demo login page (for learning only)

**Step 3: Choose Hosting Method**
- Options: Localhost or Tunnel (for external access)
- For safe lab: Use Localhost / Local IP only

**Step 4: Testing in Lab**
- Open victim machine browser
- Enter generated link
- Try login with dummy credentials
- Entered credentials appear in terminal/logs

#### Method 2: Using SETOOLKIT (Social-Engineer Toolkit)

**Launch SET:**
```bash
sudo setoolkit
```

**Step 1: Social-Engineering Attacks**
- Option: 1
- Targets human psychology
- Tricks users into revealing sensitive data

**Step 2: Website Attack Vectors**
- Option: 2
- Creates fake or malicious websites
- Captures login credentials and personal data

**Step 3: Credential Harvester Attack Method**
- Option: 3
- Creates a fake login page
- Captures username and password when victim logs in

**Step 4: Site Cloner**
- Option: 2 (inside Credential Harvester)
- Clones exact look of real websites
- Makes phishing page look authentic

**Full Practical Flow:**
```
1. Open SET
2. Select: 1 → 2 → 3 → 2
3. Enter your IP address and target website URL
4. SET clones website and starts phishing server
5. Victim credentials appear in terminal
```

**Output Location:**
```
/var/www/html/
```

#### Prevention Methods
- Check URL carefully before login
- Use HTTPS instead of HTTP
- Enable 2FA (Two-Factor Authentication)
- Implement email filtering systems
- Provide user awareness training

---

### Module 2: Password Sniffing Attack

#### Objective
Capture and analyze network traffic to extract credentials.

**Lab Setup:**
- Machine 1: Accessing login forms (victim)
- Machine 2: Running Wireshark + MITM (attacker)

#### Types of Sniffing
- **Passive sniffing:** Just capturing traffic
- **Active sniffing:** Manipulating traffic

#### Vulnerable Protocols
- HTTP (not HTTPS)
- FTP
- Telnet

#### Secure Protocols (Hard to sniff)
- HTTPS
- SSH

#### Safe Practical Simulation

**Step 1: Create Simple Login Page (HTTP only)**
```bash
# Run on Kali
python3 -m http.server 8000
```

**Step 2: Open Wireshark**
```bash
# Launch Wireshark
wireshark
```

**Step 3: Filter and Observe**
```
Filter: http
```

**What You'll See:**
- HTTP packets with login form data in readable format
- Credentials visible in plaintext: `user=admin&pass=1234`

#### Observation
- Captured packets show login form data in readable form
- Credentials are visible in HTTP request payload
- No encryption is applied

#### Security Recommendations
- Always use HTTPS
- Use certificate-based encryption (TLS)
- Enable HSTS on websites
- Avoid public Wi-Fi for logins

---

### Module 3: Hash Analysis using Hashdeep

#### Objective
Verify file integrity and detect modified files.

#### What is Hashdeep?
A command-line tool that:
- Computes hashes of files
- Compares hashes with known values
- Audits files for integrity
- Supports MD5, SHA1, SHA256

#### Practical Steps

**Step 1: Create Folder and Files**
```bash
mkdir testhash
cd testhash
touch test1.txt test2.txt
```

**Step 2: Add Content to Files**
```bash
echo "hello Anil , you doing well in your cyber security session" > test1.txt
echo "hi anil , are you attent today clas" > test2.txt
```

**Step 3: Generate Hash Values**
```bash
hashdeep test1.txt
```

**Output:**
- MD5 hash
- SHA256 hash
- File name

**Step 4: Save Hash Output to File**
```bash
hashdeep test1.txt > hash_test1.txt
```

**Step 5: Perform Hash Analysis (Audit)**

**Check Same File:**
```bash
hashdeep -a -k hash_test1.txt test1.txt
```

**Output:**
```
hashdeep: Audit passed
```

#### Results
- Hash values successfully generated
- Matching file → Audit Passed
- Different file → Audit Failed

#### Conclusion
The hashdeep tool helps verify file integrity by comparing hash values. If the hash matches, the file is unchanged; otherwise, it indicates modification.

---

### Module 4: SQL Injection Testing

#### Objective
Understand SQL Injection vulnerabilities in web applications.

#### Testing Website
Altoro Mutual Test Site (vulnerable demo application)

#### How SQL Injection Works

**Normal Query:**
```sql
SELECT * FROM users WHERE username='user' AND password='pass';
```

**After Injection:**
```sql
SELECT * FROM users WHERE username='' OR 1=1 --';
```

**Result:** 
- `1=1` is always TRUE
- `--` comments out the rest
- Authentication may be bypassed

#### Payloads Used

**Classic Boolean-Based Payloads:**
```
' OR 1=1 --
' OR '1'='1' --
" OR "1"="1
```

**Common Variations:**
```
admin" --
admin" #
admin"/*
admin" or "1"="1
admin" or "1"="1"--
admin") or ("1"="1
admin") or ("1"="1"--
1234 " AND 1=0 UNION ALL SELECT "admin", "81dc9bdb52d04dc20036dbd8313ed055
```

#### Testing Observation
- If application is vulnerable:
  - Login may succeed without valid credentials
  - Error messages may reveal database info
- If secure:
  - Input is sanitized
  - Login fails

#### Prevention Techniques
- Use Prepared Statements (Parameterized Queries)
- Input validation & sanitization
- Use ORM frameworks
- Limit database permissions
- Hide error messages

#### Conclusion
SQL Injection vulnerabilities occur due to lack of input validation. Proper coding practices can prevent such attacks.

---

### Module 5: Website Cloning using HTTrack

#### Objective
Copy a website and run it in an offline environment.

#### Using GUI

**Step 1: Open HTTrack**
- Launch HTTrack Website Copier

**Step 2: Create New Project**
- Click Next
- Enter:
  - Project Name (REC Sonbhadra clone)
  - Category (optional)
  - Save path (folder)

**Step 3: Enter Website URL**
- Add the website URL you want to copy
- Example: `http://recsonbhadra.ac.in/`

**Step 4: Set Action**
- Choose: Download Website(s)

**Step 5: Start Copying**
- Click Next → Finish
- HTTrack will download:
  - HTML pages
  - CSS styles
  - Images & media
  - Create local site structure

#### How It Works
- Crawls website links
- Downloads resources
- Rewrites links for offline access

#### Limitations
- Dynamic sites (login, database) may not work fully
- Some scripts may break offline
- Database-driven content won't function

#### Important Points
- HTTrack = website mirroring tool
- Works via web crawling
- Used for:
  - Offline browsing
  - Website backup
  - Learning UI design

#### Conclusion
HTTrack was used to copy a website and store it locally. The downloaded website was successfully accessed offline using the index.html file, demonstrating how website mirroring works.

---

### Module 6: DoS Attack Simulation

#### Objective
Understand how high traffic impacts server performance.

#### What is a DoS Attack?
A Denial of Service (DoS) attack floods a system with excessive requests so that:
- It becomes slow, or
- It becomes unavailable to legitimate users

#### Types of DoS Attacks

1. **Traffic Flooding**
   - Overloads bandwidth
   - Example: SYN flood, UDP flood

2. **Application Layer Attack**
   - Targets web servers (HTTP requests)
   - Harder to detect

3. **Distributed DoS (DDoS)**
   - Multiple machines attack one target

#### Working Principle
1. Attacker sends massive number of requests
2. Server resources (CPU/RAM/network) get exhausted
3. Legitimate users cannot access the service

#### Create Web Server (Target Machine)

**Install Apache:**
```bash
sudo apt update
sudo apt install apache2 -y
```

**Start server:**
```bash
sudo systemctl start apache2
```

**Check in browser:**
```
http://<ip>
```

#### Create DoS Attacking Machine

Use tools like:
- Apache Bench (ab)
- Slowhttptest
- Hping3

#### Defense Methods
- Use firewall
- Rate limiting
- Load balancer
- CDN (like Cloudflare)
- Intrusion Detection System (IDS)

#### Important Notes
- Only test in your own lab (local network / VM)
- Never target real websites
- Keep load controlled and gradual

#### Conclusion
This experiment demonstrates how high traffic can impact server performance and helps understand DoS behavior and prevention techniques without performing harmful attacks.

---

### Module 7: Password Attack using Hydra/Medusa

#### Objective
Identify weak passwords in systems.

#### What is Password Attack?
A technique used to gain unauthorized access by trying different password combinations.

**Used in:**
- Cybersecurity testing
- Ethical hacking
- Penetration testing

#### What is Dictionary Attack?
- Uses a list of possible passwords (wordlist)
- Each password is tried one by one
- Faster than brute force

#### Tools Used

**Hydra:**
- Fast and widely used password cracking tool
- Supports many protocols: FTP, SSH, HTTP, Telnet, etc.
- Multi-threaded (fast)
- Easy syntax

**Medusa:**
- Similar to Hydra but more parallelized
- Designed for large-scale attacks
- High performance
- Modular design

#### Working Principle
1. Target system is selected
2. Service (FTP/SSH/HTTP) is identified
3. Username is chosen
4. Wordlist (dictionary) is loaded
5. Tool tries passwords one by one
6. If match found → access granted

#### Types of Password Attacks
- **Dictionary Attack** → Uses wordlist
- **Brute Force Attack** → Tries all combinations
- **Hybrid Attack** → Combination of both

#### Advantages
- Easy to perform
- Effective against weak passwords
- Automated using tools

#### Disadvantages
- Time-consuming for large wordlists
- Can be blocked by:
  - Firewalls
  - IDS/IPS
- Ineffective against strong passwords

#### Prevention Methods
- Use strong passwords
- Enable account lockout
- Use CAPTCHA
- Implement 2-Factor Authentication (2FA)
- Limit login attempts

#### Ethical Considerations
Password attacks should only be performed:
- In authorized environments
- For educational purposes
- In penetration testing with permission
- **Unauthorized attacks are illegal**

#### Conclusion
Password attacks using Hydra and Medusa help in identifying weak passwords in systems. These tools are useful for ethical hackers to improve system security.

---

## OBSERVATIONS {#observations}

### Network Observations
- Devices on the same network can observe traffic patterns
- Unencrypted communication (HTTP) exposes sensitive information
- Packet sniffing tools can capture visible data in transit

### Application Security Observations
- Web applications without input validation are vulnerable to SQL Injection
- Login forms using HTTP are insecure against interception attacks
- Poor session management increases security risks

### System Behavior Observations
- High traffic load affects server response time significantly
- System logs help in tracking abnormal activities
- Misconfigured networks can expose internal IP ranges

### Tool-Based Observations
- Wireshark effectively captures packet-level data
- Hashdeep ensures file integrity verification
- Hydra demonstrates vulnerability of weak passwords

---

## SECURITY FINDINGS {#security-findings}

### Encryption Importance
- HTTP protocol does not encrypt data
- HTTPS uses TLS encryption to protect communication
- Encryption prevents unauthorized data reading

### Password Security
- Weak passwords can be easily guessed or brute-forced
- Strong passwords include uppercase, lowercase, numbers, and symbols
- Multi-factor authentication improves security significantly

### Network Security
- Open networks are vulnerable to sniffing attacks
- Network segmentation reduces attack surface
- Firewalls help block unauthorized access

### Application Security
- Input validation is essential to prevent SQL injection
- Secure coding practices reduce vulnerabilities
- Regular security testing is required

### Monitoring & Detection
- Network monitoring tools detect suspicious activity
- Logs are important for forensic analysis
- IDS/IPS systems improve detection capability

---

## CONCLUSION {#conclusion}

This Cyber Security Internship provided practical exposure to various types of cyber attacks and defense mechanisms in a controlled lab environment.

### Key Learnings

The project helped in understanding:
- How attackers exploit insecure systems
- How data can be intercepted over networks
- Importance of encryption in communication
- Role of strong authentication systems
- Real-world behavior of security tools

### Key Learning Outcome

Cybersecurity is not only about attacking systems but also about protecting data and preventing breaches.

### Final Statement

All experiments were performed strictly in a controlled and authorized lab environment for educational and learning purposes only. No real-world systems or unauthorized networks were targeted.

---

## FUTURE SCOPE

### Future Improvements

- Implementation of AI-based intrusion detection systems
- Advanced encryption techniques for communication security
- Cloud security enhancement mechanisms
- Automated vulnerability scanning systems
- Real-time threat detection using machine learning

### Career Opportunities

- Cyber Security Analyst
- Ethical Hacker
- SOC (Security Operations Center) Analyst
- Penetration Tester
- Security Engineer
- Cloud Security Specialist
- Threat Intelligence Analyst

---

## REFERENCES {#references}

### Books
- Network Security Essentials – William Stallings
- Cybersecurity Fundamentals – ISACA Guide

### Online Resources
- [OWASP Official Website](https://owasp.org/)
- [Kali Linux Documentation](https://www.kali.org/)
- [Wireshark User Guide](https://www.wireshark.org/)
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)

### Tools Documentation
- Kali Linux Tools Repository
- Hashdeep Documentation
- Hydra Tool Manual
- Metasploit Framework Guide

---

**Document Version:** 1.0  
**Last Updated:** April 2026  
**Status:** Complete
