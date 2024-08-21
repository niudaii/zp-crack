## zp-crack
### Overview
Security engine command line tool - crack
### Features
- Supported Services
  - ftp, ssh, telnet, smtp, httpbasic, pop3, wmi, imap, snmp, ldap, smb, smtpssl, rtsp, rsync, imapssl, pop3ssl, socks5, sqlserver, oracle, mqtt, mysql, rdp, postgresql, amqp, vnc, winrm, redis, memcached, mongodb, tomcat, weblogic, jenkins, gitlab, nacos, nexus, svn
- Flexible Service Input
  - use default port-service(example: -i 10.1.2.5:3306)
  - manually set the service(example: -i 10.1.2.6:3307---mysql)
- Proxy Support
  - socks5
- Dynamic Password Replacement
  - password that contains %user% will be replaced by the corresponding username.
### Download
https://github.com/niudaii/zp-crack/releases
### Usage
```
Usage:
  zp-crack crack [flags]

Examples:
./zp-crack crack -i 10.1.2.5:3306
./zp-crack crack -i 10.1.2.6:3307---mysql
./zp-crack crack -i 10.1.2.5:3306,10.1.2.6:3307---mysql
./zp-crack crack -f input.txt

Flags:
      --crack-all           crack all user and pass
      --delay int           delay time between crack
  -h, --help                help for crack
      --max-task-num int    max crack num, 0 is no limit
      --max-task-time int   max crack time in sec (default 300)
      --pass strings        pass list, split by comma
      --pass-file string    pass file
      --proxy string        socks5 proxy
      --threads int         scan threads (default 5)
      --timeout int         single crack timeout (default 30)
      --user strings        user list, split by comma
      --user-file string    user file

Global Flags:
  -i, --inputs strings       inputs split by comma
  -f, --inputs-file string   inputs file split by line(example: -f 'xxx.txt')
      --level string         logger level(debug|info|error) (default "debug")
  -o, --output-file string   output file to write results (default "output.json")
```
### Default port-service
```
21:    plugins.FTP,
22:    plugins.SSH,
23:    plugins.TELNET,
25:    plugins.SMTP,
80:    plugins.HTTPBASIC,
110:   plugins.POP3,
135:   plugins.WMI,
143:   plugins.IMAP,
161:   plugins.SNMP,
389:   plugins.LDAP,
445:   plugins.SMB,
465:   plugins.SMTPSSL,
554:   plugins.RTSP,
873:   plugins.RSYNC,
993:   plugins.IMAPSSL,
995:   plugins.POP3SSL,
1080:  plugins.SOCKS5,
1433:  plugins.SQLSERVER,
1521:  plugins.ORACLE,
1883:  plugins.MQTT,
3306:  plugins.MYSQL,
3389:  plugins.RDP,
5432:  plugins.POSTGRES,
5672:  plugins.AMQP,
5900:  plugins.VNC,
5985:  plugins.WINRM,
6379:  plugins.REDIS,
11211: plugins.MEMCACHED,
27017: plugins.MONGODB,
```
### Source Code Status
Due to certain reasons, I am unable to open source the code at this time. However, I warmly welcome everyone to submit issues and suggestions! Your feedback is crucial for me to improve the project.
### Disclaimer
This tool is only intended for security research. Users are responsible for all legal and related liabilities resulting from the use of this tool. The original author does not assume any legal responsibility.
