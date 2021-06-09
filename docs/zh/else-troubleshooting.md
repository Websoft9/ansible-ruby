# 故障处理

此处收集使用 Ruby 过程中最常见的故障，供您参考

> 大部分故障与云平台密切相关，如果你可以确认故障的原因是云平台造成的，请参考[云平台文档](https://support.websoft9.com/docs/faq/zh/tech-instance.html)

#### 如何查看错误日志？

日志文件路径为：`/data/logs`。检索关键词 **Failed** 或者 **error** 查看错误

#### Ruby服务无法启动？

服务无法启动最常见的问题包括：磁盘空间不足，内存不足，配置文件错误。  
建议先通过命令进行排查  

```shell
# 查看磁盘空间
df -lh

# 查看内存使用
free -lh

# 查看服务状态和日志
systemctl status ruby
journalctl -u ruby
```

#### 通过 Ansible 无法运行 `gem install bundler` 这样的程序？

原因：有待进一步研究  
方案：通过 bash -lc 运行 gem install 命令  

```
- name: Install version {{ruby_bundle_version}} of bundler
  shell: bash -lc "gem install bundler -v {{ ruby_bundle_version }} -N"
```

#### /urs/bin 目录下找不到 gem, ruby 等可执行文件或链接？

本项目通过 RVM 安装，通过 `source /etc/profile.d/rvm.sh` 实现 gem, ruby 等命令的全局化。

