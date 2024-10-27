## Objetivo
Download this image and find the flag.

- [Download image](https://artifacts.picoctf.net/c/217/pico.flag.png)
## Solución
```
┌──(kali㉿Franco)-[~/parcial2/steg0]
└─$ file pico.flag.png     
pico.flag.png: PNG image data, 585 x 172, 8-bit/color RGBA, non-interlaced
                                                                                               
┌──(kali㉿Franco)-[~/parcial2/steg0]
└─$ zsteg -a pico.flag.png | grep pico
b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_a9a181eb}$t3g0"
/var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s': stack level too deep (SystemStackError)
        from /var/lib/gems/3.1.0/gems/iostruct-0.1.3/lib/iostruct.rb:159:in `inspect'
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.1.0/gems/iostruct-0.1.3/lib/iostruct.rb:159:in `inspect'
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.1.0/gems/iostruct-0.1.3/lib/iostruct.rb:159:in `inspect'
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.1.0/gems/iostruct-0.1.3/lib/iostruct.rb:159:in `inspect'
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
         ... 10066 levels...
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg.rb:26:in `run'
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/bin/zsteg:8:in `<top (required)>'
        from /usr/local/bin/zsteg:25:in `load'
        from /usr/local/bin/zsteg:25:in `<main>'

```

## Notas adicionales

## Referencias