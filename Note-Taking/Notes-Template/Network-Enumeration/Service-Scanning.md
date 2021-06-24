# Active Host Service Scanning Commands



## Ports Service Scanning

```bash
#  Top-ports 250/5000 (TCP) -- Only Open 
nmap -iL active-host-list.txt --top-ports 5000 --open -oA top-5000-scan

# Top-ports 250/5000 (UDP) -- Only Open 
nmap -sU -iL active-host-list.txt --top-ports 205 --open -oA top-250-scan-udp

# Fast 1000 TCP ports used -- Disable Reverse DNS resolution/Don't Ping
nmap -iL factive-host-list.txt -T4 -n -Pn -oA fastscan-1000

# Fragmented Scan 1000 TCP -- Only Open
nmap -iL factive-host-list.txt -f --open -oA fragmented-1000
```



## Version Detection and Scripts

```bash
# Get Version/OS information with basic script test
nmap -sV -sC -O -iL active-host-list.txt -oA version-scan-large

# Get in-depth information of hosts
nmap -iL active-host-list.txt -A 

# Check for vulnerbilities against list of IPs
nmap --script vuln -iL file.txt
```

