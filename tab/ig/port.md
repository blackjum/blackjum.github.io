# 端口服务信息

> ## 常见端口列表

  端口号	      端口服务/协议简要说明	         关于端口可能的一些渗透用途
  -	tcp 20,21    ftp 默认的数据和命令传输端口[可明文亦可加密传输]  允许匿名的上传下载,爆破,嗅探,win提权,远程执行(proftpd 1.3.5),各类后门(proftpd,vsftp 2.3.4)
  -	tcp 22	ssh[数据ssl加密传输]	可根据已搜集到的信息尝试爆破,v1版本可中间人,ssh隧道及内网代理转发,文件传输,等等…常用于linux远程管理…
  -	tcp 23	telnet[明文传输]	爆破,嗅探,一般常用于路由,交换登陆,可尝试弱口令,也许会有意想不到的收获
  -	tcp 25	smtp[简单邮件传输协议,多数linux发行版可能会默认开启此服务]	邮件伪造,vrfy/expn 查询邮件用户信息,可使用smtp-user-enum工具来自动跑
  -	tcp/udp 53	dns[域名解析]	允许区域传送,dns劫持,缓存投毒,欺骗以及各种基于dns隧道的远控
  -	tcp/udp 69	tftp[简单文件传输协议,无认证]	尝试下载目标及其的各类重要配置文件
  - tcp 80-89,443,8440-8450,8080-8089	web[各种常用的web服务端口]	各种常用web服务端口,可尝试经典的top n,vpn,owa,webmail,目标oa,各类java控制台,各类服务器web管理面板,各类web中间件漏洞利用,各类web框架漏洞利用等等……
  - tcp 110	[邮局协议,可明文可密文]	可尝试爆破,嗅探
  - tcp 137,139,445	samba[smb实现windows和linux间文件共享,明文]	可尝试爆破以及smb自身的各种远程执行类漏洞利用,如,ms08-067,ms17-010,嗅探等……
  - tcp 143	imap[可明文可密文]	可尝试爆破
  - udp 161	snmp[明文]	爆破默认团队字符串,搜集目标内网信息
  - tcp 389	ldap[轻量级目录访问协议]	ldap注入,允许匿名访问,弱口令
  - tcp 512,513,514	linux rexec	可爆破,rlogin登陆
  - tcp 873	rsync备份服务	匿名访问,文件上传
  - tcp 1194	openvpn	想办法钓vpn账号,进内网
  - tcp 1352	Lotus domino邮件服务	弱口令,信息泄漏,爆破
  - tcp 1433	mssql数据库	注入,提权,sa弱口令,爆破
  - tcp 1521	oracle数据库	tns爆破,注入,弹shell…
  - tcp 1500	ispmanager 主机控制面板	弱口令
  - tcp 1025,111,2049	nfs	权限配置不当
  - tcp 1723	pptp	爆破,想办法钓vpn账号,进内网
  - tcp 2082,2083	cpanel主机管理面板登录	弱口令
  - tcp 2181	zookeeper	未授权访问
  - tcp 2601,2604	zebra路由	默认密码zerbra
  - tcp 3128	squid代理服务	弱口令
  - tcp 3312,3311	kangle主机管理登录	弱口令
  - tcp 3306	mysql数据库	注入,提权,爆破
  - tcp 3389	windows rdp远程桌面	shift后门[需要03以下的系统],爆破,ms12-020[蓝屏exp]
  - tcp 4848	glassfish控制台	弱口令
  - tcp 4899	radmin远程桌面管理工具,现在已经非常非常少了	抓密码拓展机器
  - tcp 5000	sybase/DB2数据库	爆破,注入
  - tcp 5432	postgresql数据库	爆破,注入,弱口令
  - tcp 5632	pcanywhere远程桌面管理工具	抓密码,代码执行,已经快退出历史舞台了
  - tcp 5900,5901,5902	vnc远程桌面管理工具	弱口令爆破,如果信息搜集不到位,成功几率很小
  - tcp 5984	CouchDB	未授权导致的任意指令执行
  - tcp 6379	redis未授权	可尝试未授权访问,弱口令爆破
  - tcp 7001,7002	weblogic控制台	java反序列化,弱口令
  - tcp 7778	kloxo	主机面板登录
  - tcp 8000	Ajenti主机控制面板	弱口令
  - tcp 8443	plesk主机控制面板	弱口令
  - tcp 8069	zabbix	远程执行,sql注入
  - tcp 8080-8089	Jenkins,jboss	反序列化,控制台弱口令
  - tcp 9080-9081,9090	websphere控制台	java反序列化/弱口令
  - tcp 9200,9300	elasticsearch	远程执行
  - tcp 10000	webmin linux主机web控制面板入口	弱口令
  - tcp 11211	memcached	未授权访问
  - tcp 27017,27018	mongodb	爆破,未授权访问
  - tcp 3690	svn服务	svn泄露,未授权访问
  - tcp 50000	SAP Management Console	远程执行
  - tcp 50070,50030	hadoop	默认端口未授权访问       未授权访问
> 批量搜索可以采用fofa等
> 若不是最新版本极有可能存在历史漏洞

