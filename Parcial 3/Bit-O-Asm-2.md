## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).
## Solución
```
┌──(kali㉿Franco)-[~/picoCTF/reversing/Bit-O-Asm-2]
└─$ ls
disassembler-dump0_b.txt

┌──(kali㉿Franco)-[~/picoCTF/reversing/Bit-O-Asm-2]
└─$ file disassembler-dump0_b.txt 
disassembler-dump0_b.txt: ASCII text

```

En la línea <+22>, transferimos el valor desde la dirección señalada por el puntero base a `eax`, donde se almacena. Luego, convertimos el valor `0x9fe1a` de hexadecimal a decimal, obteniendo el número 654874, el cual corresponde a la bandera.

```
picoCTF{654874}
```
## Notas adicionales

## Referencias
