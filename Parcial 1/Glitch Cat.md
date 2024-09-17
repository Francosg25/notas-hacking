## Objetivo
Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance.
## Solución
```
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1]
└─$ cd Glitch\ Cat 
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Glitch Cat]
└─$ nc saturn.picoctf.net 58182 
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Glitch Cat]
└─$ python           
Python 3.11.9 (main, Apr 10 2024, 13:16:36) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
'picoCTF{gl17ch_m3_n07_bda68f75}'
```
## Notas adicionales

## Referencias