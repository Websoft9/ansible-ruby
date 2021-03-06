# Parameters

The Ruby deployment package contains a sequence of software (referred to as "components") required for Ruby to run. Below list the important information, the component name, installation directory path, configuration file path, port, version, etc.

## Path

This solution use Docker to deploy all service, you can run the command `docker ps` to list them  

### Ruby

本环境采用 [RVM](https://rvm.io/)预装了 Ruby 以及所需的其他软件包：[gem](https://rubygems.org/), rake, bundler 等。  

Ruby 安装目录： */usr/local/rvm/rubies/ruby-version*  
Ruby 命令命令： */usr/local/rvm/rubies/ruby-2.4.10/bin*  
RVM 安装目录： */usr/local/rvm*  
Ruby 网站目录： */data/wwwroot*  

> version 为版本号，例如：2.4.10。gem, bundler 等工具与版本强相关

### Nginx

Nginx vhost configuration file: */etc/nginx/conf.d/default.conf*    
Nginx main configuration file: */etc/nginx/nginx.conf*   
Nginx logs file: */var/log/nginx*  
Nginx rewrite rules directory: */etc/nginx/conf.d/rewrite*  
Nginx htpasswd file: */etc/nginx/.htpasswd/htpasswd.conf*  

### MySQL

MySQL installation directory: */usr/local/mysql*  
MySQL data directory: */data/mysql*  
MySQL configuration file: */etc/my.cnf*    

MySQL Web Management refer to [MySQL Management](/admin-mysql.md)

###  phpMyAdmin

phpMyAdmin is a visual MySQL management tool, is installed based on docker.  

phpMyAdmin directory：*/data/apps/phpmyadmin*  
phpMyAdmin docker compose file：*/data/apps/phpmyadmin/docker-compose.yml*  

### MongoDB

MongoDB data directory: */var/lib/mongodb*  
MongoDB Configuration File:  */etc/mongod.conf*  
MongoDB logs File:  */var/log/mongodb*  

### adminMongo

adminMongo is a visual MongoDB management tool, is installed based on docker.  

Docker root directory: */var/lib/docker*  
Docker image directory: */var/lib/docker/image*  

### Docker

Docker root directory: */var/lib/docker*  
Docker image directory: */var/lib/docker/image*   
Docker daemon.json: please create it when you need and save to to the directory */etc/docker*   

### Redis

Redis configuration file: */etc/redis.conf*  
Redis data directory: */var/lib/redis*  
Redis logs file: */var/log/redis/redis.log*

## Ports

Open or close ports by **[Security Group Setting](https://support.websoft9.com/docs/faq/tech-instance.html)** of your Cloud Server to decide whether the port can be accessed from Internet.  

You can run the cmd `netstat -tunlp` to check all related ports.  

The following are the ports you may use:

| Name | Number | Use |  Necessity |
| --- | --- | --- | --- |
| TCP | 80 | HTTP to access Ruby | Required |
| TCP | 443 | HTTPS to access Ruby | Optional |
| TCP | 3306 | Remote to access MySQL | Optional |
| TCP | 9003 | Use port to access Ruby | Optional |
| TCP | 9002 | Ruby Document Server on Docker | Optional |
| TCP | 9090 | phpMyAdmin on Docker | Optional |
| TCP | 9091 | adminMongo on Docker | Optional |

## Version

You can see the version on product pages at Marketplace. However, after being deployed to your server, the components will be updated automatically, resulting in a certain change in the version number. Therefore, run the command on the server to view the exact version number. 

```shell
# Check all components version
sudo cat /data/logs/install_version.txt

# Linux Version
lsb_release -a

# Nginx  Version
nginx -V

# Apache version
apache -v

# Docker Version
docker -v

# MySQL version
mysql -V

# MongoDB version
mongodb -V

# Ruby version
ruby -v
bundler -v
gem -v
rails -v
```