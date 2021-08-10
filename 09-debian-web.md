#   DEBIAN-WEB
![screenshot0](IMG/debian-logo.png)  
___

##  Installation :
`sudo curl -fsSL https://deb.nodesource.com/setup_16.x | sudo bash - `  

`sudo apt-get -y install nodejs python3-pip apache2 libapache2-mod-php7.3 mariadb-server mariadb-client librabbitmq-dev composer php7.3 php7.3-{apcu,amqp,bcmath,bz2,common,cli,curl,dev,fpm,gd,intl,mbstring,mysql,opcache,readline,redis,xdebug,xml,yaml,zip}`  
___

##  Apache 2
`sudo nano /etc/apache2/sites-available/000-Adminer.conf`

    Listen 8080
    <VirtualHost *:8080>
        ServerAdmin USERNAME@localhost
        ServerName Adminer
        DocumentRoot /var/www/Adminer/public/
        <Directory /var/www/Adminer/public/>
            Options +Indexes +FollowSymLinks
            AllowOverride All
            Require all granted
        </Directory>
    </VirtualHost> 

`mkdir -p Documents/Adminer`  
`sudo ln -s ~/Documents/Adminer /var/www/Adminer`  
`sudo a2ensite 000-Adminer.conf`  
`sudo systemctl reload apache2`  
`sudo a2enmod rewrite`  
`sudo systemctl restart apache2`  
___

##  PHP 7.3
`sudo a2enmod proxy_fcgi setenvif`  
`sudo systemctl restart apache2`  
`sudo a2enconf php7.3-fpm`  
`sudo systemctl reload apache2`  
`sudo emacs -nw /etc/php/7.3/apache2/php.ini`

    memory_limit = 512M
    display_errors = On
    post_max_size = 16M
    upload_max_filesize = 32M
`sudo systemctl restart apache2`  
___

##  Adminer 4.8.1
`cd ~/Documents/Adminer/public`  
`wget https://www.adminer.org/latest.php`  
`mv latest.php index.php`
___

##  NodeRED
`bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)`  
`sudo systemctl enable nodered.service`
___

##  Python3.7
`cd /usr/bin`  
`sudo rm python`  
`sudo ln -s python3 python`  
`python`  