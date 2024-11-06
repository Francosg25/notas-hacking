## Objetivo
What does asm2(0xb,0x2e) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/717467c8c8b4332ea5873ad8fe7b2dad/test.S)
## Solución
```
┌──(kali㉿Franco)-[~/picoCTF/reversing3/asm2]
└─$ python3
Python 3.12.6 (main, Sep  7 2024, 14:20:15) [GCC 14.2.0]
Type "help", "copyright", "credits" or "license" for mor
>>> 0xb <= 0x63f3
True
>>> hex(0x2e + 0x1)
'0x2f'
>>> 0xb - 0xffffff80
-4294967157
>>> hex(0xb+128)
'0x8b'                                                  
>>> 0x8b <= 0x63f3                                      
True                                                    
>>>
```

```
>>> import numpy
>>> numpy.int32(0xffffff80)
<stdin>:1: DeprecationWarning: NumPy will stop allowing conversion of out-of-bound Python integers to integer arrays.  The conversion of 4294967168 to int32 will fail in the future.
For the old behavior, usually:
    np.array(value).astype(dtype)
will give the desired result (the cast overflows).
-128
>>> 0x63f3 / 128
199.8984375
>>> int(0xb)
11
>>> hex(246)
'0xf6'
>>> 
```
## Notas adicionales

## Referencias