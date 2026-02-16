# INCIDENT RESPONSE REPORT – SIMULATED MALWARE ATTACK

**Prepared By:** SOWBHAGYA TADI  
**Date:** 14/02/2026  
**Internship Domain:** Cybersecurity  
**Tools Used:** Kali Linux, Metasploitable, Wireshark, Nmap, Cyber Kill Chain, MITRE ATT&CK, Snort  

---

## 1. Executive Summary

This report documents a simulated cybersecurity incident conducted in a controlled lab environment.  
A port scan and unauthorized SSH login attempt were simulated using Kali Linux against a vulnerable system.

The attack was detected using system logs, Wireshark, and Snort IDS.  
The threat was successfully contained and eradicated.

---

## 2. Incident Description

A simulated unauthorized login attempt was performed using a test account.  
Authentication failures were observed in `/var/log/auth.log`.

Network traffic between Kali (192.168.56.103) and Metasploitable (192.168.56.101) was analyzed using Wireshark.  
ICMP echo requests and destination unreachable packets confirmed active communication.

**Incident Name:** Simulated Unauthorized Login Attempt & Network Activity Detection  
**Date/Time of Discovery:** 13 February 2026, 16:05  

**Detected By:**
- Syslog Monitoring (`/var/log/auth.log`)
- Wireshark Network Analysis
- Snort IDS
- Process Monitoring (`ps aux`)

---

## 3. Indicators of Compromise (IOC)

| IOC Type | Details |
|----------|---------|
| Suspicious IP | 192.168.56.101 |
| File | /usr/bin/appid_detector_builder.sh |
| MD5 | 2115ba220e255b28ca1a58e93ed69f5c |
| SHA-256 | d72712d5b70e36e05c43a09d4522fef67fa5e2fcc7e03a7c684f117747c9f952 |
| Open Ports | SSH (22), HTTP (80) |
| Log Evidence | Multiple failed login attempts |

---

## 4. Detection & Response Timeline

| Time | Details |
|------|---------|
| 04:02 PM | FAILED SU (to testuser) kali on pts/2 |
| 04:22 PM | Authentication failure logname=kali euid=0 |
| 04:24 PM | FAILED SU (to testuser) kali on pts/2 |

---

## 5. Containment and Eradication Actions

### Network Isolation
Command used:
sudo ifconfig eth0 down
Verification:
ifconfig
### Removed Malicious File
sha256sum malware.sh rm malware.sh
### Patched System
sudo apt update && sudo apt upgrade -y
### Changed Passwords
passwd msfadmin
---

## 6. Root Cause Analysis

**Cause:** Weak SSH password allowed brute-force attempts.  
No MFA or account lockout mechanism was implemented.

**Impact:**  
Simulated unauthorized access and potential data exposure.

---

## 7. Lessons Learned

- Implement strong password policies  
- Enable IDS/IPS tools like Snort  
- Regular vulnerability scanning  
- Maintain proper logging and monitoring  
- Use MFA wherever possible  

---

## 8. Conclusion

The simulated incident demonstrated how unauthorized login attempts and suspicious activity can be detected using logs, network monitoring, and IDS tools.

Implementing stronger authentication, monitoring, and patch management significantly reduces the risk of future attacks.