## Objetivo
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/5ef2e9103d55972d975437f68175b9ab/dolls.jpg)
## Solución
Descargamos lo que se ocupa
```
https://mercury.picoctf.net/static/5ef2e9103d55972d975437f68175b9ab/dolls.jpg
```
Con binwalk podemos ver que son varios zip dentro de la imagen, iremos descomprimiendo de uno por uno hasta encontrar la bandera
```
┌──(kali㉿Franco)-[~/picoCTF/forensic3/matryoshkadoll]
└─$ sudo apt install binwalk
binwalk is already the newest version (2.3.4+dfsg1-5).
binwalk set to manually installed.
Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 954
                                                                                               
┌──(kali㉿Franco)-[~/picoCTF/forensic3/matryoshkadoll]
└─$ binwalk dolla.jpg                                                             

General Error: Cannot open file dolla.jpg (CWD: /home/kali/picoCTF/forensic3/matryoshkadoll) : [Errno 2] No such file or directory: 'dolla.jpg'

                                                                                               
┌──(kali㉿Franco)-[~/picoCTF/forensic3/matryoshkadoll]
└─$ binwalk dolls.jpg                              

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378954, uncompressed size: 383940, name: base_images/2_c.jpg
651612        0x9F15C         End of Zip archive, footer length: 22                                                                                            
┌──(kali㉿Franco)-[~/picoCTF/forensic3/matryoshkadoll]
└─$ unzip dolls.jpg           
Archive:  dolls.jpg
warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/2_c.jpg                                                                                                  
┌──(kali㉿Franco)-[~/picoCTF/forensic3/matryoshkadoll]
└─$ ls    
base_images  dolls.jpg                                                                                            
┌──(kali㉿Franco)-[~/picoCTF/forensic3/matryoshkadoll]
└─$ cd base_images/                                                                                              
┌──(kali㉿Franco)-[~/picoCTF/forensic3/matryoshkadoll/base_images]
└─$ ls
2_c.jpg                                                                                              
┌──(kali㉿Franco)-[~/picoCTF/forensic3/matryoshkadoll/base_images]
└─$ unzip 2_c.jpg  
Archive:  2_c.jpg
warning [2_c.jpg]:  187707 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/3_c.jpg     
                                                                                               
┌──(kali㉿Franco)-[~/picoCTF/forensic3/matryoshkadoll/base_images]
└─$ ls
2_c.jpg  base_images
                                                                                               
┌──(kali㉿Franco)-[~/picoCTF/forensic3/matryoshkadoll/base_images]
└─$ unzip 3_c.jpg
unzip:  cannot find or open 3_c.jpg, 3_c.jpg.zip or 3_c.jpg.ZIP.
                                                                                               
┌──(kali㉿Franco)-[~/picoCTF/forensic3/matryoshkadoll/base_images]
└─$ ls 2_c.jpg   
2_c.jpg                                                                                           
┌──(kali㉿Franco)-[~/picoCTF/forensic3/matryoshkadoll/base_images]
└─$ cd base_images                                                                                             
┌──(kali㉿Franco)-[~/…/forensic3/matryoshkadoll/base_images/base_images]
└─$ ls        
3_c.jpg                                                                                  
┌──(kali㉿Franco)-[~/…/forensic3/matryoshkadoll/base_images/base_images]
└─$ unzip 3_c.jpg 
Archive:  3_c.jpg
warning [3_c.jpg]:  123606 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/4_c.jpg                                                                                                  
┌──(kali㉿Franco)-[~/…/forensic3/matryoshkadoll/base_images/base_images]
└─$ ls
3_c.jpg  base_images                                                                                             
┌──(kali㉿Franco)-[~/…/forensic3/matryoshkadoll/base_images/base_images]
└─$ cd base_images                                                                                 
┌──(kali㉿Franco)-[~/…/matryoshkadoll/base_images/base_images/base_images]
└─$ unzip 4_c.jpg 
Archive:  4_c.jpg
warning [4_c.jpg]:  79578 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: flag.txt                
                                                                                               
┌──(kali㉿Franco)-[~/…/matryoshkadoll/base_images/base_images/base_images]
└─$ ls
4_c.jpg  flag.txt
                                                                                               
┌──(kali㉿Franco)-[~/…/matryoshkadoll/base_images/base_images/base_images]
└─$ cat flag.txt  
picoCTF{e3f378fe6c1ea7f6bc5ac2c3d6801c1f}                                                                             
```
## Notas adicionales

## Referencias