## Objetivo
Why search for the flag when I can make a bookmarklet to print it for me?

Additional details will be available after launching your challenge instance.
## Solución
Se nos da una instancia y nos metemos a la pagina que se nos da, ahi adentro nos da un codigo, ese codigo lo introducimos en la consola de la inspeccion de pagina
```
        javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓË¨ËÓ§Èí";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
    
```
Al final nos da la bandera
```
picoCTF{p@g3_turn3r_e8b2d43b}
```
## Notas adicionales

## Referencias