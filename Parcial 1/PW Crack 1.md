## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.
## Solución                                                                            
```                    
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1]
└─$ cd PW\ Crack\ 1 
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 1]
└─$ ls
level1.flag.txt.enc  level1.py
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 1]
└─$ nano level1.py             
                                                                                                
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 1]
└─$ python
Completing external command
py3clean                                      pyi-grab_version                            
py3compile                                    pyi-makespec                                
py3rsa-decrypt                                pyinstaller                                 
py3rsa-encrypt                                pyi-set_version                             
py3rsa-keygen                                 pylnk3                                      
py3rsa-priv2pub                               pylupdate5                                  
py3rsa-sign                                   pylupdate6                                  
py3rsa-verify                                 pypykatz                                    
py3versions                                   pyrcc5                                      
pybabel                                       pyserial-miniterm                           
pybabel-python3                               pyserial-ports                              
pyclean                                       py-sneakers                                 
pycompile                                     pyspnego-parse                              
pydoc                                         python                                      
pydoc2                                        python2                                     
pydoc2.7                                      python2.7                                   
pydoc3                                        python3                                     
pydoc3.11                                     python3.11                                  
pydoc3.12                                     python3.11-config                           
pyfiglet                                      python3.12                                  
pygettext2                                    python3-config                              
pygettext2.7                                  python3-qr                                  
pygettext3                                    python-argcomplete-check-easy-install-script
pygettext3.11                                 python-dotenv                               
pygettext3.12                                 python-faraday                              
pygmentex                                     pyuic5                                      
pygmentize                                    pyuic6                                      
pyhtmlizer3                                   pyversions                                  
pyi-archive_viewer                            pyvnc.py                                    
┌──(kali㉿Franco)-[~/hacking/PARCIAL 1/PW Crack 1]
└─$ python level1.py 
Please enter correct password for flag: 691d
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}

```
## Notas adicionales

## Referencias