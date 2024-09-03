# Odoo <br>
https://github.com/beremavertel/setup
```
odooallrequirements

sudo chown odoo:odoo /usr/share/odoo*/ -R
sudo chmod g+w /usr/share/odoo*/ -R

sudo chmod og+w */static/description/banner.png
sudo chmod 664 */static/description/banner.png
sudo chmod 664 */static/description/icon.png

$ git add --ignore-errors .

sudo rm -rf /usr/share/core-odoo/addons/l10n_se
sudo rm -rf /usr/share/core-odoo/addons/l10n_se_ocr


jakob@fossa:/usr/share/odoo-event$ git pull
error: cannot open .git/FETCH_HEAD: Permission denied
jakob@fossa:/usr/share/odoo-event$ id 
uid=1000(jakob) gid=1000(jakob) groups=1000(jakob),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),110(lxd)


krajak@fossa:~$ ls -ld /usr/share/
drwxr-xr-x 148 root root 4096 maj  7 09:39 /usr/share/
krajak@fossa:~$ sudo chown root:odoo /usr/share/
krajak@fossa:~$ sudo chmod g+w /usr/share/
krajak@fossa:~$ ls -ld /usr/share/
drwxrwxr-x 148 root odoo 4096 maj  7 09:39 /usr/share/


$ git remote get-url origin

odoogitclone odoo-stock
git config --global --add safe.directory /usr/share/odoo-stock


# odoo log rotate <br>
https://www.odoo.com/forum/help-1/why-logrotate-functionality-is-removed-in-odoo13-189132
jakob@ring:$ nano  /etc/logrotate.d/odoo
/var/log/odoo/.odoo-server.log.swp
/var/log/odoo/odoo-server.log
/var/log/odoo/odoo-server.log.1

* * * * * * *
Läser paketlistor… Färdig
Bygger beroendeträd… Färdig
Läser tillståndsinformation… Färdig
4 paket kan uppgraderas. Kör ”apt list --upgradable” för att se dem.
krajak@hugo:~$ sudo apt list --upgradable

The following packages have been kept back:
  sosreport
0 upgraded, 0 newly installed, 0 to remove and 1 not upgraded.
krajak@hugo:~$ sudo apt install sosreport --fix-broken

* * * * * * *
jakob@marina:/usr/share/odoo-project$ 
grep -sR "'name':" */*__.py
grep -sR "'version':" */*__.py
grep -sR "'category':" */*__.py
grep -sR "'summary':" */*__.py
grep -sR "'description':" */*__.py
grep -sR "'description':" */*/*__.py -n | grep "40"
grep -sR "'depends':" */*__.py
grep -sR "'repository':" */*__.py
grep -sR "'website':" */*__.py
ls | wc -l
grep -sR "'website':" */*__.py | tr "'" " "

Find the latest project to copy / paste:
grep -r "2023-03-*" odoo-*/*/static/description/notes.txt
grep -r "2023-*" */static/description/notes.txt
grep -r "2023-12*" /usr/share/odoo*/*/static/description/notes.txt

2022-11-25
grep -r "Expire:" /srv/backup/fossa/*/summary
grep -r "communication_center_massmail_meeting"

## FIND LATEST COMPLETE PROJECT
odoo-website-sale/website_sale_product_variant/static/description/notes.txt:2022-12-08
odoo-website-sale/website_sale_terms/static/description/notes.txt:2022-12-08
jakob@marina:/usr/share$ grep -r "2022-12-*" odoo-*/*/static/description/notes.txt


* * * * * *

## MANIFEST-CHECKER
1. $ git clone git@github.com:beremavertel/setup.git
2. jakob@marina:/usr/share/project$ python3 ~/odootools/scripts/odoocheckdeps.py -t
2. krabban@server:/usr/share/project$ python3 ~/setup/scripts/check_manifests.py -t

## ORIGIN
git remote show origin
git config --get remote.origin.url

krajak@odooutv14:/usr/share/odooext-cybro-OpenHRMS-fix$ git remote -v
origin	git@github.com:vertelab/odooext-cybro-OpenHRMS-fix.git (fetch)
origin	git@github.com:vertelab/odooext-cybro-OpenHRMS-fix.git (push)

* * * * * *
# IF ERROR REMAINS...! DO THE PIP / PIP3 INSTALL! :-)
# https://github.com/vertelab/odootools/blob/14.0/repos/allrequirements

for req in `ls /usr/share/odoo*/requirements.txt`
do
	sudo pip3 install -r $req
done

* * * * * *

error: cannot open .git/FETCH_HEAD: Permission denied

jakob@tessan:/usr/share$ sudo adduser jakob odoo
Adding user `jakob' to group `odoo' ...
Adding user jakob to group odoo
Done.

