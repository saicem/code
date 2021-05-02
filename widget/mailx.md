## 安装`mailx`
```shell
yum  -y install mailx
```

## 编辑配置文件
```shell
vim /etc/mail.rc
```
```
set from=email@host             //对方收到邮件时显示的发件人
set smtp=smtp.126.com           //smtp服务器地址
set smtp-auth-user=13510861001  //邮箱用户名
set smtp-auth-password="XXX"    //邮箱授权码&密码
set smtp-auth=login             //SMTP的认证方式，默认是login
```

## 发送邮件
- mail -s "summary" address < filepath
- echo "content" | mail -s "summary" address
- cat filepath | mail -s "summary" address

>带附件 `-a filepath`
