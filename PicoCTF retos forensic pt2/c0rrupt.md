## Objetivo
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
## Solución
- Instalamos la herramienta `pngcheck` para que nos ayude a identificar que errores contiene la imagen
```
```shell
┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ sudo apt install pngcheck                                 

...

┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ pngcheck -v flag.png 
zlib warning:  different version (expected 1.2.13, using 1.3.1)

File: flag.png (202940 bytes)
  invalid chunk name "C"DR" (43 22 44 52)
ERRORS DETECTED in flag.png

┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ hexeditor flag.png
```

- Buscamos el hexadecimal 43 22 44 52 y lo cambiamos por 49 49 44 52.

```
┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ eog flag.png     

┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ file flag.png 
flag.png: PNG image data, 1642 x 1095, 8-bit/color RGB, non-interlaced

┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ pngcheck -v flag.png
zlib warning:  different version (expected 1.2.13, using 1.3.1)

File: flag.png (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 2852132389x5669 pixels/meter
  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)
ERRORS DETECTED in flag.png

┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ hexeditor flag.png 
```

- Cambiamos la resolución cambiando en la línea 00000040 el AA por 00.

```
┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ eog flag.png       

┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ file flag.png       
flag.png: PNG image data, 1642 x 1095, 8-bit/color RGB, non-interlaced

┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ pngcheck -v flag.png
zlib warning:  different version (expected 1.2.13, using 1.3.1)

File: flag.png (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in flag.png

┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ hexeditor flag.png
```

- Cambiamos en la línea 00000050 AA AA por 00 00.

```
┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ open flag.png 

┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ pngcheck -v flag.png
zlib warning:  different version (expected 1.2.13, using 1.3.1)

File: flag.png (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
  invalid chunk name "�DET" (ffffffab 44 45 54)
ERRORS DETECTED in flag.png

┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ open flag.png       

┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ hexeditor flag.png
```

- Modificamos la línea 00000050 para que quedara de la siguiente manera:

```shell
00000050  52 24 F0 00  00 FF A5 49   44 41 54 78  5E EC BD 3F

┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ open flag.png

┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ 
```

```shell
picoCTF{c0rrupt10n_1847995}
```

## Notas adicionales

## Referencias