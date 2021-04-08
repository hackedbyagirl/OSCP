# Initial Intelligence Gathering
Initial intel gathering through port scanning, banner gathering, etc. 

## Host Scanning: nmap 

```bash
# Fast simple scan
nmap 10.11.1.111

# Nmap ultra fast
nmap 10.11.1.111 --max-retries 1 --min-rate 1000

# Get open ports
nmap -p - -Pn -n 10.10.10.10

# Get sV from ports
nmap -pXX,XX,XX,XX,XX -Pn -sV -n 10.10.10.10

# Full complete slow scan with output
nmap -v -A -p- -Pn --script vuln -oA full 10.11.1.111

# Network filtering evasion
nmap --source-port 53 -p 5555 10.11.1.111
    # If work, set IPTABLES to bind this port
    iptables -t nat -A POSTROUTING -d 10.11.1.111 -p tcp -j SNAT --to :53

# Scan for UDP
nmap 10.11.1.111 -sU
nmap -sU -F -Pn -v -d -sC -sV --open --reason -T5 10.11.1.111

# With naabu   
naabu -top-ports 1000 -silent -exclude-cdn -nmap-cli 'nmap -sV --min-rate 40000 -T4 --open --max-retries 2 -oN -' 10.10.10.10
```

## Domain Enum

### DNSRecon

```bash
dnsrecon -d www.example.com -a 
dnsrecon -d www.example.com -t axfr
dnsrecon -d 
dnsrecon -d www.example.com -D  -t brt
```

### DIG

```bash
dig www.example.com + short
dig www.example.com MX
dig www.example.com NS
dig www.example.com> SOA
dig www.example.com ANY +noall +answer
dig -x www.example.com
dig -4 www.example.com (For IPv4)
dig -6 www.example.com (For IPv6)
dig www.example.com mx +noall +answer example.com ns +noall +answer
dig -t AXFR www.example.com
dig axfr @10.11.1.111 example.box
```

### DNSEnum

```bash
# dnsenum
dnsenum 10.11.1.111
```

## Packet Scanning

### tcpdump

```bash
tcpdump -i eth0
tcpdump -c -i eth0
tcpdump -A -i eth0
tcpdump -w 0001.pcap -i eth0
tcpdump -r 0001.pcap
tcpdump -n -i eth0
tcpdump -i eth0 port 22
tcpdump -i eth0 -src 172.21.10.X
tcpdump -i eth0 -dst 172.21.10.X

# Online service
https://packettotal.com/
```

## Packet strings analyzer

```bash
# https://github.com/lgandx/PCredz
./Pcredz -f file-to-parse.pcap
./Pcredz -d /tmp/pcap-directory-to-parse/
./Pcredz -i eth0 -v
```



