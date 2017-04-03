## tmux

- tmux list-session 列出所有回话
- tmux new -s <会话名>
- tmux attach-session -t <会话名>
- tmux rename-session -t <会话名>
- tmux choose-session -t <会话名>
- tmux kill-session -t <会话名>

## 会话

- tmux new -s  <会话名>
- C-b d 分离回话
- exit 退出回话
- C-b s 选择并切换回话


## 窗口

- C-b c 创建一个新的窗口
- C-b & 关闭窗口
- C-b w 选择窗口

## 面板

- C-b % 将当前面板分为左右两块
- C-b 方向键 选择面板
- C-b x 关闭当前面板