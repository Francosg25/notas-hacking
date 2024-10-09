## Objetivo
Decode this [message](https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav) from the moon.
## Solution
```
┌──(kali㉿Franco)-[~/picoCTF/forensic2]
└─$ wget https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav
--2024-10-07 12:14:09--  https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 11066998 (11M) [application/octet-stream]
Saving to: ‘message.wav’
message.wav             100%[==============================>]  10.55M   335KB/s    in 34s     
2024-10-07 12:14:51 (322 KB/s) - ‘message.wav’ saved [11066998/11066998]
```
Clonamos un repositorio donde viene un programa, que nos ayuda a convertir audios a imagenes
```
┌──(kali㉿Franco)-[~/picoCTF/forensic2/m00nwalk]
└─$ sudo git clone https://github.com/colaclanth/sstv  
Cloning into 'sstv'...
```
Usamos este programa para convertir el audio a imagen
```
┌──(kali㉿Franco)-[~/picoCTF/forensic2/m00nwalk/sstv]
└─$ python setup.py install
running install
/usr/lib/python3/dist-packages/setuptools/_distutils/cmd.py:66: SetuptoolsDeprecationWarning: setup.py install is deprecated.
```
## Notas adicionales

## Referencias