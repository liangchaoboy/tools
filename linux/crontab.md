## crontab

###  启动crontab 服务

- crond 是linux下用来周期性的执行某种任务或等待处理某些事件的一个守护进程

```

service crond start //启动服务
service crond stop //关闭服务
service crond restart //重启服务

OR

/etc/init.d/cron stop
/etc/init.d/cron start

```

### 命令格式

- crontab [-u user] file crontab [-u user] [ -e | -l | -r ]
- u user 用来设定某个用户的crontab服务
- file file是命令文件的名字,表示将file做为crontab的任务列表文件并载入crontab。如果在命令行中没有指定这个文件，crontab命令将接受标准输入（键盘）上键入的命令，并将它们载入crontab
- e 添加、删除或编辑crontab文件中的条目
- l 参数列出crontab文件
- r 删除crontab文件

### crontab的文件时间格式

```
1. 每分钟执行一次            
*  *  *  *  * 
2. 每隔一小时执行一次        
00  *  *  *  * 
or
* */1 * * *  (/表示频率)

3. 每小时的15和30分各执行一次 
15,45 * * * * （,表示并列）

4. 在每天上午 8- 11时中间每小时 15 ，45分各执行一次
15,45 8-11 * * * command （-表示范围）

5. 每个星期一的上午8点到11点的第3和第15分钟执行
3,15 8-11 * * 1 command

6. 每隔两天的上午8点到11点的第3和第15分钟执行
3,15 8-11 */2 * * command
```

- 有时我们创建了一个crontab，但是这个任务却无法自动执行，而手动执行这个任务却没有问题，这种情况一般是由于在crontab文件中没有配置环境变量引起的 