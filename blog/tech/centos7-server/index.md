
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

```
x Nginx armhf package does not exists:
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

```
yum install vim

yum install git
```
```
yum install mariadb-server
systemctl enable mariadb

vim /etc/my.cnf.d/server.cnf
# [mariadb]
# character-set-server = utf8mb4

vim /etc/my.cnf.d/client.cnf
# [client-mariadb]
# default-character-set = utf8mb4
```

```
useradd ***
passwd ***
usermod -aG wheel ***
# check
visudo

# Disable root to login via ssh
vi /etc/ssh/sshd_config
systemctl restart sshd

passwd root

exit
```

```
sudo yum install golang

vim ~/.bash_profile
```

Write:

```
export GOROOT=$HOME/go
export PATH=$PATH:$GOROOT/bin
```

```
source ~/.bash_profile
```

## Gitea

https://docs.gitea.io/en-us/install-from-source/

```
go get -d -u code.gitea.io/gitea
cd $GOPATH/src/code.gitea.io/gitea

create database gitea;
create user gitea identified by '***';
grant all privileges on gitea.* to gitea;
```
