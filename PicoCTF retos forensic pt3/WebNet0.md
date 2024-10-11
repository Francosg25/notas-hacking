## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
## Solución
```
- Entramos con wireshark y seleccionamos Preferencias/Protocolo/TLS
- Editamos, agregamos la llave y aplicamos los cambios.
- Seleccionamos uno de los paquetes y iremos a HTTP Stream
```
## Notas adicionales

## Referencias