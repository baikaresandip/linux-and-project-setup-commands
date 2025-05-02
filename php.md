# PHP

- Install the missing PHP 8.3 extensions using:
- `sudo apt install php8.3-xml php8.3-dom php8.3-simplexml php8.3-soap php8.3-amqp`
- `sudo systemctl restart php8.3-fpm`
- `sudo systemctl restart apache2`  # or nginx if using that

### ✅ 1. Check installed PHP versions

`update-alternatives --list php` OR `ls /usr/sbin/php*`

### ✅ 2. Install the target PHP-FPM version (if not already)
 `sudo apt install php8.2 php8.2-fpm`

### ✅ 3. Switch CLI PHP version (optional)
`sudo update-alternatives --config php`
### ✅ 4. Configure Apache to use the correct PHP-FPM
        If you're using Apache with php-fpm, make sure you have the correct proxy_fcgi settings.

        A. Disable the old PHP module (if any):
        `sudo a2dismod php8.1`


### Change in any of the PHP ini
`sudo nano /etc/php/8.3/fpm/php.ini`

`sudo nano /etc/php/8.3/cli/php.ini`

`sudo systemctl restart php8.3-fpm`

`sudo systemctl restart apache2`


