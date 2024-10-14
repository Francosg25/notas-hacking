## Objetivo
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/f63e4eba644c99e92324b65cbd875db6/dds1-alpine.flag.img.gz)
## Solución
```

┌──(kali㉿Franco)-[~/picoCTF/forensic4/DiskDiskSleuth]
└─$ wget https://mercury.picoctf.net/static/f63e4eba644c99e92324b65cbd875db6/dds1-alpine.flag.img.gz   
--2024-10-14 19:21:49--  https://mercury.picoctf.net/static/f63e4eba644c99e92324b65cbd875db6/dds1-alpine.flag.img.gz
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29768910 (28M) [application/octet-stream]
Saving to: ‘dds1-alpine.flag.img.gz’

dds1-alpine.flag.img.gz 100%[==============================>]  28.39M   836KB/s    in 35s     

2024-10-14 19:22:24 (832 KB/s) - ‘dds1-alpine.flag.img.gz’ saved [29768910/29768910]


┌──(kali㉿Franco)-[~/picoCTF/forensic4/DiskDiskSleuth]
└─$ gzip -d dds1-alpine.flag.img.gz 

┌──(kali㉿Franco)-[~/picoCTF/forensic4/DiskDiskSleuth]
└─$ ls    
dds1-alpine.flag.img

┌──(kali㉿Franco)-[~/picoCTF/forensic4/DiskDiskSleuth]
└─$ srch_strings dds1-alpine.flag.img | grep picoCTF       
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_ad5c96c0}


```

## Notas adicionales
srch_strings: Se usa para buscar y extraer cadenas de texto legibles dentro de archivos binarios.
## Referencias