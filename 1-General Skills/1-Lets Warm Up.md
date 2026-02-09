# Lets Warm Up

## Descripción

If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

## Solución

**Usando python:**
### Solución 1 

- Usando cyberchef: https://gchq.github.io/CyberChef/#recipe=From_Hex('0x')&input=MHg3MA

### Solución 2 

```
>>> int (0x70) #Convierte un hexadecimal a un entero
112
>>> chr(112) #Convierte un entero a carácter
'p'
>>> ord('p') #Convierte un carácter a entero
112
```

picoCTF{p}
## Notas adicionales

- Usamos python para convertir de un hexadecimal a carácter

## Referencias