
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
