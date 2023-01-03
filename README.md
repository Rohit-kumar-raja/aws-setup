# aws-server-setup 

# Install apache2
```c
 sudo apt install apache2
```
# install php
```python
 sudo apt install php
```
```python
 sudo apt install php7.4 or many more versions
```
# intatll phpmyadmin
 sudo apt instal phpmyadmin

# config phpmyadmin
```htm
 sudo nano /etc/apache2/apache2.conf
``` 
 add into 
```htm
 Include /etc/phpmyadmin/apache.conf
```
# install mysql-server
```htm
sudo apt install mysql-server
```

# first connect with the mysql database 
```htm
  sudo mysql -u root -p
```

# create user for phpmyadmin or mysql database
```htm
CREATE USER username IDENTIFIED by 'password';
```

```htm
GRANT ALL PRIVILEGES ON *.* TO 'username'@'localhost';
```

```htm
FLUSH PRIVILEGES;
```

# Restart Your Server
```htm
sudo systemctl restart apache2
```
# Install FTP server
```htm
 sudo apt install vsftpd
 ```
# Create FTP Accounts
 ```htm
 sudo useradd -m testuser
```
```htm
sudo passwd testuser
```
# Configure Firewall to Allow FTP Traffic
```htm
sudo ufw allow 20/tcp
sudo ufw allow 21/tcp
```
# Configuring and Securing Ubuntu vsftpd Server
# Change Default Directory
```htm
sudo mkdir /srv/ftp/new_location
sudo usermod -d /srv/ftp/new_location ftp
```
# Restart the vsftpd service to apply the changes:

```htm
sudo service vsftpd restart
```
# Authenticate FTP Users
```html
sudo nano /etc/vsftpd.conf
```
Find the entry labeled write_enable=NO, and change the value to “YES.”
```html
sudo systemctl restart vsftpd.service
```
