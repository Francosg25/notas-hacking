## Objetivo
Sometimes RSA [certificates](https://jupiter.challenges.picoctf.org/static/c882787a19ed5d627eea50f318d87ac5/cert) are breakable
## Solución
```
franco@franco-VirtualBox:~/PicoCTF/Parcial3/john_pollard$ wget https://jupiter.challenges.picoctf.org/static/c882787a19ed5d627eea50f318d87ac5/cert

--2024-11-16 14:31:26--  https://jupiter.challenges.picoctf.org/static/c882787a19ed5d627eea50f318d87ac5/cert

Resolviendo jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8

Conectando con jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)[3.131.60.8]:443... conectado.

Petición HTTP enviada, esperando respuesta... 200 OK

Longitud: 725 [application/octet-stream]

Guardando como: ‘cert’

  

cert            100%[===================>] 725  --.-KB/s en 0s  

  

2024-11-16 14:31:27 (254 MB/s) - ‘cert’ guardado [725/725]

  

franco@franco-VirtualBox:~/PicoCTF/Parcial3/john_pollard$ openssl x509 -pubkey -in cert -out cert.pub

franco@franco-VirtualBox:~/PicoCTF/Parcial3/john_pollard$ openssl rsa -pubin -in cert.pub -text

Public-Key: (53 bit)

Modulus: 4966306421059967 (0x11a4d45212b17f)

Exponent: 65537 (0x10001)

writing RSA key

-----BEGIN PUBLIC KEY-----

MCIwDQYJKoZIhvcNAQEBBQADEQAwDgIHEaTUUhKxfwIDAQAB

-----END PUBLIC KEY-----

  
  

Al meter el numero de modulus a una pagina de factorizacion, nos da la bandera
```

## Notas adicionales

## Referencias
[https://www.alpertron.com.ar/ECM.HTM]
