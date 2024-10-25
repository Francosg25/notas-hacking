## Objetivo
How about some hide and seek heh? Look at this image [here](https://artifacts.picoctf.net/c/235/atbash.jpg).
## Solución
```
┌──(kali㉿Franco)-[~/picoCTF/crypto3/hidetoseeme]
└─$ file atbash.jpg 
atbash.jpg: JPEG image data, JFIF standard 1.01, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 465x455, components 3
                                                                                                  
┌──(kali㉿Franco)-[~/picoCTF/crypto3/hidetoseeme]
└─$ strings atbash.jpg | grep pico
                                                                                                  
┌──(kali㉿Franco)-[~/picoCTF/crypto3/hidetoseeme]
└─$ exiftool atbash.jpg
ExifTool Version Number         : 12.76
File Name                       : atbash.jpg
Directory                       : .
File Size                       : 52 kB
File Modification Date/Time     : 2023:03:15 23:16:32-04:00
File Access Date/Time           : 2024:10:24 19:59:47-04:00
File Inode Change Date/Time     : 2024:10:24 19:59:31-04:00
File Permissions                : -rw-rw-r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Image Width                     : 465
Image Height                    : 455
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 465x455
Megapixels                      : 0.212

```

Instalamos la herramienta de `Steghide` para extraer el texto de la imagen 
```
                                                                                                  
┌──(kali㉿Franco)-[~/picoCTF/crypto3/hidetoseeme]
└─$ steghide --extract -sf atbash.jpg
Enter passphrase: 
wrote extracted data to "encrypted.txt".
                                                                                                  
┌──(kali㉿Franco)-[~/picoCTF/crypto3/hidetoseeme]
└─$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_92533667}
```

Y con la ayuda de cyberchef desencriptamos esto aplicandole `Atbash Cipher` 
```
picoCTF{atbash_crack_92533667}


```
## Notas adicionales

## Referencias