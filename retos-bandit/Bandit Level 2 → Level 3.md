## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory
## Datos de acceso al nivel
bandit2 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

## Solución
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces in this film
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: film: No such file or directory
bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
bandit2@bandit:~$ cat "spaces in this filename"
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
bandit2@bandit:~$
## Notas adicionales
Si el nombre del archivo contiene espacios - usar \ antes del espacio para cada espacio - delimitar el nombre del archivo con ""

## Referencias

