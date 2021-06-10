# 更多...

下面每一个方案，都经过实践证明行之有效，希望能够对你有帮助

## 域名绑定

绑定域名的前置条件是：已经完成域名解析（登录域名控制台，增加一个A记录指向服务器公网IP）  

完成域名解析后，从服务器安全和后续维护考量，需要完成**域名绑定**：

Ruby 域名绑定操作步骤：

1. 确保域名解析已经生效  
2. 使用 SFTP 工具登录云服务器
3. 修改 [Nginx虚拟机主机配置文件](/zh/stack-components.md#nginx)，将其中的 **server_name** 项的值修改为你的域名
   ```text
   server
   {
   listen 80;
   server_name ruby.yourdomain.com;  # 此处修改为你的域名
   ...
   }
   ```
4. 保存配置文件，重启 [Nginx 服务](/zh/admin-services.md#nginx)

## 隔离环境

有两种隔离环境的解决方案：

* RVM Gemset
* Bundler

经过实验验证，bundle 可以很方便的将项目所需的软件包安装到项目目录中。  

## gem 源

rubygems.org 存放在 Amazon S3 上，有时由于网络问题导致无法安装

```
# 查询当前源，假设为：https://rubygems.org/
gem sources -l

# 删除当前源
gem sources --remove https://rubygems.org/

# 安装替换源
gem sources -a https://gems.ruby-china.com/

# 查询替换后的结果
gem sources -l

# bundle 源更换  
bundle config mirror.https://rubygems.org https://gems.ruby-china.com/
```
