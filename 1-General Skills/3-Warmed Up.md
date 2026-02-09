# Warmed Up
## Descripción

What is 0x3D (base 16) in decimal (base 10)?
## Solución

**Usando python:**
### Solución 1 

- Usando cyberchef: https://gchq.github.io/CyberChef/#recipe=To_Base(10)&input=MFgzRA

### Solución 2 

```
>>> int(0x3D)
61
```
 
picoCTF{61}
## Notas adicionales

- En cyberchef toma el prefijo "0x" para tomarlo como un valor hexadecimal (base16) por lo que solo hace falta decirlo que lo convierta a base10 , y en python solo basta con usar (int()) para transformar de un hexadecimal a un entero
## Referencias