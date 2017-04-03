## screen 

- screen -S yourname -> 新建一个叫yourname的session
- screen -ls -> 列出当前所有的session
- screen -r yourname -> 回到yourname这个session
- screen -R yourname -> 先试图恢复离线的作业。若找不到离线的作业，即建立新的screen作业
- screen -d -r yourname -> 结束当前session并回到yourname这个session

## 快捷键

- C-a d > detach， 暂时离开当前的session
- C-a t 显示当前时间
- C-a k 关闭当前的window

