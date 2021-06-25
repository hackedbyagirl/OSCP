# FTP Checklist

- [ ] Banner Grabbing/Fingerprinting

  - [ ] Software/version

- [ ] Vulnerbility Detection

  - [ ] nmap NSE scripts
  - [ ] searchsploit
  - [ ] anonymous login
  - [ ] browser connection

- [ ] Common Credentials Testing

  - [ ] admin, administrator, root, ftpuser, test, etc. (safer than brute forcing)

- [ ] Bruteforce

  - [ ] hydra

- [ ] Packetsniffing - Wireshark

  - [ ] tcp.port==21

- [ ] Enumerate Files and Folders

  - [ ] current pwd
  - [ ] FTP directior access check
  - [ ] Files and folders have current access to
  - [ ] config files
    - [ ] ftpusers
    - [ ] ftp.conf
    - [ ] proftpd.conf

- [ ] Common command Check

  - [ ] | *?*/help                    | print local help information              |
    | --------------------------- | ----------------------------------------- |
    | *append*                    | Append to a file                          |
    | *ascii*                     | set ascii transfer type                   |
    | *binary*                    | Set Binary transfer type                  |
    | *bye/\*exit**/quit          | Terminate ftp session and exit            |
    | *cd*                        | Change remote working directory           |
    | *chmod*                     | Change file permissions of remote file    |
    | *close*/disconnect          | Terminate FTP session                     |
    | *debug*                     | toggle/set debugging mode                 |
    | *delete*/mdelete (multiple) | delete remote file                        |
    | *dir*/ls                    | list contents of remote directory         |
    | *get*/recv/mget (multiple)  | receive file                              |
    | *mkdir*                     | make directory on remote machine          |
    | *passive*                   | enter passive transfer mode               |
    | *put*/*mput* (multiple)     | send one file                             |
    | *pwd*                       | print working directory on remote machine |
    | *rename*                    | rename file                               |
    | *rmdir*                     | remove directory on remote machine        |
    | *size*                      | show size of remote file                  |
    | *type*                      | set file transfer type                    |
    | *verbose*                   | toggle verbose mode                       |

