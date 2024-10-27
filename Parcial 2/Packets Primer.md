## Objetivo
Download the packet capture file and use packet analysis software to find the flag.

- [Download packet capture](https://artifacts.picoctf.net/c/194/network-dump.flag.pcap)
## Solución
```
┌──(kali㉿kali)-[~/picoCTF/parcial2]
└─$ ls
network-dump.flag.pcap

┌──(kali㉿kali)-[~/picoCTF/parcial2]
└─$ file network-dump.flag.pcap 
network-dump.flag.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)

┌──(kali㉿kali)-[~/picoCTF/parcial2]
└─$ wireshark network-dump.flag.pcap &                                
[1] 3810

┌──(kali㉿kali)-[~/picoCTF/parcial2]
└─$ Warning: program compiled against libxml 212 using older 209

[1]  + done       wireshark network-dump.flag.pcap
┌──(kali㉿kali)-[~/picoCTF/parcial2]
└─$
```
Abrimos el archivo con wireshark, seleccionamos un archivo que información y le damos clic en TCP Steam; y despues nos da la bandera
## Notas adicionales

## Referencias