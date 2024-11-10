# Atacs senzills a serveis {.atacsServeis_h1}

## 21 - FTP {.atacsServeis_h2}

- Utilitzem l'usuari `anonymous` o `ftp` sense contrasenya, pot ser que estigui habilitat el mode anonim.
- En cas de tenir accés anonim, utilitzém `wget -m <ftp://anonymous:anonymous@IP>`.
- Buscar la versió del servidor ftp a searchsploit o [Exploit-DB](https://www.exploit-db.com).
- Si hi ha un servidor web, mirem si hi ha algun directori directament relacionat amb ftp, en cas d'existir podem usar reverse-shells o altres.
{atacsServeis_ul}

## 22 - SSH {.atacsServeis_h2}

## 23 - TELNET {.atacsServeis_h2}

## 53 - DNS {.atacsServeis_h2}

## 80/443 - WEB {.atacsServeis_h2}

## 88 - KERBEROS {.atacsServeis_h2}

## 111 - NFS {.atacsServeis_h2}

showmount -e 192.168.1.101

mount 192.168.1.101:/ /tmp/

## 161 - SNMP {.atacsServeis_h2}

## 3306 - MySQL {.atacsServeis_h2}

## 3389 - RDP {.atacsServeis_h2}