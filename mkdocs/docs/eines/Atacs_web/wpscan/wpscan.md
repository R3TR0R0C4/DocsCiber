# WpScan

![](./img/wpscanLogo.png)

[Home](../../../README.md)

[KaliTools](https://www.kali.org/tools/netcat/)

## Utilització

Pots utilitzar wpscan sense registrar-te pero idealment utilitzaríes una api key per poder detectar versións i vulnerabilitats d'extensions.

[Link de registre](https://wpscan.com/register/)

Podem utilitzar correus temporals com aquest: [Link](https://temp-mail.org/)

### Paràmetres Comúns
 - `--url <url>` :Indiquem l'url on està el servidor wordpress
 - `--api-token <token>` :Indiquem quina api key tenim
 - `--stealthy` :Aleatoritzem el User_agent per fer l'escaneig més discret

### Exemples d'ús

 - Escaneig d'un servei amb una api key:

   ![](./img/utilitzacio1.png)

 - Aqui una part del resultat:
   
   ![](./img/resultat1.png)