SECURITY THREAT IDENTIFICATION REPORT 
Internship Platform: Internpe 
Task Name: Security Threat Identi ication 
Student Name: SOWBHAGYA TADI 
Tools Used: VirtualBox, Metasploitable, Nmap, Wireshark 
Date: 27 / 01 / 2026 
INTRODUCTION 
The objective of this task is to analyze and identify potential security threats 
in a simulated environment. A vulnerable operating system (Metasploitable) 
was installed using VirtualBox to the main goal of this task is to understand how 
attackers identify open ports. Tools like Nmap and Wireshark were used to 
perform network scanning , capture traffic , and analyze potential 
vulnerabilities. 
This exercise provides practical experience in cybersecurity and helps in 
understanding  
how to protect systems against unauthorized access, malicious attacks, and data 
breaches. 
TOOLS USED  
1. VirtualBox – Used to create a virtual environment. 
2. Metasploitable – A vulnerable Linux-based operating system. 
3. Nmap – Used for network scanning and identifying open ports. 
4. Wireshark – Used to capture and analyze network traffic. 
ENVIRONMENT SETUP 
 
VirtualBox was installed on the host system and Metasploitable was configured 
as a virtual machine. The network adapter was set to Bridged Adapter/NAT 
to allow communication between the host machine and the virtual machine. 
 
 
 
 
 
 
 
  
  
NMAP SCANNING AND RESULT 
Nmap was used to scan the Metasploitable machine to identify open ports and 
running services. The following command was used: 
nmap 192.168.56.101 
Identified Open Ports and Services:
21 – FTP 
22 – SSH 
23 – Telnet 
25 – SMTP 
80 – HTTP 
139 – NetBIOS 
445 – SMB 
3306 – MySQL 
5432 – PostgreSQL 
5900 – VNC 
WIRESHARK TRAFFIC ANALYSIS 
Wireshark was used to capture live network traffic between the host system 
and the Metasploitable machine. Packets such as ICMP, TCP, and HTTP were 
observed. This analysis helps in identifying unauthorized access attempts 
and unusual network behaviour. 
IDENTIFIED SECURITY THREATS 
1. Multiple open ports increase the attack surface. 
2. Insecure services like FTP and Telnet transmit data without encryption. 
3. Open database ports may allow unauthorized data access. 
4. Lack of firewall protection makes the system vulnerable. 
OBSERVATIONS 
1. Multiple types of packets were observed including TCP, UDP, ICMP, and 
HTTP. 
2. Packets were exchanged between the host system and the Metasploitable 
virtual machine. 
3. Open ports identified by Nmap such as FTP (21), SSH (22), and HTTP (80) 
showed corresponding network activity. 
4. Unencrypted protocols like FTP and Telnet were observed, indicating 
potential for sensitive data exposure. 
5. Traffic flow was consistent with scanning and browsing activity, 
demonstrating normal and test-generated network communication. 
CONCLUSION 
This task provided practical knowledge of how security threats can be 
identified in a vulnerable environment. 
By using tools like Nmap and Wireshark, it is possible to analyze      
network vulnerabilities and take appropriate security measures to 
protect systems.
Nmap 192.168.56.101
**Identified Open Ports and Services:**

- 21 – FTP  
- 22 – SSH  
- 23 – Telnet  
- 25 – SMTP  
- 80 – HTTP  
- 139 – NetBIOS  
- 445 – SMB  
- 3306 – MySQL  
- 5432 – PostgreSQL  
- 5900 – VNC  

---

## WIRESHARK TRAFFIC ANALYSIS

Wireshark was used to capture live network traffic between the host system
and the Metasploitable machine. Packets such as ICMP, TCP, and HTTP were
observed.

This analysis helps in identifying unauthorized access attempts and
unusual network behavior.

---

## IDENTIFIED SECURITY THREATS

1. Multiple open ports increase the attack surface  
2. Insecure services like FTP and Telnet transmit data without encryption  
3. Open database ports may allow unauthorized data access  
4. Lack of firewall protection makes the system vulnerable  

---

## OBSERVATIONS

1. Multiple packet types such as TCP, UDP, ICMP, and HTTP were observed  
2. Traffic was exchanged between host and Metasploitable VM  
3. Open ports identified by Nmap showed corresponding network activity  
4. Unencrypted protocols like FTP and Telnet were observed  
5. Traffic pattern matched scanning and testing activity  

---

## SCREENSHOTS

![Nmap Scan](images/nmap_scan.png)  
![Wireshark Capture](images/wireshark.png)  
![Metasploitable VM](images/metasploitable.png)  

---

## CONCLUSION

This task provided practical knowledge of identifying security threats
in a vulnerable environment.

By using tools like Nmap and Wireshark, network vulnerabilities can be
analyzed and appropriate security measures can be implemented to
protect systems.
