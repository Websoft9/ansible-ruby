# 更新升级

网站技术日新月异，**更新升级**是维护工作之一，长时间不升级的程序，就如长时间不维护的建筑物一样，会加速老化、功能逐渐缺失直至无法使用。  

这里注意更新与升级这两词的差异（[延伸阅读](https://support.websoft9.com/docs/faq/zh/tech-upgrade.html#更新-vs-升级)），例如：
- 操作系统打个补丁常称之为**更新**，Ubuntu16.04 变更为 Ubuntu18.04，称之为**升级**
- MySQL5.6.25-->MySQL5.6.30 常称之为**更新**，MySQL5.6->MySQL5.7 称之为**升级**

Ruby 完整的更新升级包括：系统级更新（操作系统和运行环境）和 Ruby 程序升级两种类型

## 系统级更新

运行一条更新命令，即可完成系统级（包含Ruby小版本更新）更新：

``` shell
#For Ubuntu&Debian
apt update && apt upgrade -y

#For Centos&Redhat
yum update -y --skip-broken
```
> 本部署包已预配置一个用于自动更新的计划任务。如果希望去掉自动更新，请删除对应的Cron


## Ruby 升级

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