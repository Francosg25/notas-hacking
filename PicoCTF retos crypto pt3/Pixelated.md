## Objetivo
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/c9593d1d2ac9d850da95bffe0ac3b6c6/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/c9593d1d2ac9d850da95bffe0ac3b6c6/scrambled2.png)
## Solución
Descargamos la herramienta imagemagick y convertimos las dos imagenes en una sola
```
┌──(kali㉿Franco)-[~/picoCTF/crypto3/pixelated]
└─$ sudo apt install imagemagick
Upgrading:                      
  imagemagick          imagemagick-6.q16           libmagickcore-6.q16-7t64
  imagemagick-6-common libmagickcore-6.q16-7-extra libmagickwand-6.q16-7t64                       

┌──(kali㉿Franco)-[~/picoCTF/crypto3/pixelated]
└─$ convert scrambled1.png scrambled2.png -compose Add -composite bandera.png

┌──(kali㉿Franco)-[~/picoCTF/crypto3/pixelated]
└─$ ls    
bandera.png  scrambled1.png  scrambled2.png

┌──(kali㉿Franco)-[~/picoCTF/crypto3/pixelated]
└─$ eog bandera.png 

```

```
picoCTF{da8fcef8}
```
## Notas adicionales

## Referencias