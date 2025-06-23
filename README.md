# task-1-network-scan
🔍 Nmap TCP SYN scan on my local network to identify open ports and understand network exposure. Created as part of Cyber Security Internship Task 1.
🔍 Task 1: Network Port Scan - Cyber Security Internship

## 📌 Objective

Perform a local network port scan to identify open ports on devices in the subnet 192.168.1.0/24 using *Nmap*, and analyze potential risks.
---
## 🛠 Tools Used

- [Nmap](https://nmap.org/) - For network scanning
- [Wireshark](https://www.wireshark.org/) (optional) - For packet analysis

---

## 🧪 Steps Taken

1. Installed *Nmap* from the official site.
2. Determined local subnet as 192.168.1.0/24.
3. Executed TCP SYN scan:
   ```bash
   nmap -sS 192.168.1.0/24

   . Found active host: 192.168.1.4 with open ports:

135: Microsoft RPC

139: NetBIOS Session Service

445: Microsoft-DS Active Directory

902: VMware Server Remote Management

912: VMware Authentication Daemon



5. Saved raw scan results to results/nmap_scan




---

🔐 Security Analysis

Ports 135, 139, 445 are commonly targeted due to Windows SMB vulnerabilities (e.g., EternalBlue).

Ports 902 and 912 indicate VMware-related services, which can be a risk if exposed externally.

These ports should be monitored or firewalled if not required.
