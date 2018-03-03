
`wget https://suitecrm.com/files/156/SuiteCRM-7.8/217/SuiteCRM-7.8.15.zip`
`unzip SuiteCRM-7.8.15.zip`
`mv SuiteCRM-7.8.15 suitecrm`
`rm SuiteCRM-7.8.15.zip`

`sudo chown -R nginx:nginx suitecrm`
`cd suitecrm`
`sudo chmod 766 custom`
`sudo chmod 755 cache`
`sudo chmod 755 modules`

`sudo mysql -u root -p`
`create database suitecrm_db;`
`grant all privileges to suitecrm.* on suitecrm;`
`\q`



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
