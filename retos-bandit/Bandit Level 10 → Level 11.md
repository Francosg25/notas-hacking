## Objetivo

The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Datos de acceso al nivel
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

## Solución
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==
bandit10@bandit:~$ file data.txt
data.txt: ASCII text
bandit10@bandit:~$ base64 -d data.txt
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

## Notas adicionales
base64 -d data.txt base64 permite codificar y descodificar cadenas de caracteres
## Referencias
[[https://www.google.com/search?client=firefox-b-d&q=comando+base64+linux]]

