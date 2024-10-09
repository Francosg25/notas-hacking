## Objetivo
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt) is all blank!
## Solución
Descargamos el contenido 
```
┌──(kali㉿Franco)-[~/picoCTF/forensic2/whitepages]
└─$ wget https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt 
--2024-10-07 12:39:50--  https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt
```
Usamos un comando que nos remplazara caracteres a 0 y 1 para convertir en binario todo y asi poder transformar la bandera
```
sed "s/\xe2\x80\x83/0/g" whitepages.txt | sed "s/\x20/1/g"
```

Usamos cyberchef para poder convertir una cadena binaria a texto 
## Notas adicionales

## Referencias