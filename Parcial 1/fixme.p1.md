## Objetivo

Fix the syntax error in this Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/27/fixme1.py)

## Solución
```
──(kali㉿Franco)-[~/hacking/PARCIAL 1]
└─$ cd fixme.p1 
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/fixme.p1]
└─$ ls 
fixme1.py
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/fixme.p1]
└─$ python fixme1.py           
  File "/home/kali/hacking/PARCIAL 1/fixme.p1/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/fixme.p1]
└─$ nano fixme1.py            
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/fixme.p1]
└─$ nano fixme1.py
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/fixme.p1]
└─$ python fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
```
## Notas adicionales

## Referencias