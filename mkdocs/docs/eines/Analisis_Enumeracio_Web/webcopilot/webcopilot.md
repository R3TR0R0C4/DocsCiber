# h4r5h1t / WebCopilot
![](./img/webcopilotLogo.png)

[Home](../../../README.md)

[GitHub](https://www.kali.org/tools/webcopilot/)

[Baixada Local](./githubClone/webcopilot_2024-05-04.7z)

## Utilització

webcopilot [opcions] [URL | objectiu]

### Paràmetres Comuns

Opcions bàsiques:

- `-u <URL>`, `--url <URL>` : Especifica la URL de l'objectiu per analitzar.
- `-m <mode>`, `--mode <mode>` : Defineix el mode d'anàlisi (ex: `scan`, `audit`, `report`).
- `-t <nombre>`, `--threads <nombre>` : Nombre de fils paral·lels per optimitzar la velocitat d'escaneig.
- `-o <fitxer>`, `--output <fitxer>` : Defineix un fitxer de sortida per al resultat.
- `-v`, `--verbose` : Mostra la sortida detallada durant l'execució.
- `--proxy <proxy>` : Utilitza un servidor proxy per a les connexions.

Modes disponibles:

- `scan` : Escaneig bàsic de l'objectiu per trobar vulnerabilitats.
- `audit` : Auditoria en profunditat per a una anàlisi més exhaustiva.
- `report` : Generació d'informes detallats de l'anàlisi.

### Exemples d'ús

* Realitzar un escaneig bàsic d'un lloc web:

    ```
    webcopilot -u https://example.com -m scan
    ```

<br>

* Auditoria detallada d'un objectiu amb sortida guardada:

    ```
    webcopilot -u https://example.com -m audit -o resultat.txt
    ```

<br>

* Executar l'escaneig amb un servidor proxy:

    ```
    webcopilot -u https://example.com -m scan --proxy http://proxyserver:port
    ```

### Notes Addicionals

- Utilitzeu `--debug` per una sortida detallada de depuració.
- L'opció `--no-verify` desactiva la verificació de certificats SSL/TLS.

Per més informació, consulteu la [documentació completa de WebCopilot](https://www.kali.org/tools/webcopilot/).

