#   DEBIAN-SECURITY
![screenshot0](IMG/debian-logo.png)  
___

##  SUDO
***ATTENTION À BIEN REMPLACER USERNAME IP-ADDRESS & PORT***❗❗❗  
`su -`  
`nano /etc/sudoers`  

    USERNAME ALL=(ALL:ALL) ALL

***On demande le mot de passe***  
🛑***OU INVERSEMENT***❗❗

    USERNAME ALL=(ALL) NOPASSWD: ALL

`exit`  
`sudo apt-get update -y`  
***Voilà... ...USERNAME possède les droits...***
___

##  SSHD
`sudo nano /etc/ssh/sshd_config`

    Port PORT
    ChallengeResponseAuthentication no
    UsePAM yes
    X11Forwarding yes
    PrintMotd no
    AcceptEnv LANG LC_*
    Subsystem       sftp    /usr/lib/openssh/sftp-server
    PermitRootLogin no
    AllowUsers USERNAME
`sudo systemctrl restart sshd`  
___

***Depuis la machine hote***  
`ssh-keygen`  

!!! UNIX!!!  
`ssh-copy-id -pPORT <USERNAME>@<IP-ADDRESS>`  
!!! OU POWERSHELL !!! (utile pour autolog awec l'application Terminal de Windows 10)  
`scp.exe -PPORT .\.ssh\id_rsa.pub USERNAME@IP-ADDRESS:~/.ssh/authorized_keys`  
  
`ssh -p44044 <USERNAME>@<IP-ADDRESS>`  
___

***Retour sous Debian***  
`sudo nano /etc/ssh/sshd_config`  

    PasswordAuthentication no
    UsePAM no
`sudo systemctrl restart sshd`  

##  FAIL2BAN
`sudo apt-get install -y fail2ban`  