# SQL 
## ON WSL
### INSTALATION
```
sudo apt update
sudo apt install mysql-server mysql-client
```
### START SERVER
```
sudo service mysql start
```
- to start sql server
- used after instalation 
- may be later if somehow got stopped
### USE SQL
- for using in command line [refer_this](https://www.w3schools.com/sql)
```
sudo mysql
```
- you may use from nodejs/php/ any means

## possible errors While Using from nodejs
### Auth mode not supported
- run this in mysql terminal
```
 ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '';
 flush privileges;
 ```
