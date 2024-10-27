## Objetivo
Someone might have hidden the password in the trace file. Find the key to unlock [this file](https://artifacts.picoctf.net/c/492/flag.zip). [This tracefile](https://artifacts.picoctf.net/c/492/dump.pcap) might be good to analyze.
## Solución
Abrimos con wireshack y filtramos paquetes que nos da, explorando estos archivos nos da un archivo para decodificarlo en base64 
```
└─$ echo -n aaAABBHHPJGTFRLKVGhpcyBpcyB0aGUgc2VjcmV0OiBwaWNvQ1RGe1IzNERJTkdfTE9LZF8= | base64 -di
```
Eso es la contrasenia con la que descomprimos el zip y ahi nos da la bandera 

```                                                                                    
┌──(kali㉿Franco)-[~/parcial2/FindAndOpen]
└─$ cat flag 
picoCTF{R34DING_LOKd_fil56_succ3ss_cbf2ebf6}

```

## Notas adicionales

## Referencias