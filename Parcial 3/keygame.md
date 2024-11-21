## Objetivo
[keygenme-trial.py](https://mercury.picoctf.net/static/0c363291c47477642c72630d68936e50/keygenme-trial.py)
## Solución
Creamos un programa para descifrar la bandera
```
import hashlib
import base64


key_part_static1_trial = "picoCTF{1n_7h3_|<3y_of_"
key_part_dynamic1_trial = "xxxxxxxx"
key_part_static2_trial = "}"
key_full_template_trial = key_part_static1_trial + key_part_dynamic1_trial + key_part_static2_trial

username_trial = b"FRASER"

potential_dynamic_key = ""

offset = 23

positions = [4,5,3,6,2,7,1,8]

for p in positions:
    potential_dynamic_key += hashlib.sha256(username_trial).hexdigest()[p]

key = key_part_static1_trial + potential_dynamic_key + key_part_static2_trial
print(key)
print(len(key))
```

```
picoCTF{1n_7h3_|<3y_of_ac73dc29}
```
## Notas adicionales

## Referencias