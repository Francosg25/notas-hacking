## Objetivo
Download this packet capture and find the flag.

 [Download packet capture](https://artifacts.picoctf.net/c/134/capture.flag.pcap)
## Solución
Abrimos el archivo con wireshack, y dentro del paquete nos viene una conversacion, y con un filtro obtenemos la bandera
```
┌──(kali㉿Franco)-[~/parcial2]
└─$ sudo openssl des3 -d -salt -in file.des3 -out file.txt -k supersecretpassword123
[sudo] password for kali: 
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
                                                                                               
┌──(kali㉿Franco)-[~/parcial2]
└─$ cat file.txt 
picoCTF{nc_73115_411_5786acc3}      
```
## Notas adicionales

## Referencias