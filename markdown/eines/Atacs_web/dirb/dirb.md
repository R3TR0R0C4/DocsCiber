# dirb

![](./img/dirbLogo.png)

[Home](../../../README.md)

[KaliTools](https://www.kali.org/tools/dirb/)

## Utilització

dirb <url_base> <url_base> [<wordlist_file(s)>] [options]

### Paràmetres Comúns
 - `-a <agent_string>` :Especifica el USER_AGENT, per defecte s'utilitza "Default is: "Mozilla/4.0 (com-patible; MSIE 6.0; Windows NT 5.1)".
 - `-i` :Realitza la búsqueda 'case-sensitive'.
 - `-o <arxiu>` :Guarda la sortida a un arxiu.
 - `-p <proxy[:port]>` :Utilitza el proxy indicat, port per defecte 1080.
 - `-P <proxy_username:proxy_password>` :Autenticació del proxy.
 - `-r` :No buscar de forma recursiva.
 - `-S` :Mode silencios
 - `-t` :No forçar que el final de l'url acabi amb "/".
 - `-u <username:password>` :Usuari i contrasenya de la pàgina.
 - `-w` :No parar als missatges d'error.