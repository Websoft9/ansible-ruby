# FAQ

#### Ruby 体系中 Gem, Bundler, Rake, Rails 是什么？

- RubyGems 是 Ruby 的包管理工具，类似 Python 中的 pip
- Gems 是 Ruby 通过 RubyGems 安装的包，为例避免误解，建议用“包”这个名字替代
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

#### Ruby 是否支持多版本？

Ruby 的多版本管理非常灵活。

* RVM 支持多个 Ruby 版本安装和切换（包括默认设置）
* 每个 Ruby 版本下，都可以通过 gem 安装同一个包的多个版本（参考 [Rails 多版本](/zh/solution-rails.md#多版本)）

#### Rails 如何才能被外网访问？

```text
rails s -b 0.0.0.0
```

#### 本项目中 Ruby 采用何种安装方式？

采用 rvm 安装，支持多版本

#### 推荐 Ruby 的学习资源？

[Awesome Ruby](https://github.com/chendelin1982/awesome-ruby)

#### If there is no domain name, can I deploy Ruby?

Yes, access Ruby by *http://Server's Internet IP:8161*.

#### What is the password for the database root user?

The password is stored in the server related file `/credentials/password.txt`.

#### Is there a web-base GUI database management tool?

Yes, phpMyAdmin is included. Visit by *http://Server's Internet IP:9090*.

#### Is it possible to modify the source path of Ruby?

No.

#### How to change the permissions of filesystem?

Change owner(group) or permissions as below:

```shell
chown -R apache.apache /data/wwwroot
find /data/wwwroot -type d -exec chmod 750 {} \;
find /data/wwwroot -type f -exec chmod 640 {} \;
```

#### What's the difference between Deployment and Installation?

- Deployment is a process of installing and configuring a series of software to the server in a different order, which is a complex system engineering.  
- Installation is the process of starting the initial wizard after the application is prepared.  
- Installation is simpler than deployment. 

#### What's Cloud Platform?

Cloud platform refers to platform manufacturers that provide cloud computing services, such as: **Azure, AWS, Alibaba Cloud, HUAWEI CLOUD, Tencent Cloud**, etc.

#### What is the difference between Instance, Cloud Server, Virtual Machine, ECS, EC2, CVM, and VM?

No difference. All refer to cloud servers. They are the different terminology used by manufacturers.
