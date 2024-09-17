## Objetivo
Fix the syntax error in the Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/4/fixme2.py)

---
## Solución
```
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/fixme.p2]
└─$ ls
fixme2.py
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/fixme.p2]
└─$ python fixme2.py
  File "/home/kali/hacking/PARCIAL 1/fixme.p2/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/fixme.p2]
└─$ nano fixme2.py
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/fixme.p2]
└─$ python fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
```       
## Notas adicionales

## Referencias