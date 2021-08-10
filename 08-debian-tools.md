#   DEBIAN-TOOLS
![screenshot0](IMG/debian-logo.png)  
___

##  TOOLS :
`sudo apt-get install -y emacs25-nox git curl tor`
___

##  BASH
`nano .bash_aliases`

    alias cls="clear;ls"
    alias clsa="clear;ls -lshaG"
    alias Rfresh="source ~/.bashrc"
`source ~/.bashrc`
___

## TOR (optional)
`systemctl status tor@default.service`  
`nano /etc/tor/torrc`

    SocksPort ADRESSE_IP_SERVER:9050
    SocksPolicy accept 192.168.0.0/16
    RunAsDaemon 1
    DataDirectory /var/lib/tor

`systemctl restart tor@default.service`

***Options dans Firefox de l'Host -> Paramètre réseau (tout en bas)***  

    Hôte SOCKS : ADRESSE_IP_SERVER Port:9050
