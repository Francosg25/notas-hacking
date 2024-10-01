## Objetivo
How about trying to match a regular expression

Additional details will be available after launching your challenge instance.
## Solución
Primeramente nos vamos al código fuente de la pagina y vemos que esta una expresion de esta forma 
```
<script>
	function send_request() {
		let val = document.getElementById("name").value;
		// ^p.....F!?
		fetch(`/flag?input=${val}`)
			.then(res => res.text())
			.then(res => {
				const res_json = JSON.parse(res);
				alert(res_json.flag)
				return false;
			})
		return false;
	}

```
Introducimos esto en la caja de texto de la pagina y nos da la bandera
```
p.....F!

picoCTF{succ3ssfully_matchtheregex_8ad436ed}
```

## Notas adicionales

## Referencias