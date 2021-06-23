# Potential Vulnerable Hosts 
Decription: Track high-level IPs that I think might be vulnerable - mainly taken from what I see when I am doing enumeration/service scanning.

|     IP      |  Port  |   Version    |          Notes/Observations          |
| :---------: | :----: | :----------: | :----------------------------------: |
| 10.XX.XX.XX | ftp/21 | vsftpd 1.1.3 | Outdated software/Anon login allowed |
| 10.XX.XX.XX | smb/445/139 | - | Identified RCE exploit using seachsploit |
| 10.XX.XX.XX | ssh/22 | openssh 2.0 | Outdated software/Need to look for potential exploits |
