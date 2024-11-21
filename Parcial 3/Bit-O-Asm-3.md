## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt).
## Solución
```
┌──(kali㉿Franco)-[~/picoCTF/reversing/Bit-O-Asm-3]
└─$ ls
disassembler-dump0_c.txt

┌──(kali㉿Franco)-[~/picoCTF/reversing/Bit-O-Asm-3]
└─$ file disassembler-dump0_c.txt 
disassembler-dump0_c.txt: ASCII text
```

Realizamos las operaciones que se hacen para obtener el valor final de `eax`

```
picoCTF{2619997}
```

## Notas adicionales

## Referencias