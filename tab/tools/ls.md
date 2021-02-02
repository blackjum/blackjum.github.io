# 漏洞扫描器

> ## AWVS
> 扫web

> ## Burpsuite

> ## Nessus
> 扫主机

> ## Xray
> 结合burp被动扫描

> ## nmap
> ```bash
> # nmap 子域名批量漏扫
> nmap -iL domain.txt --script=auth,vuln,ftp-brute,imap-brute,
smtp-brute,pop3-brute,mongodb-brute,redis-brute,ms-sql-brute,
rlogin-brute,rsync-brute,mysql-brute,pgsql-brute,oracle-sid-brute,
oracle-brute,rtsp-url-brute,snmp-brute,svn-brute,
telnet-brute,vnc-brute,xmpp-brute    > scan.txt
> ```