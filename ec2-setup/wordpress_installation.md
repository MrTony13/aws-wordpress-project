# WordPress Installation (Correct Method)

IMPORTANT:
Install WordPress ONLY inside:it has to be in root which you wil use root command(sudo su)
/var/www/html  
NOT in /home or it will not work.

## 1. Change directory
cd /var/www/html

## 2. Download WordPress
sudo wget https://wordpress.org/latest.tar.gz

## 3. Extract
sudo tar -xf latest.tar.gz
sudo mv wordpress/* .

## 4. Set permissions
sudo chown -R apache:apache /var/www/html
sudo chmod -R 755 /var/www/html

## 5. Configure wp-config.php
sudo nano wp-config.php

Update:
define('DB_NAME', 'yourdbname');
define('DB_USER', 'yourdbuser');
define('DB_PASSWORD', 'yourdbpassword');
define('DB_HOST', 'your-rds-endpoint');

## 6. Restart Apache
sudo systemctl restart httpd
