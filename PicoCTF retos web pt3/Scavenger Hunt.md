## Objetivo
There is some interesting information hidden around this site [http://mercury.picoctf.net:44070/](http://mercury.picoctf.net:44070/). Can you find it?
## Solución
Primeramente vemos el codigo fuente de la pagina que se nos da, ahi nos dan la primera parte de la bandera
```
      <div id="tababout" class="tabcontent">
		<h3>What</h3>
		<p>I used these to make this site: <br/>
		  HTML <br/>
		  CSS <br/>
		  JS (JavaScript)
		</p>
	<!-- Here's the first part of the flag: picoCTF{t -->
```
Despues nos vamos a la hoja de estilos, donde se encuentra la segunda parte 
```
/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */
```
Despues, en el archivo de javascript, nos da una pista que dice que tenemos que entrar al archivo robots.txt, donde se encotrara nuestra otra parte de la bandera
```
User-agent: *
Disallow: /index.html
# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?
```
Con la pista que se nos dio, tenemos que entrar al servidor apache que nos menciona
```
# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.
```
La ultima pista que nos da es que tenemos que entrar al archivo de almacenamiento de mac OS
```
Congrats! You completed the scavenger hunt. Part 5: _7a46d25d}
```
## Notas adicionales

## Referencias