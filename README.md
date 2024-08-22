## zp-crack
### Overview
`zp-crack` is a powerful command-line tool designed for security professionals and researchers. It facilitates the cracking of various services, enabling users to test the strength of passwords across multiple protocols.
### Features
- **Supported Services**
  - ftp, ssh, telnet, smtp, httpbasic, pop3, wmi, imap, snmp, ldap, smb, smtpssl, rtsp, rsync, imapssl, pop3ssl, socks5, sqlserver, oracle, mqtt, mysql, rdp, postgresql, amqp, vnc, winrm, redis, memcached, mongodb, tomcat, weblogic, jenkins, gitlab, nacos, nexus, svn
- **Flexible Service Input**
  - Default Port-Service Format: Use the default port-service format when specifying an IP address (e.g., `-i 10.1.2.5:3306`). This format must correspond to the services listed in the **Default Port-Service Mapping** section.
  - Manual Service Specification: You can manually specify the service if it differs from the default (e.g., -i `10.1.2.6:3307---mysql`). Ensure that the specified service is included in the **Supported Services** list.
- **Proxy Support**
  - SOCKS5 proxy support for enhanced anonymity during operations.
- **Dynamic Password Replacement**
  - Passwords containing `%user%` will be dynamically replaced with the corresponding username.
### Installation
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
./zp-crack crack -f input.txt --proxy socks5://127.0.0.1:8888

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
### Default Port-Service Mapping

| Port  | Service    |
| ----- | ---------- |
| 21    | ftp        |
| 22    | ssh        |
| 23    | telnet     |
| 25    | smtp       |
| 80    | httpbasic  |
| 110   | pop3       |
| 135   | wmi        |
| 143   | imap       |
| 161   | snmp       |
| 389   | ldap       |
| 445   | smb        |
| 465   | smtpssl    |
| 554   | rtsp       |
| 873   | rsync      |
| 993   | imapssl    |
| 995   | pop3ssl    |
| 1080  | socks5     |
| 1433  | sqlserver  |
| 1521  | oracle     |
| 1883  | mqtt       |
| 3306  | mysql      |
| 3389  | rdp        |
| 5432  | postgresql |
| 5672  | amqp       |
| 5900  | vnc        |
| 5985  | winrm      |
| 6379  | redis      |
| 11211 | memcached  |
| 27017 | mongodb    |
### Source Code Status
Due to certain constraints, the source code is not currently open-source. However, contributions in the form of issues and suggestions are highly encouraged! Your feedback is invaluable for improving this project.
### Disclaimer
This tool is only intended for security research. Users are responsible for all legal and related liabilities resulting from the use of this tool. The original author does not assume any legal responsibility.
