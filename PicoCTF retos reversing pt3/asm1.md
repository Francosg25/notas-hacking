## Objetivo
What does asm1(0x8be) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/66c927e32f3d7be7a62d13a7c2250943/test.S)
## Solución
```
┌──(kali㉿Franco)-[~/picoCTF/reversing3/asm1]
└─$ python3    
Python 3.11.9 (main, Apr 10 2024, 13:16:36) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 0x8be > 0x71c
True
>>> 0x8be != 0x6cf
True
>>> hex(0x8be - 0x3)
'0x8bb'
>>> 
```
## Notas adicionales

## Referencias