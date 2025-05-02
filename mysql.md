
### Create a MySql DB and User 

```
CREATE DATABASE $MAINDB;

CREATE DATABASE ${MAINDB} /*\!40100 DEFAULT CHARACTER SET utf8 */;
CREATE USER ${MAINDB}@localhost IDENTIFIED BY '${PASSWDDB}';
GRANT ALL PRIVILEGES ON ${MAINDB}.* TO '${MAINDB}'@'localhost';
FLUSH PRIVILEGES;

CREATE DATABASE shopware_dev;
CREATE USER shopware@localhost IDENTIFIED BY 'Shopware@123';
GRANT ALL PRIVILEGES ON shopware_dev.* TO shopware@'localhost';

```

( Bash )
https://raw.githubusercontent.com/saadismail/useful-bash-scripts/master/db.sh

#### Other MySql Commands
SELECT user,host FROM mysql.user;

