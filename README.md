# bastille-phpmyadmin
Bastille Template for phpMyAdmin

## Configuration

## Setup MariaDB
To access MariaDb via phpMyAdmin you need to add the access rights for user `root` (could be a security issue) or another users with extensive rights on the server directly.
Log on at the server and grant the authorizations:
```sh
mysql -u root -p
CREATE USER 'local'@'localhost' IDENTIFIED BY 'Pass_Phrase';
GRANT ALL PRIVILEGES ON *.* TO 'local'@'localhost' WITH GRANT OPTION;
FLUSH PRIVILEGES;
SHOW GRANTS FOR 'local'@'localhost';
```
Replace `local` with a good user name and `localhost` with your host of phpMyAdmin, see `/etc/hosts` and use a strong password instead of `Pass_Phrasae`.
