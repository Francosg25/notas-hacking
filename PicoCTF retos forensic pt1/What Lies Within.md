## Objetivo
There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?
## Solución
```
Descargamos el archivo que se nos da
┌──(kali㉿Franco)-[~/picoCTF/forensic/whatlieswithin]
└─$ wget https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png
```
Despues de esto instalamos zsteg
```
sudo gem install zsteg
```
Usamos esta herramienta para descubir la bandera en la imagen que se descargo 

```
┌──(kali㉿Franco)-[~/picoCTF/forensic/whatlieswithin]
└─$ zsteg -a buildings.png | grep pico
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"
```
## Notas adicionales
zsteg **se especializa en descubrir datos ocultos en archivos PNG y BMP**.

## Referencias
