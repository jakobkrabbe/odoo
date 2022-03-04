# Odoo
My Odoo files and notes

Look in every branch, to download projects.

` some code`

```
sudo chown odoo:odoo /usr/share/odoo*/ -R
sudo chmod g+w /usr/share/odoo*/ -R

git remote show origin
git config --get remote.origin.url

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
#!/bin/bash
# 2021-08-18 - Automated sudo update
# To execute this simple script, write in Terminal: $ bash update_script.bs

sudo apt-get update -y
sudo apt-get upgrade -y
sudo apt-get autoclean -y
sudo apt-get autoremove -y
sudo apt update -y
sudo apt upgrade -y
sudo apt autoclean -y
sudo apt autoremove -y
# sudo reboot
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
(sudo apt-get update -y) >> $strLog$dteNow
(sudo apt-get upgrade -y) >> $strLog$dteNow
(sudo apt-get autoclean -y) >> $strLog$dteNow
(sudo apt-get autoremove -y) >> $strLog$dteNow
# sudo reboot


## Settiings:
https://crontab.guru/#50_7_*_*_*

## Cron Jobs For Beginners | Linux Task Scheduling
https://www.youtube.com/watch?v=v952m13p-b4

```

