## Objetivo
All we know is the file with the flag is named `down-at-the-bottom.txt`... Disk image: [dds2-alpine.flag.img.gz](https://mercury.picoctf.net/static/aed64c508175df5fe23207c10e0e47e5/dds2-alpine.flag.img.gz)
## Solución
```
┌──(kali㉿Franco)-[~/parcial2/diskdisksleuthII]
└─$ file dds2-alpine.flag.img 
dds2-alpine.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0x10,81,1), startsector 2048, 260096 sectors
                                                                                               
┌──(kali㉿Franco)-[~/parcial2/diskdisksleuthII]
└─$ mmls dds2-alpine.flag.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000262143   0000260096   Linux (0x83)
                                                                                               
┌──(kali㉿Franco)-[~/parcial2/diskdisksleuthII]
└─$ fsstat dds2-alpine.flag.img -o 2048 | head
FILE SYSTEM INFORMATION
--------------------------------------------
File System Type: Ext3
Volume Name: 
Volume ID: dc53a3bb0ae739a5164c89db56bbb12f

Last Written at: 2021-02-16 13:21:20 (EST)
Last Checked at: 2021-02-16 13:21:19 (EST)

Last Mounted at: 2021-02-16 13:21:19 (EST)
                                                                                               
┌──(kali㉿Franco)-[~/parcial2/diskdisksleuthII]
└─$ fls -r dds2-alpine.flag.img -o 2048 | grep down
++ d/d 2177:    if-down.d
++ d/d 2178:    if-post-down.d
++ d/d 2180:    if-pre-down.d
++ d/d 2204:    shutdown
+ r/r 18291:    down-at-the-bottom.txt
+ l/l 18311:    ifdown
+ r/r 18344:    openrc-shutdown
+++++ r/r 12472:        down.sh
                                                                                               
┌──(kali㉿Franco)-[~/parcial2/diskdisksleuthII]
└─$ icat ./dds2-alpine.flag.img -o 2048 18291
   _     _     _     _     _     _     _     _     _     _     _     _     _  
  / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \ 
 ( p ) ( i ) ( c ) ( o ) ( C ) ( T ) ( F ) ( { ) ( f ) ( 0 ) ( r ) ( 3 ) ( n )
  \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/ 
   _     _     _     _     _     _     _     _     _     _     _     _     _  
  / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \ 
 ( s ) ( 1 ) ( c ) ( 4 ) ( t ) ( 0 ) ( r ) ( _ ) ( n ) ( 0 ) ( v ) ( 1 ) ( c )
  \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/   \_/ 
   _     _     _     _     _     _     _     _     _     _     _  
  / \   / \   / \   / \   / \   / \   / \   / \   / \   / \   / \ 
 ( 3 ) ( _ ) ( f ) ( 5 ) ( 5 ) ( 6 ) ( 5 ) ( e ) ( 7 ) ( b ) ( } )

```
## Notas adicionales

## Referencias