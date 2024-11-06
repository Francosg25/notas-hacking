## Objetivo
asm3(0xba6c5a02,0xd101e3dd,0xbb86a173) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/cb753ae52bca4aa303deca5fbfb01bfb/test.S)
## Solución
```
asm3:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   xor    eax,eax
        <+5>:   mov    ah,BYTE PTR [ebp+0xb]
        <+8>:   shl    ax,0x10
        <+12>:  sub    al,BYTE PTR [ebp+0xd]
        <+15>:  add    ah,BYTE PTR [ebp+0xc]
        <+18>:  xor    ax,WORD PTR [ebp+0x12]
        <+22>:  nop
        <+23>:  pop    ebp
        <+24>:  ret 
```

Con un emulador en lenguaje maquina logramos obtener el resultado al ver los registros
```
0x669B
```
## Notas adicionales

## Referencias