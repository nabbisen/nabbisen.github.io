# install

- usb installer: *.fs

# firmware update (because of an old network card)

- usb mount: *.gz x 3

# lumina

- .xsession

```
exec start-lumina-desktop
```

# fcitx-anthy

- .xsession

```
export LANG=ja_JP.UTF-8
export GTK_IM_MODULE=fcitx
export QT_IM_MODULE=fcitx
export XMODIFIERS=@im=fcitx

exec start-lumina-desktop
```

- rm obstacle

```
rm -rf ~/.config/fcitx
```
