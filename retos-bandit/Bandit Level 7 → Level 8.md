## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**
## Datos de acceso al nivel
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
## Solución
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ wc -l data.txt
98567 data.txt
bandit7@bandit:~$ grep -n millionth data.txt
86483:millionth dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
## Notas adicionales
wc -l - cuenta las líneas que tiene un archivo de texto 
grep -n millionth data.txt el comando grep, permite filtrar las líneas de un archivo en base a un patrón 
-n indica a grep que muestre el numero de linea del patrón

## Referencias
