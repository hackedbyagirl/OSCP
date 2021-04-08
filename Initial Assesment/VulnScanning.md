# Vulnerability Scanning

## Vulnerability Analysis
Basic intel gathering that includes port and vulnerability scans. This can be done via manual scanning or automated scanning. Scanning can include:
* ports
* internet scanning
* internal Scanning 
* authenticated scanning
* unauthenticated scanning

### Common Vuln Scanning Tools - Overview:
Vulnerability scanning tools assist with finding vulnerabilites. Scanners detect and classify system weaknesses to prioritze fixes and sometimes predict the effectiveness of countermeasures. Vuln identifies vulnerabilities, it does not exploit them. However, finding weakness provides info to determine your attack vector. Common tools include:

**Burp:** Web Vuln scanner. 

**Nessus:** Configurable scanner to meet needs. This can include OS scanning, port scanning, compliance, etc. This tool is software based. 

**Nikto:** Web Vuln scanner used to test a Web Site, Virtual Host and Web Server for known security vulnerabilities and mis-configurations. Tests for security vulnerabilities and mis-configured web servers. This tool is noisy. 

**Nmap:** Port scanner to help identify network weaknesses. It finds open ports on internet-facing systems, and it provides an accurate port status for servers, firewalls, and network perimeters. CLI commands. 

**ZAP:** This security tool helps you detect top security threats highlighted by OWASP. Some of those vulnerabilities include SQL injection, broken access control, cross-site scripting (XSS), under-protected APIs, and cross-site request forgery

* *Note: Remember to ensure you are abiding by the OSCP guidelines and using approved scanners.* * 
