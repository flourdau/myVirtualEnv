#   DEBIAN-TOOLS
![screenshot0](IMG/debian-logo.png)  
___

##  TOOLS :
`sudo apt-get install -y emacs25-nox git curl`
___

##  BASH
`emacs -nw ~/.upDate`

    _IP=$(hostname -I) || true

    printf "\nYo! Nous somme le :\n"
    date
    uptime -p

    if [ "$_IP" ]; then
        printf "\nLocal IP Address : %s\n\n" "$_IP"
    fi

    sudo apt-get update -y
    sudo apt-get dist-upgrade -y
    sudo apt-get autoclean -y
    printf "\nUpdate! :)\n"

    exit 0
___

`emacs -nw  .bash_aliases`

    alias cls="clear;ls"
    alias clsa="clear;ls -lshaG"
    alias Rfresh="source ~/.bashrc"
    alias up="sudo sh ~/.upDate"
`source ~/.bashrc`
___

##  TOR (optional)
`sudo apt-get install -y tor`  
`systemctl status tor@default.service`  
`emacs -nw  /etc/tor/torrc`

    SocksPort ADRESSE_IP_SERVER:9050
    SocksPolicy accept 192.168.0.0/16
    RunAsDaemon 1
    DataDirectory /var/lib/tor

`systemctl restart tor@default.service`

***Options dans Firefox de l'Host -> Paramètre réseau (tout en bas)***  

    Hôte SOCKS : ADRESSE_IP_SERVER Port:9050
