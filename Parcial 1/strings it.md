## Objetivo

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?
## Solución
```                                                                         
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1]
└─$ cd strings\ it                  
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/strings it]
└─$ ls
strings
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/strings it]
└─$ grep picoCTF strings
grep: strings: binary file matches
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/strings it]
└─$ strings -n10 strings | grep picoCTF
picoCTF{5tRIng5_1T_7f766a23}
```
                                      
## Notas adicionales

## Referencias