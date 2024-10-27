## Objetivo
How about some hide and seek heh? Download this [file](https://artifacts.picoctf.net/c/373/trace.pcap) and find the flag.
## Solución
Descargamos el archivo y con un simple strings y grep nos da la bandera
```
┌──(kali㉿Franco)-[~/parcial2/pspoisoing]
└─$ wget https://artifacts.picoctf.net/c/373/trace.pcap
--2024-10-26 20:03:36--  https://artifacts.picoctf.net/c/373/trace.pcap
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.120, 13.225.222.105, 13.225.222.28, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.120|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 106715 (104K) [application/octet-stream]
Saving to: ‘trace.pcap’

trace.pcap              100%[==============================>] 104.21K  --.-KB/s    in 0.08s   

2024-10-26 20:03:37 (1.20 MB/s) - ‘trace.pcap’ saved [106715/106715]


┌──(kali㉿Franco)-[~/parcial2/pspoisoing]
└─$ strings trace.pcap | grep pico              
picoCTF{P64P_4N4L7S1S_SU55355FUL_4d72dfcc}9~

```

## Notas adicionales

## Referencias