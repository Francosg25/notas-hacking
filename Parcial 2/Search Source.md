## Objetivo
The developer of this website mistakenly left an important artifact in the website source, can you find it?The website is [here](http://saturn.picoctf.net:54615/)
## Solución
```
┌──(kali㉿Franco)-[~/picoCTF/parcial2/searchsource]
└─$ httrack 'http://saturn.picoctf.net:50201/' 
Mirror launched on Sun, 20 Oct 2024 20:00:57 by HTTrack Website Copier/3.49-5 [XR&CO'2014]
mirroring http://saturn.picoctf.net:50201/ with the wizard help..
Done.: saturn.picoctf.net:50201/images/fevicon.png (153 bytes) - 404
Thanks for using HTTrack!

┌──(kali㉿Franco)-[~/picoCTF/parcial2/searchsource]
└─$ grep -nr picoCTF                    
saturn.picoctf.net_50201/css/style.css:328:/** banner_main picoCTF{1nsp3ti0n_0f_w3bpag3s_587d12b8} **/

```
## Notas adicionales

## Referencias