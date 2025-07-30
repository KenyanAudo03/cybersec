# Web Recon

---

### **dirb**

Brute-forces directories and files on websites using wordlists.

**Example:**
```bash 
dirb http://target.com /usr/share/wordlists/dirb/common.txt
```

---

### **gobuster**

Fast content discovery tool for web and DNS.

**Example (directory scan):**
```bash
gobuster dir -u http://target.com -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt
```

**Example (subdomain scan):**
```bash
gobuster dns -d example.com -w /usr/share/wordlists/subdomains.txt
```

---

### **nikto**

Scans web servers for vulnerabilities, outdated software, and dangerous files.

**Example:**
```bash
nikto -h http://target.com
```

---

### **whatweb**

Identifies technologies used by a website.

**Example:**
```bash
whatweb http://target.com
```