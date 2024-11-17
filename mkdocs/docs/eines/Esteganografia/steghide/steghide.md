# Steghide

![](./img/kali-tools-icon-missing.png)

[Home](../../../README.md)

[KaliTools](https://www.kali.org/tools/steghide/)

## Utilització

steghide [opcions] [arxiu]

### Paràmetres Comúns

Opcións d'amagat:

 - `-ef <arxiu>`, ` --embedfile <arxiu>` :Especifiquem l'arxiu que amagarem
 - `-cf <arxiu>`, ` --coverfile <arxiu>` :Especifiquem l'arxiu de coverta (el que es veurà com resultat)
 - `-p <string>`, `--passphrase <string>` :Contrasenya d'encriptació (opcional). 
 - `-sf <arxiu>`, `--stegofile <arxiu>` :Especifiquem l'arxiu de sortida, si no s'especifica, es sobre-escriurà l'arxiu de coverta..
 - `-z`, `--compress` :Comprimeix les dades avans d'amagarles, valors de 0 a 9, per defecte 6.
  

Opcións d'extracció:

 - `-sf <arxiu>`, `--stegofile <arxiu>` :Indiquem l'arxiu d'on extreure les dades.
 - `-xf`, `--extractfile` :Arxiu de sortida de dades (opcional).
 - `-p`, `--passphrase` :Contrasenya de l'arxi


### Exemples d'ús

* Guardem l'arxiu `secret.txt` a la foto `cover.jpg`, amb la contrasenya `mysecretpass` i compressió màxima (9):

    ```
    steghide embed -cf cover.jpg -ef secret.txt -p "mysecretpass" -z 9
    ```

<br>

*  Extraiem l'arxiu amagat de `cover.jpg` amb la contrasenya `mysecretpass`:

    ```
    steghide extract -sf cover.jpg -p "mysecretpass"
    ```