## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Solución                                                                                    
```
┌──(kali㉿Franco)-[~/picoCTF/forensic3/WebNet1]
└─$ wget https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap      
--2024-10-09 13:11:40--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 92525 (90K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap            100%[==============================>]  90.36K  23.1KB/s    in 3.9s    

2024-10-09 13:11:59 (23.1 KB/s) - ‘capture.pcap’ saved [92525/92525]

                                                                                               
┌──(kali㉿Franco)-[~/picoCTF/forensic3/WebNet1]
└─$ wget https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key
--2024-10-09 13:12:29--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1704 (1.7K) [application/octet-stream]
Saving to: ‘picopico.key’

picopico.key            100%[==============================>]   1.66K  --.-KB/s    in 0s      

2024-10-09 13:12:43 (49.0 MB/s) - ‘picopico.key’ saved [1704/1704]                                                                                            
┌──(kali㉿Franco)-[~/picoCTF/forensic3/WebNet1]
└─$ ls
capture.pcap  picopico.key

┌──(kali㉿Franco)-[~/picoCTF/forensic3/WebNet1]
└─$ wireshark capture.pcap &
[1] 32565
```

En wireshack usando la misma llave que habiamos puesto seguimos los streams que teniamos de TLS. despues vemos los paquetes http, hasta abajo saldra la bandera
## Notas adicionales

## Referencias