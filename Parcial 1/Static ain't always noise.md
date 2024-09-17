## Objetivo


Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/static)? This [BASH script](https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/ltdis.sh) might help!
## Solución
```                    
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1]
└─$ cd Static\ ain\'t\ always\ noise 
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Static ain't always noise]
└─$ ls
ltdis.sh  static
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Static ain't always noise]
└─$ strings static | grep pico               
picoCTF{d15a5m_t34s3r_1e6a7731}
```
## Notas adicionales

## Referencias