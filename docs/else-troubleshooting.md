# Troubleshooting

If you're having trouble with running Ruby, here is a quick guide to solve most common problems.

> Most faults about the Instance is closely related to the Instance provider, Cloud Platform. Provided you're sure the fault is caused by Cloud Platform, refer to [Cloud Platform Documentation](https://support.websoft9.com/docs/faq/tech-instance.html).

#### How can I check the error logs?

You can find the keywords **Failed** or **error** from the logs directory: `/data/logs`

#### Can't start MySQL service?

Insufficient disk space and memory, incorrect configuration file may cause the failure to start the service. 

It is recommended to first check through the command.

```shell
# restart MySQL service
systemctl status mysql
journalctl -u mysql

# view disk space
df -lh

# view memory rate
free -lh
```

#### /urs/bin 目录下找不到 gem, ruby 等可执行文件或链接？

本项目通过 RVM 安装，通过 `source /etc/profile.d/rvm.sh` 实现 gem, ruby 等命令的全局化。