# Host Discovery Commands

## Network Host Discovery

### nmap

```bash
# Pingsweep Host Discovery - Ping Scan Only
nmap -sn -iL file-of-IPs.txt -oG basic-host-discovery-ping.gnmap

# ICMP Echo Ping Host Discovery
nmap -PE -iL file-of-IPs.txt -oG basic-host-discovery-ICMPecho.gnmap

# Traceroute Discovery
nmap -traceroute -iL file-of-IPs.txt -oA basic-host-discovery-tracert.gnmap
```



### netdiscover

```bash
# Discover IP using your network device -- Active
netdiscover -i eth1  

# Host Discovery based on subnet range -- Active
netdiscover -r  10.0.0.1/24

# Passive Host Discovery - Sniffing Only/No Sending Packets
netdiscover -i eth1  -p 

# Passive Host Discovery - Sniffing Network Traffic based on a file containing a list of IP ranges
netdiscover -p  -l filename.txt
```

