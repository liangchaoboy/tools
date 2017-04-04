####  Linux保持SSH连接时间设置

- 打开 /etc/ssh/sshd_config 文件，找到一个参数为 ClientAliveCountMax，它是设定用户端的 SSH 连线闲置多长时间后自动终止连线的数值，单位为分钟
- 修改后保存并关闭文件，重新启动 sshd:/etc/rc.d/init.d/sshd restart
-  vim .bash_profile export TMOUT=1000000
- ssh -p port user@ip
- ssh-keygen 生成秘钥
- 重启 ssh 服务

```
　// ubuntu系统
　service ssh restart
　// debian系统
　/etc/init.d/ssh restart
```