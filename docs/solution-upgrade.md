# Update & Upgrade

To update and upgrade is one of the main task for system maintenance. Like buildings without maintenance for a long time, programs without upgrading will age faster, lose functionality until they are unavailable.

Get to know the differences between the terms **Update** and **Upgrade**([Extended reading](https://support.websoft9.com/docs/faq/tech-upgrade.html#update-vs-upgrade))
- Patching operating system is **Updating**, while Ubuntu16.04 to Ubuntu18.04 means **Upgrading**.
- MySQL5.6.25 to MySQL5.6.30 means **Updating**, yet MySQL5.6 to MySQL5.7 means **Upgrading**.

Maintenance for Ruby includes the following two tasks.

- Update system (Operating System and Runtime) 
- Upgrade Ruby

## Update System 

Run a command to complete updating the system:

``` shell
#For Ubuntu&Debian
sudo apt update && apt upgrade -y

#For Centos&Redhat
sudo yum update -y --skip-broken
```
> This deployment package is pre-configured with a scheduled task for automatic updating. If you want to remove the automatic updating, please delete the corresponding Cron.

## Upgrade Ruby

> 升级之前请确保您已经完成了服务器的镜像（快照）备份

### Patch 升级

Ruby 基于 RVM 部署，小版本的更新非常简单

```
rvm upgrade 1.9.2-p136 1.9.2-p180
rvm upgrade ree-2011.01 ree-2011-02
```

### 版本升级

例如需将 Ruby 2.5 升级到 Ruby 2.6，只需一条命令

```
rvm install 2.6
```