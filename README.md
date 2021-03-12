# odoo
My Odoo files and notes

Paste in Terminal:<br>
Vertel AB -- public<br>
<br>
wget -O- https://raw.githubusercontent.com/jakobkrabbe/odoo/10.0/install_repos_vertel_public.bs | bash

Vertel AB -- private<br>
<br>
wget -O- https://raw.githubusercontent.com/jakobkrabbe/odoo/10.0/install_repos_vertel_private.bs | bash


OCA repos<br>
<br>
wget -O- https://raw.githubusercontent.com/jakobkrabbe/odoo/10.0/install_repos_oca.bs | bash


External repos<br>
<br>
wget -O- https://raw.githubusercontent.com/jakobkrabbe/odoo/10.0/install_repos_remote.bs | bash


```
File "/usr/local/lib/python2.7/dist-packages/bcrypt/__init__.py", line 57
    def gensalt(rounds: int = 12, prefix: bytes = b"2b") -> bytes:
                      ^
SyntaxError: invalid syntax

Downgrade with: (https://velenux.wordpress.com/2020/10/28/bcrypt-3-2-0-breaks-ansible-and-more-on-centos-7/)
	
# pip uninstall bcrypt
# pip install bcrypt==3.1.7
```
