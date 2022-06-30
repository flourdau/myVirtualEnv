|             |             |               |
| :---        |    :----:   |          ---: |
| [Previous](05-debian-install.md)     |-----------------------------------------------------------------------------------------------------------------------------| [Next](07-debian-security.md)   |
|             |             |               |

#   DEBIAN-CONFIG
![screenshot0](IMG/debian-logo.png)  
___

### Dependances
`su -`  
![screenshot00a](IMG/06-debian-config/00a.png)  
***Insérez l'ISO de Debian***  
`apt-get install -y dkms build-essential`  
`eject`
___

### Additions
***Cliquez sur :***  
![screenshot00](IMG/06-debian-config/00.png)  
___

***Si GUI (Interface Graphique)***  
***Patientez & fermez la pop-up qui s'affiche***  
`sh /media/cdrom0/VBoxLinux*.run`  
***Si no GUI***   
`mount /dev/sr0 /media/cdrom0`  
`sh /media/cdrom0/VBoxLinux*.run`  
`eject`  

### Dossiers partagés
***ATTENTION À BIEN REMPLACER USERNAME***❗❗❗  
`usermod -aG vboxsf USERNAME`  
`shutdown -h 0`  
![screenshot00](IMG/06-debian-config/01.png) 
___

![screenshot00](IMG/06-debian-config/02.png)  
***On en profite pour activer le copier-coller...***
___

![screenshot00](IMG/06-debian-config/04.png)  
***On peut maintenant ajouter un dossier à partager***
___

![screenshot00](IMG/06-debian-config/05.png)  
***Attention, juste nommer le partage (NOM_DOSSIER_PARTAGÉ_DANS_VIRTUALBOX) mais ne rien cocher***  
___

***On relance la VM***  
`mkdir ~/partage_vm`  
`su -`  
`nano /etc/fstab`

	NOM_DOSSIER_PARTAGÉ_DANS_VIRTUALBOX	/home/USERNAME/partage_vm	vboxsf	defaults	0	0
***Ajoutez la ligne, attention aux tabulations!***
___

###	Pensez à exporter!

![screenshot85](IMG/05-debian-install/85.png)

|             |             |               |
| :---        |    :----:   |          ---: |
| [Previous](05-debian-install.md)     |-----------------------------------------------------------------------------------------------------------------------------| [Next](07-debian-security.md)   |
|             |             |               |

