## Objetivo
This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.
## Solución

```
Obtenemos el archivo que nos da
┌──(kali㉿Franco)-[~/picoCTF/forensic]
└─$ wget https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg

```
Despues de esto usamos la herramienta de hexeditor y le damos ctrl+w
Al usar esto, buscaremos la bandera por medio de la palabra "PicoCTF" dentro de los bits 
```
┌──(kali㉿Franco)-[~/picoCTF/forensic]
└─$ hexeditor garden.jpg
```
## Notas adicionales
Hexeditor sirve para buscar los bits dentro de una imagen
## Referencias