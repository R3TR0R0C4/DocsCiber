# Hydra

![](./img/hydraLogo.png)

[Home](../../../../README.md)

[KaliTools](https://www.kali.org/tools/hydra/)

## Utilització

hydra [opcions] [protocol://objectiu[:port]]

### Paràmetres Comuns

Opcions bàsiques:
- `-l <usuari>`, `--login <usuari>` : Especifica un únic nom d'usuari per provar.
- `-L <arxiu>`, `--logins <arxiu>` : Especifica un fitxer amb una llista de noms d'usuari.
- `-p <contrasenya>`, `--password <contrasenya>` : Especifica una única contrasenya per provar.
- `-P <arxiu>`, `--passwords <arxiu>` : Especifica un fitxer amb una llista de contrasenyes.
- `-t <nombre>`, `--tasks <nombre>` : Nombre de fils paral·lels (per defecte 16).
- `-o <arxiu>`, `--output <arxiu>` : Desar els resultats en un fitxer.
- `-f`, `--exit-on-success` : Finalitza el procés tan bon punt es trobi una contrasenya vàlida.
- `-V`, `--verbose` : Mostra cada intent de login.

Protocols suportats (exemples):
- `ssh` : Brute force per connexions SSH.
- `ftp` : Prova d'accés a servidors FTP.
- `http` : Atac a serveis web HTTP.
- `smb` : Força bruta per serveis SMB.

### Exemples d'ús

* Atac de força bruta contra un servei SSH amb l'usuari `admin` i un fitxer de contrasenyes:

    ```
    hydra -l admin -P passwords.txt ssh://192.168.1.100
    ```

<br>

* Utilitzar una llista de noms d'usuari (`users.txt`) i un fitxer de contrasenyes (`passwords.txt`) per a un atac a un servidor FTP:

    ```
    hydra -L users.txt -P passwords.txt ftp://192.168.1.101
    ```

<br>

* Realitzar un atac web HTTP a una pàgina d'inici de sessió amb un formulari personalitzat:

    ```
    hydra -l user -P common-passwords.txt -s 8080 -t 4 http-post-form \
    "/login:username=^USER^&password=^PASS^:F=error" 192.168.1.102
    ```

### Notes Addicionals
- Utilitzeu l'opció `-d`, `--debug` per mostrar sortida detallada per depurar errors.
- La variable `F=error` al formulari HTTP indica el text que Hydra busca per determinar un intent fallit.

Per més opcions avançades i exemples, consulteu la [documentació completa de Hydra](https://www.kali.org/tools/hydra/).

