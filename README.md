## 🛡️ 6-Week Cybersecurity Lab Plan

### Week 1: Core Network & OS Skills
- **Linux**: `ls`, `cd`, `cp`, `chmod`, `ps`, `netstat`, `iptables`, `journalctl`
- **Windows**: `ipconfig`, `tasklist`, `net user`, PowerShell, Event Viewer basics  
- **Networking**: `ping`, `traceroute`, `nslookup`, `whois`, `nmap -sn`; IP, MAC, DNS, ports, TCP/UDP  
- **Practice**: Set up VMs (Kali, Ubuntu, Win10) and scan them using Nmap.

### Week 2: Vulnerability Scanning & Recon
- **Tools**: Nmap (`-sV`, `-O`, `-A`, `--script`), theHarvester, whois, dig, dnsenum  
- **Web Recon**: dirb, gobuster, nikto, whatweb  
- **Practice**: Run recon and scans on local and TryHackMe machines.

### Week 3: Exploitation & Gaining Access
- **Metasploit**: Scan, choose payloads, exploit  
- **Targets**: FTP, SMB, outdated apps  
- **Web Exploits**: Try basic XSS, SQLi  
- **Practice**: Rooms like *Metasploit*, *Vulnversity*, *OWASP Top 10*

### Week 4: Privilege Escalation
- **Linux**: Sudo misconfigs, SUIDs, kernel exploits  
- **Windows**: Registry issues, weak services, token abuse  
- **Tools**: LinPEAS, WinPEAS, PowerUp, Seatbelt  
- **Practice**: TryHackMe *Linux PrivEsc*, *Windows PrivEsc*

### Week 5: Defenses, Hardening & Monitoring
- **Logs**: `/var/log/auth.log`, Event Viewer  
- **Basic SIEM**: Wazuh or TryHackMe labs  
- **Defenses**: UFW, Defender, Auditd, FIM, account lockouts  
- **Practice**: Harden SSH, monitor attacks in real time

### Week 6: Real-World Scenarios
- **CTFs**: TryHackMe or Hack The Box  
- **Simulate**: 
  - Attack from Kali  
  - Defend on Ubuntu/Windows (logs, blocks, patches)  
- **Projects**: 
  - Write a short report (findings, exploits, fixes)  
  - Document post-exploitation hardening steps
