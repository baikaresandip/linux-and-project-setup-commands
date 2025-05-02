
## Apache Server
The Apache HTTP server is the most widely-used web server in the world. It provides many powerful features including dynamically loadable modules, robust media support, and extensive integration with other popular software.

### Installation
Apache is available within Ubuntu’s default software repositories, making it possible to install it using conventional package management tools.

Let’s begin by updating the local package index to reflect the latest upstream changes:

`sudo apt update`
`sudo apt install apache2`



Restart: `sudo systemctl restart apache2`
Start: `sudo systemctl start apache2`
Stop: `sudo systemctl stop apache2`
Reload: `sudo systemctl reload apache2`
Disable: `sudo systemctl disable apache2`
Enable: `sudo systemctl enable apache2`

port change: 
make 80 to 8080 in below files:
`sudo vim /etc/apache2/ports.conf`
`sudo vim /etc/apache2/sites-available/000-default.conf`

####  Add New site to apache
`sudo nano /etc/apache2/sites-available/your_domain.conf`

```
<VirtualHost *:80>
    ServerAdmin webmaster@localhost
    ServerName your_domain
    ServerAlias www.your_domain
    DocumentRoot /var/www/your_domain
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```
Run below commands

`sudo a2ensite your_domain.conf`
`sudo a2dissite 000-default.conf`
`sudo apache2ctl configtest`
`sudo systemctl restart apache2`

- Add Website to the Host file
- Run - `sudo vim /etc/hosts`
- Add this code
    - `127.0.0.1    www.YOURDOMAIN.com`
- Run `sudo systemctl restart apache2`


##### Bonus Tip

```
sudo add-apt-repository ppa:realpvn/easy-apache
sudo apt-get update
sudo apt-get install easy-apache

#to install Apache server
easy-apache -a

#to install SSL
easy-apache -s

#full setup, Apache and SSL
easy-apache -f

```
