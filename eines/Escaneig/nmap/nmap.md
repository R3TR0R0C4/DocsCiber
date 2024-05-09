# ncat

[Link](https://nmap.org/)

## Utilització

<p>Usage: nmap [Scan Type(s)] [Options] {target specification}</p>

### Paràmetres Comúns
 - `-T<0-5>` :Configura la velocitat d'escaneig (Més alt més ràpid)
 - `-O` :Habilita la detecció d'OS
 - `-oN/-oX/-oG <file>` :Sortida, Normal, XML, Grepable
 - `-sL` :List Scan - simply list targets to scan
 - `-sn` :Ping Scan - disable port scan
 - `-Pn` :Treat all hosts as online -- skip host discovery