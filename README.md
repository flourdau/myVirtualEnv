#   VIRTUALSERVER
##  Sommaire :
01. [Installation de VirtualBox](01-vbox-install.md)  
02. [Configuration](02-vbox-config.md)  
03. [Création d'une Machine Virtuelle](03-machine-create.md)  
04. [Configuration](04-machine-config.md)  
05. [Installation de Debian 12](05-debian-install.md)  
06. [Configuration](06-debian-config.md)  
07. [Securité](07-debian-security.md)  
08. [GUI - Graphical User Interface](08-debian-GUI.md)  
09. [Web](09-debian-web.md)  
10. [Fun](10-debian-fun.md)  


### 👋 Hello World! 🌍
Si vous souhaitez installer ou virtualiser [Debian](https://www.debian.org), je partage [mes notes](https://flourdau.github.io/VirtualServer/). :)

Durant mes formations, j’ai construit mon environnement de développement personnalisé en utilisant [VirtualBox](https://www.virtualbox.org), pour travailler avec Linux, plus précisément [Debian](https://www.debian.org), tout en conservant un système d’exploitation Windows 10 plus orienté multimédia.  

Malgré l’émergence de nouvelles technologies (CodeSpaces de GitHub, CodePen, etc.), j’ai continué la virtualisation pour plusieurs raisons :

- Contrôle total de la machine, des droits...
- Ajustement de la puissance en fonction de la machine hôte.
- Clonage rapide, sauvegarde et relance rapide de l’état de la machine virtuelle.
- Pas besoin d'être connecté

Certes, la mise en place peut être longue et nécessite une capacité de stockage importante, mais ces inconvénients ne m’ont pas dissuadé de continuer avec la virtualisation.  


Au fil des installations, j’ai pris des notes sur les processus d’installation des différents composants (pare-feu, ssh, serveur web, PHP, bases de données, GUI, éditeurs de code…). J’ai ensuite organisé et formaté ces notes pour les partager facilement.

Pour ce faire, j’ai utilisé un langage très simple : le markdown. Et pour partager ces notes, j’ai trouvé en GitHub la solution idéale. En effet, GitHub comprend le langage markdown et permet de créer très facilement un site statique.

En suivant cette procédure, il vous faudra un peu de temps, de patience & quelques connaissances de base, mais j’ai fait de mon mieux pour simplifier le processus au maximum, de faire en sorte que ce soit le plus accessible, adaptez-vous selon vos besoins. L'abus du copier/coller est recommandé.

Je vous invite à découvrir par vous-même ici : [https://flourdau.github.io/VirtualServer/](https://flourdau.github.io/VirtualServer/)

Pour installer directement Debian comme machine hôte, passez directement à la [partie 5](05-debian-install.md).  

Si vous remarquez des erreurs ou des pratiques discutables, n’hésitez pas à me le signaler. Je me ferai un plaisir d'améliorer/corriger cela.  

#VirtualBox #Debian  

### Hôte :  

    Windows 10 Home 22H2
    VirtualBox 7  

### Machine Virtuelle :
    
    Debian 12
    2 CPU
    4096Mo RAM
    NO-GUI ou GUI
    64Go HDD

[Next](01-vbox-install.md)