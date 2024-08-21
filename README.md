# zp-crack
security engine command line tool - crack
### features
- supported services: ftp, ssh, telnet, smtp, httpbasic, pop3, wmi, imap, snmp, ldap, smb, smtpssl, rtsp, rsync, imapssl, pop3ssl, socks5, sql server, oracle, mqtt, mysql, rdp, postgresql, amqp, vnc, winrm, redis, memcached, mongodb, tomcat, weblogic, jenkins, gitlab, nacos, nexus, svn
- support proxy(socks5)
### usage
```bash
Usage:
  ./zp-crack crack [flags]

Flags:
      --crack-all           crack all user and pass
      --delay int           delay time between crack (default 1)
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
                             crack example: ./zp-crack crack -i 10.1.2.138:3307---mysql,10.1.2.138:3306
  -f, --inputs-file string   inputs file split by line(example: -f 'xxx.txt')
      --level string         logger level(debug|info|error) (default "info")
  -o, --output-file string   output file to write results (default "output.json")
```
### disclaimer
This tool is only intended for security research. Users are responsible for all legal and related liabilities resulting from the use of this tool. The original author does not assume any legal responsibility.
