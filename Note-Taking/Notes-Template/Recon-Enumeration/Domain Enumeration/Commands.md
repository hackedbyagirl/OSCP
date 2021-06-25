# Domain Information Gathering Commands

[toc]

***

## Server/Record Information

### dnsrecon

```bash
# Basic Scan
dnsrecon -d site.com

# Filter out brute force and wildcards
dnsrecon -d site.com -f 
```

### dnsenum

```bash
# Basic Server Information 
dnsenum site.com

# In-Depth scan
dnsenum --enum site.com
```

### dig

```bash
# Basic Scan - Find IP Address
dig site.com

# Basic Scan - Find IP Address (IPs Only)
dig site.com +short

# DNS query all record types
dig site.com ANY +noall +answer

# DNS A record search
dig site.com A

# DNS MX record search
dig site.com MX

# DNS NS record search
dig site.com NS
```

### nslookup

```bash
# Find IP Address of a host
nslookup site.com

# Reverse Lookup
nslookup <IP>
```

### whois - Registry

```bash 
# Basic Information
whois site.com

# Basic Information - IP Address
whois <IP> 
```



## Web Technology/Fingerprinting

### whatweb

```bash
# Website Technology Scan - Domain
whatweb site.com

# Website Technology Scan - IP
whatweb <IP>
```

### wafw00f - Firewall Fingerprinting

```bash
# Firewall Detection
wafw00f site.com

# Find all Firewalls Accociated
wafw00f site.com -a
```

### netcreaft

```bash
# Website
netcraft.com
```

### builtwith

```bash
# Website
builtwith.com
```

### Wappalyzer

```bash
# Webiste
wappalyzer.com
```



### Subdomain Enumeration

### amass

``` bash
# Basic Find All Subdomains
amass enum -d site.com
```



### gobuster

```bash
# Basic -- follow redirects
gobuster dir -u site.com -w /path/to/wordlist -r
```



### burpsuite

```bash
# Use burp Proffesional to spider (non-oscp)
```

