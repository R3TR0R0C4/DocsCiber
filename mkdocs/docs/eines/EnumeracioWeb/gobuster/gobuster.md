# gobuster

![](img/gobusterLogo.png)

[Home](../../../README.md)

[KaliTools](https://www.kali.org/tools/gobuster/)

## Utilització

gobuster [opcions] [objectiu, ip/URL] -w [wordlist]

### Paràmetres Comúns

  - `-w <arxiu>` :Indiquem l'arxiu wordlist.
  - `-u <url>` :URL a escanejar, no és necessari pero recomanable.
  - `-P <Contrasenya>` :Contrasenya a utilitzar en un login d'una web.
  - `-U <Usuari>` :Usuari a utilitzar en un login d'una web.
  - `-a <User_Agent>` :Canviem el user_agent.
  - `-e` :Mostrem la url completa de l'arxiu.
  - `-k` :Ens saltem la verificació SSL.
  - `-r` :Seguir redireccións (pot ser inconvenient ja a que pot enviar-te a moltes webs).
  - `-x <extensió>` :Extensió d'arxius a buscar, podem buscarne varis separats amb comes "pdf,xml,mp3".

### Exemples d'ús

 - Búsqueda amb urls completes, amb mode directori, amb la wordlist customitzada:

   ![](./img/exempleScan1.png)


