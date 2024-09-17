## Objetivo

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm) has extraordinarily helpful information...
## Solución
```                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Wave a flag]
└─$ ls 
warm
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Wave a flag]
└─$ file warm
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=3181a501366281ab5eba1c41e54a1f40800e3966, with debug_info, not stripped
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Wave a flag]
└─$ chmod +x warm
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Wave a flag]
└─$ ls 
warm
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/Wave a flag]
└─$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}
```
## Notas adicionales

## Referencias