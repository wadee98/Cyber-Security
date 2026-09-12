# Cisco Ethical Hacker Course: Lab Write-Ups

Field notes from the Cisco Ethical Hacker course labs. Each file consolidates a topic's labs into a single reference, written in first-person narrative voice, with commands, findings, remediation, and gotchas per tool.

## Files
### [Passive Reconnaissance](./passive-reconnaissance.md)
Reconnaissance without touching the target. Covers OSINT platforms (OSINT Framework, WhatsMyName, SpiderFoot, Recon-ng), DNS lookup tools (nslookup, whois, dig, host), SSL certificate recon (browser, crt.sh), organizational and breach recon (HaveIBeenPwned, EmailHarvester, ExifTool, Wayback Machine), Shodan for internet-exposed devices, and local traffic capture with tcpdump and Wireshark

### [Active Reconnaissance](./active-reconnaissance.md)
Reconnaissance that touches the target. Covers host discovery and port scanning with Nmap (including NSE scripts like smb-enum-users and smb-enum-shares), packet crafting with Scapy (sniff, custom ICMP, TCP SYN), vulnerability scanning with Nmap Vulners and GVM (OpenVAS), SMB enumeration with enum4linux and smbclient,  sslscan for certificates recon, and web vulnerability scanning with Nikto. 

### [Attacks & Exploitation](./attacks-and-exploitation.md)
Exploitation techniques following active recon. Covers SQL injection on DVWA (full UNION-based chain from `' OR 1=1 #` through credential dump and hash cracking), on-path (MITM) attacks with Ettercap via ARP spoofing, social engineering with the Social Engineer Toolkit (SET) website cloner and credential harvester, and password cracking with Hashcat, John the Ripper.

### Final Capstone [Questions](./final-capstone/Questions.pdf) and [Solutions](./final-capstone/Solutions.md)
The CISCO Final Capstone Activity is a comprehensive hands-on assessment that evaluates skills across web application exploitation, network service enumeration, packet analysis, and security remediation. Throughout four distinct challenges, the activity covers exploiting SQL injection to recover and crack user credentials for SSH access, using Nmap script scans to uncover hidden web directories, enumerating unauthenticated SMB shares to extract sensitive files, and analyzing PCAP network traffic in Wireshark to reconstruct cleartext GET requests.


## Topics Not Yet Covered
The course covers additional topics not yet written up, including (but not limited to) pre engagement, wireless attacks, IOT security, post exploitation and reporting, and much more tools.

## Conventions

- **Voice**: First-person narrative; these are field notes, not lab transcripts.
- **Commands**: Real commands from the labs with actual flags and target IPs (`10.6.6.23`, `172.17.0.2`, `cisco.com`, `netacad.com`, `h4cker.org`).
- **Structure**: Each tool section has Purpose, Usage, Findings, Remediation, and Gotchas subsections.
- **Targets**: All scans and exploits were performed against lab-sanctioned targets in the course Kali VM. Do not replicate against systems you do not own or have written permission to test.

## Lab Topology

All active-recon and exploitation labs use the same virtual network topology:

![1104](resources/topology.png)