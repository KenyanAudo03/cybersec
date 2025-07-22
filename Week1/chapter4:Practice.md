## Practice: Setting up VMs and Scanning with Nmap

### 1. VM Setup

Set up the following virtual machines using VirtualBox:

- **Kali Linux**
- **Ubuntu**
- **Windows 10**

Each VM was assigned a static IP within a host-only or internal network to allow isolated scanning.

Example IP assignments:
- Kali: `192.168.56.10`
- Ubuntu: `192.168.56.11`
- Windows 10: `192.168.56.12`

Confirmed network connectivity with:
```bash
ping 192.168.56.11
```

### 2. Nmap Installation Check

Check that Nmap is installed and working

```bash
nmap -V
```

Output

- Nmap version 7.94 ( https://nmap.org )
- Platform: x86_64-pc-linux-gnu
- Compiled with: liblua-5.3 openssl-3.0.2 libpcre -libpcap-1.10.1 nmap-libdnet libssh2 zlib liblinear libxml


### 3. Host Discovery (Ping Scan)

Identified live hosts on the subnet:

```bash
nmap -sn 192.168.56.0/24
```

Output

- Nmap scan report for 192.168.56.10
- Host is up (0.00022s latency).
- Nmap scan report for 192.168.56.11
- Host is up (0.00019s latency).
- Nmap scan report for 192.168.56.12
- Host is up (0.00025s latency).


### 4. Port Scanning

Scanned all ports on a target VM:

```bash
nmap -p- 192.168.56.11
```

Output (example):

| Port    | State | Service |
|---------|-------|---------|
| 22/tcp  | open  | ssh     |
| 80/tcp  | open  | http    |
| 631/tcp | open  | ipp     |


### 5. Service Version Detection

Scanned to detect versions of running services:

```bash
nmap -sV 192.168.56.11
```

Output:

| Port    | State | Service | Version                                                |
|---------|-------|---------|---------------------------------------------------------|
| 22/tcp  | open  | ssh     | OpenSSH 8.2p1 Ubuntu 4ubuntu0.9 (Ubuntu Linux; protocol 2.0) |
| 80/tcp  | open  | http    | Apache httpd 2.4.41 ((Ubuntu))                          |
| 631/tcp | open  | ipp     | CUPS 2.3                                                 |



### 6. OS Detection

Attempted OS detection on the target:

```bash
nmap -O 192.168.56.11
```

Output:

- OS details: Linux 5.4 - 5.8 (Ubuntu)
- Network Distance: 1 hop


### 7. Notes

- All scans were performed from the Kali VM.

- The host-only adapter isolated the traffic from the internet, making it safe to scan.

- Scans completed successfully on all targets.

- Useful to see open ports and OS fingerprints across different OSes.

- Good practice for getting familiar with different Nmap scan types and options.


---

Summary of Nmap Commands Used

```bash 
nmap -V                  # Check Nmap version
nmap -sn [target]        # Ping scan / host discovery
nmap -p- [target]        # Full port scan
nmap -sV [target]        # Service version detection
nmap -O [target]         # OS detection
```