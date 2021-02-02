# &
& 表示任务后台执行  
&& 表示前一条命令执行成功再执行后一条  
| 管道  
|| 前一条失败后执行  
\> 正常信息重定向  
&> 错误信息和正常信息都重定向  

# java
```bash
# 切换jdk版本
sudo update-alternatives --config java
sudo update-alternatives --config javac
```