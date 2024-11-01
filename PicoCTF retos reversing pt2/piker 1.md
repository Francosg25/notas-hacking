## Objetivo
This service can provide you with a random number, but can it do anything else? Connect to the program with netcat: `$ nc saturn.picoctf.net 53874` The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/513/picker-I.py).
## Solución
```
┌──(kali㉿Franco)-[~/picoCTF/reversing2/piker1]
└─$ nc saturn.picoctf.net 53874 
Try entering "getRandomNumber" without the double quotes...
==> win
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x34 0x5f 0x64 0x31 0x34 0x6d 0x30 0x6e 0x64 0x5f 0x31 0x6e 0x5f 0x37 0x68 0x33 0x5f 0x72 0x30 0x75 0x67 0x68 0x5f 0x62 0x35 0x32 0x33 0x62 0x32 0x61 0x31 0x7d 
Try entering "getRandomNumber" without the double quotes...
==> 

```

Con la ayuda de cyberchef sacamos la bandera final 
```
picoCTF{4_d14m0nd_1n_7h3_r0ugh_b523b2a1}
```
## Notas adicionales


## Referencias