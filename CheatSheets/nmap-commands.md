# nmap commands and functions

Description: Common nmap scans that I use and common scripts to enumerate the results
***

## Scanning

```bash
# Network Host Discovery
nmap -sn -iL file-of-IPs.txt
```
## Host Discovery

```bash
# Basic Scan
nmap ipaddress

# Super Fast Scan on single IP
nmap ipaddress --max-retries 1 --min-rate 1000

# Find only open ports -- top 5000 scan (TCP)
nmap -iL file-of-IPs.txt --top-ports 5000 --open 

# Find only open ports -- top 5000 scan (UDP)
nmap -sU -iL file-of-IPs.txt --top-ports 5000 --open 

# Fragmented scan to avoid firewall
nmap -f ipaddress

# Get abunch of info on port services
nmap ipaddress -A

# Get Version/OS information
nmap -sV -O ipaddress

# Check for vulns of ip host
nmap --script=vuln ipaddress

# Check for vulnerbilities against list of IPs
nmap --script vuln -iL file.txt
```
**Note: I almost always output the results to a grepable file or output in .nmap and .gnmap using the -oA or -oG option**

## Parsing .gnmap files

```bash
# Parsing Ping Sweep Host Discovery Scan to create a list of active hosts
cat basic-discovery-scan.gnmap | awk '/Status: Up/ {print $2}' | sort -u > basic-host-list.txt


# Get Hosts with a speciically open port from open port scan
cat hosts-port-scan.gnmap | awk '/22\/open/ {print $2}' | sort -u > ssh-IPs.txt
cat hosts-port-scan.gnmap | awk '/21\/open/ {print $2}' | sort -u > ftp-IPs.txt
cat hosts-port-scan.gnmap | awk '/139\/open/ || /445\/open/ {print $2}' | sort -u > samba-IPs.txt


# Create a file listing all the port numbers that are open on the network that could be used to single out specific ports
cat hosts-port-scan.gnmap |grep "Ports:"|sed -e 's/^.*Ports: //g' -e 's;/, ;\n;g'| cut -d"/" -f 1|sort -n -u TCP-Port-Listing.txt

# Create a list of domain names if domain names are listed in the scan
cat basic-host-discovery.gnmap | awk '{print $3}' | tr -d '()' | sort -u >> domain_list.txt
```

