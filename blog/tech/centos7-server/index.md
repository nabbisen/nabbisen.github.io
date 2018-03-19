
CentOS 7 on Raspberry Pi 2

root / centos

```
# update packages
yum update

# set locale
# - set keyboard
localectl set-keymap jp106
localectl set-keymap jp-OADG109A
# check
localctl
# - set lang
localectl set-locale LANG=ja_JP.utf8
# check
localectl
```

```
# set up ssh
vi /etc/ssh/sshd_config 
systemctl sshd restart

firewall-cmd --add-port=***/tcp --permanent
# check
firewall-cmd --list-all
firewall-cmd --reload
```

```
yum install wget httpd
```

Nginx armhf package does not exists:
x According to [public tutorial](https://www.nginx.com/resources/wiki/start/topics/tutorials/install/)
x 
x ```
x vi /etc/yum.repos.d/nginx.repo
x ```
x 
x Write:
x 
x ```
x [nginx]
x name=nginx repo
x baseurl=http://nginx.org/packages/centos/$releasever/$basearch/
x gpgcheck=0
x enabled=1
x ```



```
yum install golang git
```
