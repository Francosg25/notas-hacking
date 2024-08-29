## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
## Datos de acceso al nivel
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
## Solución
bandit14@bandit:~$ which nc
/usr/bin/nc
bandit14@bandit:~$ nc localhost 30000
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
Correct!
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
## Notas adicionales
nc - es una herramienta que permite conectarse a un host remoto, también podemos abrir un puerto nc localhost 30000 localhost - es el host o la maquina a la que me quiero conectar 30000 - es el puerto que esta abierto en esa maquina
## Referencias
[Netcat wikipedia](https://es.wikipedia.org/wiki/Netcat)
