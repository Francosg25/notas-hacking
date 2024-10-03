## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
## Solución
Descargamos el archivo que se nos da, para posteriormente usar el wireshark
```
┌──(kali㉿Franco)-[~/picoCTF/forensic/sharkonwire1]
└─$ wireshark capture.pcap &
[1] 20596
               
```
```
Ya adentro buscamos un paquete que sea formato UDP, ahi le damos click derecho y buscamos la opcion UDP streams, estando ahi es  cuestion de ir buscando la banderas en cada paquete
```
## Notas adicionales


## Referencias