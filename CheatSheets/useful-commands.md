# Description
This is just to track useful commands that I have used but haven't structured my folders yet in a way to sort them. So this will be random lol

### Escape rbash
```bash
# Escaping through editors vi or vim
vim

# In open vim editor
:set shell=/bin/bash
:shell

# You can also escape by using a reverse shell - More info at link below
https://www.hacknos.com/rbash-escape-rbash-restricted-shell-escape/

```
### Linux Info
```bash
# Add all bin folders to path searchsploit 
export PATH="$HOME/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:$PATH"

# Get kernel information
uname -a

# Get Linux Verison
lsb_release -a

# Search for kernel exploit
searchsploit privilege | grep -i linux | grep -i kernel | grep X.X
```
