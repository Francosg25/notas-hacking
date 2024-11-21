## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/511/disassembler-dump0_d.txt).
## Solución
El texto nos da esto:
```
<+15>: Almacena 0x9fe1a en la ubicación de memoria apuntada por [rbp-0x4].
<+22>: Compara [rbp-0x4] con 0x2710.
<+29>: Salta a la instrucción en <+37> si [rbp-0x4] es menor o igual a 0x2710 (NO lo es).
<+31>: Resta 0x65 de [rbp-0x4] y almacenar el resultado en [rbp-0x4].
<+35>: Salta a <+41>.
<+37>: [NO EJECUTADO].
<+41>: Almacena el valor apuntado por [rbp-0x4] en el registro eax.
```
Realizamos las operaciones para tener el valor final


## Notas adicionales

## Referencias