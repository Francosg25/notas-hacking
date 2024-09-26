## Objetivo
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:21939/](http://mercury.picoctf.net:21939/)
## Solución
```
┌──(kali㉿Franco)-[~]
└─$  curl -X HEAD http://mercury.picoctf.net:21939/index.php?
Warning: Setting custom HTTP method to HEAD with -X/--request may not work the 
Warning: way you want. Consider using -I/--head instead.
                                                                                               
┌──(kali㉿Franco)-[~]
└─$ curl -I http://mercury.picoctf.net:21939/index.php?~  
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_6ef27873}
Content-type: text/html; charset=UTF-8

```
## Notas adicionales

## Referencias