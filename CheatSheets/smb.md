# SMB Enumeration Commands

## General

```bash
# Identification
nmap -139,445 <IP> -A 

# Vulnerabilities
nmap --script smb-vuln* -p 445 <IP>
```



### Hostname Enumeration

```bash
# Hostname lookup -nmblookup
nmblookup -A <IP>

#nbtscan
nbtscan <IP>


```

### Shares/Null Sessions

```bash
# smbmap
smbmap -H <IP>

# crackmapexec
crackmapexec smb 
```

