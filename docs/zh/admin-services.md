# 服务启停

使用由Websoft9提供的 Ruby 部署方案，可能需要用到的服务如下：

### Rails

```shell
sudo systemctl start rails
sudo systemctl stop rails
sudo systemctl restart rails
sudo systemctl status rails
```

### Apache

```shell
sudo systemctl start apache
sudo systemctl stop apache
sudo systemctl restart apache
sudo systemctl status apache
```

### Nginx

```shell
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
sudo systemctl status nginx
```

### MySQL

```shell
sudo systemctl start mysql
sudo systemctl stop mysql
sudo systemctl restart mysql
sudo systemctl status mysql
```

### MongoDB

```shell
sudo systemctl start mongo
sudo systemctl stop mongo
sudo systemctl restart mongo
sudo systemctl status mongo
```

### Redis

```shell
systemctl start redis
systemctl stop redis
systemctl restart redis
systemctl status redis
```

### phpMyAdmin

```shell
sudo docker start phpmyadmin
sudo docker stop phpmyadmin
sudo docker restart phpmyadmin
sudo docker stats pgadmin
```

### Docker

```shell
sudo systemctl start docker
sudo systemctl restart docker
sudo systemctl stop docker
sudo systemctl status docker
```
