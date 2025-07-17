# Chapter 1: Linux Basics

## Commands Practiced

- `ls` – List directory contents  
- `cd` – Change directories  
- `cp` – Copy files and directories  
- `chmod` – Change file permissions  
- `ps` – View running processes  
- `netstat` – Display network connections  
- `iptables` – Manage firewall rules  
- `journalctl` – View system logs (systemd)

## Practice Summary

### ✔️ Navigated Files and Directories
- Used `ls`, `cd`, and `cp` to explore and manage files.
- Practiced copying files between folders and checking permissions with `ls -l`.

### ✔️ Managed Permissions
- Used `chmod` to change file modes.
- Tested executable and read-only settings.

### ✔️ Process and Network Monitoring
- Used `ps aux` / `top`, `htop` to list all processes.
- Ran `netstat -tuln` to view open ports and active connections.

### ✔️ Basic Firewall Rules
- Viewed and flushed iptables rules.
- Created simple rules to allow/block specific ports.

### ✔️ Log Review
- Used `journalctl` to check system logs.
- Filtered logs by boot time and service.

## Example Commands Used

```bash
cd /home/user/test
ls -la
cp file.txt backup.txt
chmod +x script.sh
ps aux | grep ssh
netstat -tuln
sudo iptables -L
journalctl -u ssh
```

---
## Notes

- Understanding `chmod` helped clarify permission models.
- `iptables` is powerful but requires caution — it's easy to lock yourself out.
- `journalctl` is super useful for both real-time and historical log searches.
