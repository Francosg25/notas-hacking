## Objetivo
We found a brand new type of encryption, can you break the secret code? (Wrap with picoCTF{}) `apbopjbobpnjpjnmnnnmnlnbamnpnononpnaaaamnlnkapndnkncamnpapncnbannaapncndnlnpna` [new_caesar.py](https://mercury.picoctf.net/static/d8a6722e08659449dd091668c0c9bbca/new_caesar.py)
## Solución

Revisamos el codigo que se nos dio, y modificamos un codigo extra para que nos de la bandera
```
import string

  

LOWERCASE_OFFSET = ord("a")

ALPHABET = string.ascii_lowercase[:16]

  

def b16_decode(cipher):

    dec = ""

    for c in range(0, len(cipher), 2):

        b = ""

        b += "{0:04b}".format(ALPHABET.index(cipher[c]))

        b += "{0:04b}".format(ALPHABET.index(cipher[c + 1]))

        dec += chr(int(b, 2))

    return dec

  

def unshift(c, k):

    t1 = ord(c) - LOWERCASE_OFFSET

    t2 = ord(k) - LOWERCASE_OFFSET

    return ALPHABET[(t1 - t2) % len(ALPHABET)]

  

enc= "apbopjbobpnjpjnmnnnmnlnbamnpnononpnaaaamnlnkapndnkncamnpapncnbannaapncndnlnpna"

  
  

for key in ALPHABET:

    s = ""

    for i, c in enumerate(enc):

        s += unshift(c, key[i % len(key)])

    s = b16_decode(s)

    print(s)
```

```
picoCTF{et_tu?_23217b54456fb10e908b5e87c6e89156}
```

## Notas adicionales

## Referencias