## Objetivo
Download this image file and find the flag.

[Download image file](https://artifacts.picoctf.net/c/102/drawing.flag.svg)
## Solución
```
┌──(kali㉿Franco)-[~/parcial2/enhance]
└─$ wget https://artifacts.picoctf.net/c/102/drawing.flag.svg
--2024-10-24 17:08:15--  https://artifacts.picoctf.net/c/102/drawing.flag.svg
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.21.85, 13.249.21.46, 13.249.21.66, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.21.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4149 (4.1K) [application/octet-stream]
Saving to: ‘drawing.flag.svg’

drawing.flag.svg        100%[==============================>]   4.05K  --.-KB/s    in 0s      

2024-10-24 17:08:15 (48.0 MB/s) - ‘drawing.flag.svg’ saved [4149/4149]

                                                                                               
┌──(kali㉿Franco)-[~/parcial2/enhance]
└─$ strings drawing.flag.svg | grep tspan                                           
       id="text3723"><tspan
         id="tspan3748">p </tspan><tspan
         id="tspan3754">i </tspan><tspan
         id="tspan3756">c </tspan><tspan
         id="tspan3758">o </tspan><tspan
         id="tspan3760">C </tspan><tspan
         id="tspan3762">T </tspan><tspan
         id="tspan3764">F { 3 n h 4 n </tspan><tspan
         id="tspan3752">c 3 d _ d 0 a 7 5 7 b f }</tspan></text>

```

picoCTF{3nh4nc3d_d0a757bf}
## Notas adicionales

## Referencias