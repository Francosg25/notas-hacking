## Objetivo
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too

## Solución
```                  
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 2]
└─$ nano level2.py
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 2]
└─$ python          
Python 3.11.9 (main, Apr 10 2024, 13:16:36) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65)
'39ce'
>>> exit()
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 2]
└─$ python level2.py
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
```
## Notas adicionales

## Referencias