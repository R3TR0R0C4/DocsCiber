# PEAS-ng Framework
![](./img/peassLogo.png)

[Home](../../../README.md)

[KaliTools](https://www.kali.org/tools/peas-ng/)

## Utilització

peas-ng [opcions] [arxiu]

### Paràmetres Comúns

Opcions per a l'exploració de privilegis:
- `-m <mòdul>`, `--module <mòdul>` : Especifica el mòdul de verificació (e.g., `suid`, `cronjobs`, etc.).
- `-a`, `--all` : Executa tots els mòduls per obtenir una revisió completa del sistema.
- `-o <arxiu>`, `--output <arxiu>` : Desar els resultats en un fitxer.
- `-c`, `--check` : Verifica si hi ha exploits associats als resultats obtinguts.
- `-q`, `--quiet` : Mode silenciat, redueix la quantitat de sortida.

Altres opcions:
- `-t <número>`, `--threads <número>` : Defineix el nombre de fils per a la inspecció paral·lela (per defecte, 2).
- `-f`, `--format <tipus>` : Format de sortida (e.g., `json`, `txt`).
- `--timeout <número>` : Temps màxim per a l'execució de cada mòdul (en segons).

### Exemples d'ús

* Executar tots els mòduls d'exploració per obtenir un informe complet:

    ```
    peas-ng -a
    ```

<br>

* Executar el mòdul `suid` per trobar binaris SUID vulnerables:

    ```
    peas-ng -m suid
    ```

<br>

* Desar els resultats de l'anàlisi a un fitxer `output.log`:

    ```
    peas-ng -a -o output.log
    ```

<br>

* Executar tots els mòduls amb sortida en format JSON:

    ```
    peas-ng -a -f json
    ```

<br>

* Executar el mòdul `cronjobs` i verificar possibles exploits associats:

    ```
    peas-ng -m cronjobs -c
    ```

## Notes Addicionals
- Aquesta eina està dissenyada per ajudar a identificar potencials vies d'escalada de privilegis.
- Feu servir aquesta eina només amb permís en entorns autoritzats i amb responsabilitat.

