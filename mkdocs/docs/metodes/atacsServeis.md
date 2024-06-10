# Atacs senzills a serveis

## 21 - FTP

* Utilitzem l'usuari `anonymous` o `ftp` sense contrasenya, pot ser que estigui habilitat el mode anonim.
* En cas de tenir accés anonim, utilitzém `wget -m <ftp://anonymous:anonymous@IP>`.
* Buscar la versió del servidor ftp a searchsploit o [Exploit-DB](https://www.exploit-db.com).
* Si hi ha un servidor web, mirem si hi ha algun directori directament relacionat amb ftp, en cas d'existir podem usar reverse-shells o altres.

## 22 - SSH

## 23 - TELNET

## 53 - DNS

## 80/443 - WEB

## 88 - KERBEROS

## 111 - NFS

showmount -e 192.168.1.101

mount 192.168.1.101:/ /tmp/

## 161 - SNMP

## 3306 - MySQL

## 3389 - RDP