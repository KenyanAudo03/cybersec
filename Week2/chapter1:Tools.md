# Recon Tools & Practice Notes

---

## **Tools**

### **Nmap**

Nmap is used for network discovery and service enumeration.

- `-sV`: Detects service/version info on open ports.
- `-O`: OS detection.
- `-A`: Aggressive scan (includes `-O`, `-sV`, script scanning, and traceroute).
- `--script`: Runs Nmap Scripting Engine (NSE) scripts. Useful categories include `vuln`, `auth`, `exploit`.

**Example:**
```bash
nmap -A --script vuln <target>
```

--- 


### **theHarvester**

Collects emails, names, subdomains, IPs, URLs from public sources.

- `-d`: Domain.
- `-b`: Data source (e.g. google, bing, linkedin)

**Example:**
```bash
theHarvester -d youtube.com -b bing
```

---

### **whois**

Provides registration and ownership info for domains.

**Example:**
```bash
whois youtube.com
```

---

### **dig**

Used to query DNS records

- `dig youtube.com`: Standard A record lookup.
- `dig ns youtube.com`: Gets name servers.
- `dig AXFR youtube.com @ns1.youtube.com`: Attempts zone transfer.

**Example:**
```bash
dig AXFR youtube.com @ns1.youtube.com
```

---

### **dnsenum**

Automated DNS enumeration tool.

**Example:**
```bash
dnsenum youtube.com
```

**Includes**
- Subdomain brute-forcing
- Zone transfer attempts
- DNS record collection