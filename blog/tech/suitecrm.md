
Get latest:

`wget https://suitecrm.com/files/160/SuiteCRM-7.10/224/SuiteCRM-7.10.zip`

or lts:

`wget https://suitecrm.com/files/156/SuiteCRM-7.8/217/SuiteCRM-7.8.15.zip`

```
unzip SuiteCRM-*.zip
rm SuiteCRM-*.zip

mv SuiteCRM-* suitecrm
```

```
sudo chown -R nginx:nginx suitecrm
cd suitecrm
sudo chmod 766 custom
sudo chmod 755 cache
sudo chmod 755 modules
```

`sudo mysql -u root -p`

```
create database suitecrm_db;
create user suitecrm identified by '';
grant all privileges on suitecrm.* to suitecrm;
\q
```

install.php
php7-xml
php7/php.ini -- upload file size 8M (at least more than 6M)

https://crowdin.com/project/suitecrmtranslations/ja
Download: ja.zip

login

system
- module loader

upload ja.zip

* php7-tokenizer

install -> commit

quick repair

system locale

logout

done

php7-iconv
