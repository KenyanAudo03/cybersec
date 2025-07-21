# Chapter 3: Networking Basics

## Commands Practiced

- `ping` – Test basic connectivity  
- `tracert` – Trace the route to a destination  
- `nslookup` – Query DNS records  
- `whois` – Get domain registration info  
- `nmap -sn` – Scan for live hosts  
- TCP vs UDP – Connection-oriented vs connectionless  
- Common ports – 80, 443, 22, 53, 3389, etc.  
- IP, MAC, DNS – Core network identifiers

## Practice Summary

### ✔️ Tested Network Connectivity
- Used `ping` to test access to websites and internal hosts.
- Noted packet loss and latency to spot potential issues.

### ✔️ Traced Network Routes
- Ran `tracert` to map the path from local machine to remote servers.
- Observed where delays or hops dropped off.

### ✔️ DNS and Domain Lookups
- Used `nslookup` to get IPs for domains and check DNS behavior.
- Ran `whois` (online or CLI tool) to view domain ownership and status.

### ✔️ Scanned the Network
- Ran `nmap -sn 192.168.1.0/24` to find active devices on the local subnet.
- Identified IP and MAC addresses of known devices.

### ✔️ Reviewed Networking Concepts
- Practiced identifying IP and MAC addresses.
- Compared TCP and UDP behaviors.
- Noted how ports map to services and how firewalls or NAT can affect traffic.

## Example Commands Used

```cmd
ping 8.8.8.8
tracert google.com
nslookup example.com
nmap -sn 192.168.1.0/24
```

## Notes

- `ping` is the go-to for quick checks, but firewalls can block it.
- `tracert` helps identify where connectivity breaks down along the route.
- `nslookup` is useful when websites won’t load—helps spot DNS issues.
- `nmap -sn` is fast and simple for finding active devices.
- Knowing common ports helps when diagnosing services (e.g. SSH on 22, RDP on 3389).
