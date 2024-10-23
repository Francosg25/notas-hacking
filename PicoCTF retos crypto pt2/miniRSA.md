## Objetivo
Let's decrypt this: [ciphertext](https://jupiter.challenges.picoctf.org/static/d21037ad23ed84cfff20a84768a0f2b2/ciphertext)? Something seems a bit small.
## Solución
Se ejecuta ese codigo en python
```
from gmpy2 import *

gmpy2.get_context().precision = 2048

n = 293319224997949857827359760455911649366830593805589503865601601057403432>
e= 3
c = 220531641393113403107460374692824779903015522125251987265007301078204917>

for t in range(10000):
        m, tr = iroot(t*n + c, e)
        if tr:
                print('Encontre t : ' + str(t))
                print('Flag       : ' + str(bytes.fromhex(hex(m)[2:]).decode>
```
## Notas adicionales
- gmpy2.get_context().precision = 2048: Ajusta la precisión de los cálculos numéricos a 2048 bits para trabajar con números grandes.
- el bucle recorre diferentes valores de t desde 0 hasta 9999.
    - Dentro del bucle, para cada valor de t, intenta resolver la ecuación m^e=t∗n+c m^e = t * n + cme=t * n+c. Es decir, trata de encontrar el mensaje original mmm resolviendo la raíz cúbica (debido a que e=3e = 3e=3) de t∗n+ct * n + ct∗n+c.
    
    - iroot(t * n + c, e): Calcula la raíz cúbica de t∗n+ct ** n + ct * n+c y devuelve dos valores:
        
        - m: el posible valor del mensaje (el resultado de la raíz cúbica).
        - r: un valor booleano que indica si la raíz encontrada es exacta.
    - Si r es verdadero, significa que el valor calculado mmm es una raíz cúbica exacta y probablemente sea el mensaje original.
        
    - En ese caso, imprime el valor de t y convierte el mensaje m de formato hexadecimal a texto, con el cual se revela la bandera

## Referencias