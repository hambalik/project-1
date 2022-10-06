**PROJECT 1 DOCUMENTATION (LAMP IMPLEMENTATION)**

## Created a running ec2 instance on aws after my AWS account creation and selected a free tier, so easy.
![Running-instance](./images/Running-instance.PNG)


## Created an active github account with no hurdle experienced. 
![github-account-created](./images/github-account-created.PNG)


## I was succesfully able to connect to my created ec2 instance using window terminal following the procedures as was detailed in the PROJECT 1 instuctions/guide. I also tried to log into my created ec2 through PUTTY but to no avail after several attempts following number of video.
![Login-into-ubuntu-server-on-aws](./images/Login-into-ubuntu-server-on-aws.PNG)


## Apache was succesfully istalled, using Ubuntu's package manager "Apt" with the code shown below
`sudo apt update`
![installing-apache](./images/installing-apache.PNG)
![installation-of-apache](./images/installation-of-apache.PNG)


## Confirming the status of already installed apache 
`sudo systemctl status apache2`
![apache-status](./images/apache-status.PNG)


## Editting inbound rule to open inbound connection through port 80
![open-port-80](./images/open-port-80.PNG)


## Login into web server through ubuntu shell
`curl http://localhost:80`
![login-to-web-server](./images/login-to-web-server.PNG)
![login-to-web-server1](./images/login-to-web-server1.PNG)
![login-to-web-server3](./images/login-to-web-server3.PNG)
![login-to-web-server4](./images/login-to-web-server4.PNG)
![login-to-web-server5](./images/login-to-web-server5.PNG)
![login-to-web-server6](./images/login-to-web-server6.PNG)
![login-to-web-server7](./images/login-to-web-server7.PNG)
![login-to-web-server8](./images/login-to-web-server8.PNG)
![login-to-web-server9](./images/login-to-web-server9.PNG)
![login-to-web-server10](./images/login-to-web-server10.PNG)

## Testing how the installed Apache HTTP server can respond to requests from the Internet.Opening a web browser Using the following url:
[login-to-web-server-on-chrome](https://3.87.162.46)
![login-to-web-server-on-chrome](./images/login-to-web-server-on-chrome.PNG)g
![login-to-web-server-on-chrome1](./images/login-to-web-server-on-chrome1.PNG)

## Installation of MYSQL using 'apt'
`sudo apt install mysql-server`
![installation-of-mysql](./images/installation-of-mysql.PNG)
![installation-of-mysql1](./images/installation-of-mysql1.PNG)


## Running security script root user to create password, either low, medium or strong
`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';`
![security](./images/security.PNG)

## Then, exit MYSQL shell
`exit`
![exit-mysql1](./images/exit-mysql1.PNG)

## Starting interractive scrip
`sudo mysql_secure_installation`
![exit-mysql1](./images/exit-mysql1.PNG)
![security](./images/security.PNG)

## After finishing the above, log in to MYSQL test was carried out
`sudo mysql -p`
![sudo-mysql-p](./images/sudo-mysql-p.PNG)

## And finally exit MMYSQL console to proceed to step 3 of the project
`exit`
![exit-mysql3](./images/exit-mysql3.PNG)

## Installation of three packages of PHP, libapache2-mod-php and php-mysql
`sudo apt install php libapache2-mod-php php-mysql`
![installing-php...](./images/installing-php....PNG)

## PHP version confirmed
`php -v`
![confirming-php-installation](./images/confirming-php-installation.PNG)

## Setting up apache virtual host by firstly create directory for projectlamp
`sudo mkdir /var/www/projectlamp`
![project-LAMP-directory](./images/project-LAMP-directory.PNG)

## Creation and opening of new configuration file in Apache's site
`sudo vi /etc/apache2/sites-available/projectlamp.conf`
![final](./images/final.PNG)
![capture3](./images/capture3.PNG)

## Using ls command to show the new file in the sites-available directory
`sudo ls /etc/apache2/sites-available`
![sudo-ls](./images/sudo-ls.PNG)

## Enabling the new virtual host
`sudo a2ensite projectlamp`
![sudo-a2ensite](./images/sudo-a2ensite.PNG)

## Confirming configuration file does not contain syntax error
`sudo apache2ctl configtest`
![configtest](./images/configtest.PNG)

## Reloading apache for the change to take effect
`sudo systemctl reload apache2`
![reload-apache2](./images/reload-apache2.PNG)

## Creating an index.html file
`sudo echo 'Hello LAMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectlamp/index.html`
![hello-lamp](./images/hello-lamp.PNG)

## Surfing internet for the index.html file
[hello-LAMP,](https://44.203.53.92)
[Login-using-public-DNS](https://ec2-44-203-53-92.compute-1.amazonaws.com)
![Hello-LAMP1](./images/Hello-LAMP1.PNG)
![Login-using-public-DNS](./images/Login-using-public-DNS.PNG)

## Reloading apache for the change to take effect
`sudo systemctl reload apache2`
![reload-apache2](./images/reload-apache2.PNG)

## Changing the order in which the index.php file is listed within the DirectoryIndex directive
`sudo vim /etc/apache2/mods-enabled/dir.conf`
![sudo-vim](./images/sudo-vim.PNG)
![change-this](./images/change-this.PNG)

## Reloading apache for the change to take effect
`sudo systemctl reload apache2`
![reload-apache2](./images/reload-apache2.PNG)

## Creating a new file named index.php inside my custom web root folder
`vim /var/www/projectlamp/index.php`
![removing-project-lamp](./images/removing-project-lamp.PNG)
![saving-phpinfo](./images/saving-phpinfo.PNG)
![php-version7](./images/php-version7.PNG)
![zend-engine](./images/zend-engine.PNG)

## And finally, the fille created was removed because of the sensitive information about php environment ubuntu server it contains which can later be added
`sudo rm /var/www/projectlamp/index.php`
![sudo-rm](./images/sudo-rm.PNG)

**THE PROJECT 1 IMPLEMENTATION AND DOCUMENTATION COMPLETED**