# Structure
* **Cheatsheets:** Tracks common commands used for specific tools (nmap/burpsuite/etc) and resources on common topics. 
* **Checklists:** Contains checklists for certain stages of the pentest (Ex. Web Assessment, FTP assessment, Privilege Escalation, etc.)
* **Environment and Tools:** Contains environment setup configuration commands/notes I use on new vms and commands/notes for installing useful pentesting tools.
* ***Note-Taking:** Contains the file structure/outline I use for taking notes throughout the pentesting phase. I use this for OSCP note taking and my real world Pentration Testing job. **This also contains checklists and commands**

*Note: This repository is under active development so these files are not complete and will updated frequently*
***

## Goals:
* List resources, tools, and tactics for the OSCP exam as well as personal repository for career job
* Always accepting more links/stuff. Feel free to make a pull request. 
* Offering a perspective of OSCP methodology approach for anyone who needs ideas for their own methodology development
***

## OSCP Overview
Description: Basic information about the exam to remember. 

### Information:
The exam consists of several target machines that must be compromised. Some of the machines will require multiple exploitation steps, resulting first in low-level local access, and then in root or administrative privilege escalation. Other machines will be fully exploitable remotely. Specific instructions for each target will be located in your Exam Control Panel, which will only become available to you once your exam begins.

### Exam Restrictions:
You cannot use any of the following:
* Spoofing (IP, ARP, DNS, NBNS, etc)
* Commercial tools or services (Metasploit Pro, Burp Pro, etc.)
* Automatic exploitation tools (e.g. db_autopwn, browser_autopwn, SQLmap, SQLninja, now linpeas, etc.)
* Mass vulnerability scanners (e.g. Nessus, NeXpose, OpenVAS, Canvas, Core Impact, SAINT, etc.)
* Features in other tools that utilize either forbidden or restricted exam limitations
* Any tools that provide similar functions as those listed above
* **You are ultimately responsible for knowing what features or external utilities any chosen tool is using. The primary objective of the OSCP exam is to evaluate your skills in identifying and exploiting vulnerabilities, not in automating the process.**
* **You may however, use tools such as nmap (and scripting engine), Nikto, BurpFree, DirBuster, etc.** 

### Metasploit Restrictions:
The usage of Metasploit and the Meterpreter payload are restricted during the exam. You may only use Metasploit modules ( Auxiliary, Exploit, and Post ) or the Meterpreter payload against one single target machine of your choice.

However, you may use the following against all of the target machines:
* multi handler (aka exploit/multi/handler)
* msfvenom
* pattern_create.rb
* pattern_offset.rb

## Resources
```bash
#Official Documentation
https://help.offensive-security.com/hc/en-us/articles/360040165632
https://www.offensive-security.com/documentation/penetration-testing-with-kali.pdf
```
