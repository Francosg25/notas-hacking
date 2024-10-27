## Objetivo
My dog-sitter's brother made this website but I can't get in; can you help?[login.mars.picoctf.net](https://login.mars.picoctf.net/)
## Solución
En el codigo fuente de la pagina entramos al script de js
El archivo JavaScript compara el nombre de usuario y la contraseña enviados, codificándolos en base64 para verificar si cumplen con las condiciones de acceso. Usando CyberChef, copiamos el valor que se usa para la comparación de la contraseña y aplicamos la operación "From Base64" para decodificar el texto, revelando la contraseña, que es la bandera
```
picoCTF{53rv3r_53rv3r_53rv3r_53rv3r_53rv3r}
```

## Notas adicionales

## Referencias