jakob@tessan:/usr/share$ logout
Connection to tessan closed.
jakob@jango-fett:~$ ssh tessan

```

```
*** System restart required ***
Last login: Wed Feb 14 10:01:14 2024 from 176.10.242.63
krajak@burns:~$ id
uid=1113(krajak) gid=1115(krajak) groups=1115(krajak),121(odoo),1107(sudo),1108(odoo)
krajak@burns:~$ sudo nano /etc/group

>> logout >> login

krajak@burns:~$ id
uid=1113(krajak) gid=1115(krajak) groups=1115(krajak),1107(sudo),1108(odoo)


krajak@burns:/usr/share$ ls -ld odoo*
drwxrwxr-x  53 odoo 121  4096 Feb  8 13:01 odoo-account
drwxrwxrwx   4 odoo 121  4096 Feb  4  2022 odoo-auth
drwxrwxr-x  37 odoo 121  4096 Aug 28 08:05 odoo-base

krajak@burns:/usr/share$ sudo chgrp odoo odoo* -R

krajak@burns:/usr/share$ ls -ld odoo*
drwxrwxr-x  53 odoo odoo  4096 Feb  8 13:01 odoo-account
drwxrwxrwx   4 odoo odoo  4096 Feb  4  2022 odoo-auth
drwxrwxr-x  37 odoo odoo  4096 Aug 28 08:05 odoo-base

krajak@burns:/usr/share$ sudo chgrp odoo odoo* -R

```
```
## IMPORTANT!!
root@fossa:~# cd /var/log/
root@fossa:/var/log# mkdir weeklylog


#!/bin/bash
# 2022-03-04 - Automated sudo update
# To execute this simple script, write in Terminal: $ bash update_script.bs

dteNow=$(date +"%Y-%m-%d.sudo.txt")
strLog=/var/log/weeklylog/
echo "Weekly log // cleaner" >> $strLog$dteNow
(sudo apt-get update -y) >> $strLog$dteNow
(sudo apt-get upgrade -y) >> $strLog$dteNow
(sudo apt-get autoclean -y) >> $strLog$dteNow
(sudo apt-get autoremove -y) >> $strLog$dteNow
(sudo apt update -y) >> $strLog$dteNow
(sudo apt upgrade -y) >> $strLog$dteNow
(sudo apt autoclean -y) >> $strLog$dteNow
(sudo apt autoremove -y) >> $strLog$dteNow
# sudo reboot
```
```
# Categories can be used to filter modules in modules listing
# Check https://github.com/odoo/odoo/blob/14.0/odoo/addons/base/data/ir_module_category_data.xml
# for the full list
'category': 'Uncategorized',
'version': '14.0.0.0.1',
```

```
## Settings:
https://crontab.guru/#50_7_*_*_*

## Cron Jobs For Beginners | Linux Task Scheduling
https://www.youtube.com/watch?v=v952m13p-b4

## FIRST
root@fossa:~# crontab -l

## EDIT
root@fossa:~# crontab -e

## Daily
50 7 * * * /root/weekly_update.bs
## Weekly (Sunday)
50 7 * * 0 /root/weekly_update.bs

```

