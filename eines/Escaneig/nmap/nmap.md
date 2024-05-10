# nmap

![](img/nmapLogo.png)

[Home](../../../readme.md)

[Link](https://nmap.org/)

## Utilització

Usage: nmap [Scan Type(s)] [Options] {target specification}

### Paràmetres Comúns
 - `-T<0-5>` :Configura la velocitat d'escaneig (Més alt més ràpid)
 - `-O` :Habilita la detecció d'OS
 - `-oN/-oX/-oG <file>` :Sortida, Normal, XML, Grepable
 - `-sn` :Ping only, retorna MAC i temps de ping, si està encés
 - `-Pn` :Tracta tots els hosts com online, es saltarà el check inicial de ping
 - `--script=` :Permét usar scripts, vegueu 

### Scripts

[Llista Oficial](https://nmap.org/nsedoc/scripts/)

 - `banner` : Llista l'informació del banner TCP.
 - `cups-info` : Intentarà recollir informació d'impresores manejades per CUPS.
 - `dhcp-discover` : Enviarà un paquet DHCPINFORM per recollir l'informació donada per un servidor DHCP sense agarrar una adreça.
 - `dns-brute` : Fà un brute force per intentar llistar els hostnames d'un servidor DNS amb subdominis comúns.
 - `dns-fuzz` : Atac de fuzzing contra un servei DNS.
 - `docker-version` : Intenta recollir la versió de docker.
 - `ftp-anon` : Intenta un login anonymous a un servidor FTP.
 - `ftp-brute` : Atac de força bruta contra FTP.
 - `http-csrf` : Reporta si hi ha alguna vulnerabilitat Cross Site Request Forgeries (CSRF).
 - `http-enum` : Enumeració de directoris en servidor HTTP.
 - `http-passwd` : Comprova si el servidor web és vulnerable a directory traversal intentant printar el contingut de `/etc/passwd` o `\boot.ini`. 
 - `http-robots.txt` : Comprova els elements bloquejats d'un servidor web del fitxer `/robots.txt`
 - `ldap-search` : Intenta fer un search en un servei ldap.
 - `mikrotik-routeros-brute` : Intenta fer un atac de força bruta en el servei d'autentiació Mikrotik
 - `mysql-databases` : Intenta llistar les BDs d'un servei mysql.
 - `mysql-users` : Intenta llistar els usuaris d'un servei mysql.
 - `nfs-showmount` : Intenta llistar els directoris compartits per un servidor NFS.
 - `smb-server-stats` : Intenta llistar les estadistiques d'un servidor através del servei SMB pels ports 445 o 139.
 - `vulners` : Comprova vulnerabilitats, les mostra i el seu CVSS score.
 - 