## Objetivo
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it. Download the data [here](https://artifacts.picoctf.net/c/124/anthem.flag.txt).
## Solución
```
┌──(kali㉿Franco)-[~/parcial2/lookeyhere]
└─$ wget https://artifacts.picoctf.net/c/124/anthem.flag.txt
--2024-10-26 20:21:40--  https://artifacts.picoctf.net/c/124/anthem.flag.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.125, 13.225.222.105, 13.225.222.120, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.125|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108668 (106K) [application/octet-stream]
Saving to: ‘anthem.flag.txt’

anthem.flag.txt         100%[==============================>] 106.12K  --.-KB/s    in 0.06s   

2024-10-26 20:21:41 (1.60 MB/s) - ‘anthem.flag.txt’ saved [108668/108668]

                                                                                               
┌──(kali㉿Franco)-[~/parcial2/lookeyhere]
└─$ cat anthem.flag.txt| grep pico
      we think that the men of picoCTF{gr3p_15_@w3s0m3_4c479940}

```
## Notas adicionales

## Referencias