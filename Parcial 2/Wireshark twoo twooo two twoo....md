## Objetivo
Can you find the flag? [shark2.pcapng](https://mercury.picoctf.net/static/a7b4ce62a4f4313a6e5b0b03b97be953/shark2.pcapng).
## Solución
```
┌──(kali㉿Franco)-[~/picoCTF/parcial2/wiresharktwootwoootwotwoo]
└─$ ls
shark2.pcapng

┌──(kali㉿Franco)-[~/picoCTF/parcial2/wiresharktwootwoootwotwoo]
└─$ file shark2.pcapng 
shark2.pcapng: pcapng capture file - version 1.0
```

Con ayuda de wireshack filtramos los archivos
La mayoria de archivos son copias y vemos que hat algunos diferentes
Extraemos el texto  que contiene cada registro y juntan una cadena de codificacion en base64
```
cGljb0NU
RntkbnNf
M3hmMWxf
ZnR3X2Rl
YWRiZWVm
fQ==

cGljb0NURntkbnNfM3hmMWxfZnR3X2RlYWRiZWVmfQ==

[1]  + done       wireshark shark2.pcapng

┌──(kali㉿Franco)-[~/picoCTF/parcial2/wiresharktwootwoootwotwoo]
└─$ echo cGljb0NURntkbnNfM3hmMWxfZnR3X2RlYWRiZWVmfQ== | base64 -d
```
## Notas adicionales

## Referencias