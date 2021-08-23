#   DEBIAN-FUN
![screenshot0](IMG/debian-logo.png)  
___

### Hostname
`sudo emacs -nw /etc/hostname`
___

### Welcome
`sudo emacs -nw /etc/motd`

    Bienvenue sur : 
    
     ##  ###  ##   # #  ###  ##    # 
    #    #    # #  # #  #    # #   # 
     #   ##   ##   # #  ##   ##    # 
      #  #    # #  # #  #    # #     
    ##   ###  # #   #   ###  # #   #                            

___

### Cmatrix
`sudo apt-get -y install cmatrix`
___

### Terminal Windows 10
***Installez l'application Terminal depuis le Store de Windows puis dans Paramètre***  

![screenshot01](IMG/10-debian-fun/01.png)  

***'Ouvrir le fichier JSON'***  
***Ajoutez le bloc dans*** _profiles->list_    
***& remplacez les champs*** _commandline, background, ico_    

    {
        "guid": "{58ad8b0c-3ef4-5f4a-sc6f-43e789f2544}",
        "hidden": false,
        "name": "VSRV",                
        "commandline" : "ssh USERNAME@IP_VM",
        "acrylicOpacity" : 0.5,
        "backgroundImage" : "ms-appdata:///Roaming/1.jpg",
        "backgroundImageOpacity" : 0.15,
        "backgroundImageStretchMode" : "uniformToFill",
        "closeOnExit" : true,
        "colorScheme" : "Campbell",
        "cursorColor" : "#FFFFFF",
        "cursorShape" : "bar",
        "fontFace" : "Consolas",
        "fontSize" : 12,
        "historySize" : 9001,
        "icon" : "ms-appdata:///Roaming/pi.png",
        "padding" : "0, 0, 0, 0",
        "snapOnInput" : true,
        "startingDirectory" : "%USERPROFILE%/",
        "useAcrylic" : true 
    },
***Attention à backgroundImage & icon❗***  
***il correspond au dossier RoamingState situé un niveau au dessus de ce fichier JSON***  
***Si error d'SSH revoir la partie securité du tuto pour se connecter avec powershell...***  

***Voilà maintenant en un click vous êtes log! : )***
___

### Et aussi n'hésitez pas à importer & créer vos variantes! : )  
![screenshot0](IMG/10-debian-fun/00.png)