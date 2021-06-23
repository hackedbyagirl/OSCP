# Description

Establish a place to take notes regarding certain tools and information about them

***


## Seclists Intallation
Description: Seclists Installation
```bash
# For Kali Seclist Instaliation
apt -y install seclists
```


## Go 
Description: Golang installation w/ add to path

``` bash
#Installing Golang 
sudo apt install -y golang

#edit zsrhrc to set path
vim ~/.zshrc 
export GOROOT=/usr/lib/go
export GOPATH=$HOME/go
export PATH=$GOPATH/bin:$GOROOT/bin:$PATH

#reload zsh
source ~/.zshrc 
```


## Python Pip3/venv/pipx
Description: Virtual environement setup for pip(x)/venv -- mainly used for WitnessMe

```bash
#Setup and installation
sudo apt-get install python3-venv
python3 -m pip install --user pipx
python3 -m pipx ensurepath
```



