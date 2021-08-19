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
# ODOOTOOLS 

for req in `ls /usr/share/odoo*/requirements.txt`
do 
	sudo pip install -r $req
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
