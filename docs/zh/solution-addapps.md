# 安装网站

在 Ruby Runtime 环境上安装一个网站，一般是基于已有的 Rails 环境配置。  

主要步骤包括：

```
# 安装应用包
gem install yourapp

# 基于 rails 创建应用脚手架
rail new yourapp

# 安装依赖包
cd yourapp
bundle install

# 自动配置
bin/rake ..

# 运行
rails s -b 0.0.0.0
```

## 常见问题

#### 是否可以基于现有的 rails 框架直接添加应用？

待研究

#### 不同版本的 ruby 是否都可以安装 rails？

待研究

#### 每个应用是否都有隔离环境？