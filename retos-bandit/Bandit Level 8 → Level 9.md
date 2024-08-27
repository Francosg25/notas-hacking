## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de acceso al nivel
bandit8 dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
## Solución
bandit8@bandit:~$ sort data.txt | uniq -u

4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
## Notas adicionales
sort data.txt | uniq -u sort ordena las líneas de texto en orden alfabético | - redirige la salida de un comando y la pasa al siguiente comando (pipe) uniq - filtra las líneas que son únicas
## Referencias

