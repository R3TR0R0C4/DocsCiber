# Hashcat

![](./img/hashcatLogo.png)

[Home](../../../README.md)

[KaliTools](https://www.kali.org/tools/hashcat/)

## Utilització

hashcat [opcions] <hash> [diccionari | fitxer de regles]

### Paràmetres Comuns

Opcions bàsiques:
- `-m <mode>` : Especifica el tipus de hash (ex: `0` per MD5, `1000` per NTLM).
- `-a <mode>` : Selecciona el mode d'atac (ex: `0` per diccionari, `3` per força bruta).
- `-o <fitxer>` : Fitxer de sortida amb les contrasenyes desxifrades.
- `--username` : Indica que el fitxer de hash inclou noms d'usuari.
- `-w <valor>` : Estableix la quantitat de treball per GPU (ex: `1` baix, `4` alt).
- `--session <nom>` : Guarda o carrega una sessió per a aturades i represa.

Modes d'atac:
- `0` : Atac de diccionari.
- `1` : Atac de combinació.
- `3` : Força bruta.
- `6` : Atac híbrid (diccionari + brut).
- `7` : Atac híbrid (brut + diccionari).

### Exemples d'ús

* Desxifrar un hash MD5 amb un atac de diccionari:

    ```
    hashcat -m 0 -a 0 hash.txt diccionari.txt
    ```

<br>

* Realitzar un atac de força bruta contra un hash NTLM:

    ```
    hashcat -m 1000 -a 3 hash.txt ?a?a?a?a?a?a
    ```

<br>

* Continuar una sessió anterior:

    ```
    hashcat --session mysession --restore
    ```

### Notes Addicionals
- Utilitzeu `--show` per veure resultats de hashes desxifrats.
- `?a` representa un caràcter alfanumèric en un atac de força bruta.

Per més informació, consulteu la [documentació completa de Hashcat](https://www.kali.org/tools/hashcat/).

