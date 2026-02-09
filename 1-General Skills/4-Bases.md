# Bases
## Descripción

What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.
## Solución

Usando python:

### Solución 1 

- Usando cyberchef: https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YkROaGNtNWZkR2d6WDNJd2NETTE

### Solución 2 

```
>>> import base64
>>> resultado = base64.b64decode("bDNhcm5fdGgzX3IwcDM1").decode()
>>> print(resultado)
l3arn_th3_r0p35
```
 
	picoCTF{l3arn_th3_r0p35}
## Notas adicionales

- Con CyberChef nos dice que es en base64 por lo que sale automáticamente si lo queremos hacer en Linux con python tendremos que importar base64 ya que no hay algun comando por defecto por lo que una vez importemos lo convertimos a bytes "b64decode()" y posteriormente a un string con "decode()"
## Referencias
