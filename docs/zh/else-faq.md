# FAQ

#### Ruby 体系中 Gem, Bundler, Rake, Rails 是什么？

- Gem 是 Ruby 的包管理工具，类似 Python 中的 pip
- Bundler 是基于 Ruby 应用程序目录中的 Gemfile ，用于拉取依赖包的管理工具
- Gemfile 是 Ruby 依赖包清单文件
- Rake 是 Ruby 的构建程序，类似 Linux 中的 make
- Rails 是一个流行的 Ruby 应用程序开发框架

#### RVM 是什么？

RVM 是一个用于安装和管理多版本 Ruby 的命令行工具，虽然不是 Ruby 官方出品，但非常流行。

#### 什么是 Gemset？

Ruby RVM 允许我们为依赖项创建一个隔离的环境，这意味着 ruby，gems和irb都是独立的，与系统以及其他环境独立。如果你对 Python 非常熟悉，那么 RVM Gemset 就类似于 Python3 中的 VENV 或者 Python 2 中的 Virtualenv。RVM为每个Ruby版本和 gemset 提供了一个单独的 gem 目录。

#### Ruby 体系中有哪些常用的应用程序服务器？

WEBrick, passenger, Puma 等

#### Rails 如何才能被外网访问？

```text
rails s -b 0.0.0.0
```

#### 本项目中 Ruby 采用何种安装方式？

采用 rvm 安装，支持多版本

#### 推荐 Ruby 的学习资源？

[Awesome Ruby](https://github.com/chendelin1982/awesome-ruby)

#### 如果没有域名是否可以部署 Ruby 程序？

可以，访问`http://服务器公网IP` 即可

#### 数据库 root 用户对应的密码是多少？

密码存放在服务器相关文件中：`/credentials/password.txt`

#### 是否有可视化的数据库管理工具？

有，内置phpMyAdmin，访问地址：*http://服务器公网IP:9090*

#### 如何禁止外界访问phpMyAdmin？

连接服务器，编辑 [phpMyAdmin 配置文件](/zh/stack-components.md#phpmyadmin)，将其中的 `Require all granted` 更改为 `Require ip 192.160.1.0`，然后重启 Apache 服务

#### 是否可以修改Ruby的源码路径？

不可以

#### 如何修改上传的文件权限?

```shell
# 拥有者
chown -R apache.apache /data/wwwroot/
# 读写执行权限
find /data/wwwroot/ -type d -exec chmod 750 {} \;
find /data/wwwroot/ -type f -exec chmod 640 {} \;
```

#### 部署和安装有什么区别？

部署是将一序列软件按照不同顺序，先后安装并配置到服务器的过程，是一个复杂的系统工程。  
安装是将单一的软件拷贝到服务器之后，启动安装向导完成初始化配置的过程。  
安装相对于部署来说更简单一些。 

#### 云平台是什么意思？

云平台指提供云计算服务的平台厂家，例如：Azure,AWS,阿里云,华为云,腾讯云等

#### 实例，云服务器，虚拟机，ECS，EC2，CVM，VM有什么区别？

没有区别，只是不同厂家所采用的专业术语，实际上都是云服务器