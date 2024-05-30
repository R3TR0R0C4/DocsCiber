# Kerbrute

![](img/kali-tools-icon-missing.png)

[Home](../../../../README.md)

[Github](https://github.com/ropnop/kerbrute)

[![CircleCI](https://circleci.com/gh/ropnop/kerbrute.svg?style=svg)](https://circleci.com/gh/ropnop/kerbrute)

Una eina per fer força bruta i enumerar ràpidament els comptes d'Active Directory vàlids mitjançant l'autenticació prèvia de Kerberos

```
$ git clone https://github.com/ropnop/kerbrute.git
```

## Ús

Comandes més importants:

 * **bruteuser** - Força bruta a una password d'un sol username des d'una wordlist.
 * **bruteforce** - Llegeix username:password combos des d'un fitxer o stdin, i els testeja.
 * **passwordspray** - Testeja una sola password per a una llista d'usuaris.
 * **userenum** - Enumera usernames vàlids d'un domini via Kerberos

Un domini (`-d`) o un controlador de domini (`--dc`) serà necessariament especificat. En cas què no s'especifique el controlador de domini, el KDC serà cercat via DNS.

Per defecte, Kerbrute és multithreaded i utilitza 10 threads. Es pot canviar amb l'opció `-t` en cas de volguer més velocitat i rendiment.

Finalment, Kerbrute té una opció `--safe`. Quan aquesta opció està activada, si un compte torna com a bloquejat, avortarà tots els threads per deixar de bloquejar qualsevol altre compte.

## Enumeració

Per enumerar els noms d'usuari, Kerbrute envia sol·licituds TGT sense autenticació prèvia. Si el KDC respon amb un error `PRINCIPAL DESCONEGUT: el nom d'usuari no existeix`. Tanmateix, si el KDC demana una autenticació prèvia, sabem que el nom d'usuari existeix i seguim endavant. Això no provoca cap error d'inici de sessió, de manera que no bloquejarà cap compte. Això genera un ID d'esdeveniment de Windows 4768 si el registre Kerberos està habilitat.

### Exemple

```
root@kali:~# ./kerbrute userenum -d lab.ropnop.com usernames.txt

    __             __               __
   / /_____  _____/ /_  _______  __/ /____
  / //_/ _ \/ ___/ __ \/ ___/ / / / __/ _ \
 / ,< /  __/ /  / /_/ / /  / /_/ / /_/  __/
/_/|_|\___/_/  /_.___/_/   \__,_/\__/\___/

Version: dev (43f9ca1) - 03/06/19 - Ronnie Flathers @ropnop

2019/03/06 21:28:04 >  Using KDC(s):
2019/03/06 21:28:04 >   pdc01.lab.ropnop.com:88

2019/03/06 21:28:04 >  [+] VALID USERNAME:       amata@lab.ropnop.com
2019/03/06 21:28:04 >  [+] VALID USERNAME:       thoffman@lab.ropnop.com
2019/03/06 21:28:04 >  Done! Tested 1001 usernames (2 valid) in 0.425 seconds
```

