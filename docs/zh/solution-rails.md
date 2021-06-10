# Rails

Rails 是 Ruby 生态中流行的 Web 应用程序开发框架。目的是通过解决快速开发中的共通问题，简化 Web 应用的开发。

Rails 依赖如下组件：  

* Ruby
* SQLite3
* Node.js
* Yarn

## 使用

本部署方案默认已安装 Rails，本地浏览器访问：*http://服务器公网IP地址:3000* 即可访问：  

![Ruby Rails](https://libs.websoft9.com/Websoft9/DocsPicture/zh/ruby/ruby-railsgui-websoft9.png)

## 多版本

```
# 安装 rails 5.0 和 最新版本
gem install rails --version=5.0
gem install rails

# 查询已安装的 rails
gem list | grep rails

结果：rails (6.1.3.2, 5.0.7.2, 5.0.0)

# 指定一个 rails 版本去创建项目

rails _5.0.0_ new myproject5
```

##  常见问题

#### 如何将包安装到项目目录下？

```
# 安装第三方包到项目 vendor/bundle 目录
bundle install --deployment

# 安装所有包到项目目录
bundle install --path=$(pwd)
```

#### 如何指定 RailS 应用程序的端口？

参数 -p 即指定端口号

```
rails s -p 8000
```

#### 一个 rails 框架可以部署几个应用？

有待研究。建议部署部署一个。
