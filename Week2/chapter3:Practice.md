# Practice

---

## **Local Machines**

Set up local vulnerable VMs like:

- Metasploitable
- DVWA
- Juice Shop

**Steps**

1. `nmap -sV -O <target>`
2. Web scans with `dirb` or `gobuster`
3. Run `nikto` and `whatweb` on local apps
4. Use `dig`, `dnsenum`, `whois` on local DNS setups (if configured)
   

---

## **TryHachMe Machines**

Good beginner rooms:

- `Nmap`
- `Web Fundamentals`
- `OWASP Top 10`
  
**Workflow Examples:**
```bash
nmap -sV -O <target>
gobuster dir -u http://<target> -w wordlist.txt
whatweb http://<target>
nikto -h http://<target>
```

Use `theHarvester`, `dig`, `dnsenum` for passive recon if external domains are involved.