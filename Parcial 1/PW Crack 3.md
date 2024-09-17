## Objetivo

Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## Solución                                                                                     
```
┌──(kali㉿Franco)-[~]
└─$ cd hacking/PARCIAL\ 1/PW\ Crack\ 3 
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ nano level3.py                                    
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ nano level3.py
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ python level3.py 
Please enter correct password for flag: f0ac
That password is incorrect
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ nano level3.py  
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ python level3.py
Please enter correct password for flag: 3ac8
That password is incorrect
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ python level3.py
Please enter correct password for flag: ^[[A
That password is incorrect
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ nano level3.py  
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ python level3.py
Please enter correct password for flag: ec27
That password is incorrect
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ python level3.py
Please enter correct password for flag: 
That password is incorrect
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ nano level3.py  
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ python level3.py
Please enter correct password for flag: 4b17
That password is incorrect
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ nano level3.py  
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ python level3.py
Please enter correct password for flag: 4e66
That password is incorrect
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ nano level3.py  
                                                                                               
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 3]
└─$ python level3.py
Please enter correct password for flag: 865e
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}

```
## Notas adicionales

## Referencias