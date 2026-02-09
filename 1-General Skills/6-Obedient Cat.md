# Obedient Cat
## Descripción

This file has a flag in plain sight (aka "in-the-clear").[flag](https://challenge-files.picoctf.net/c_wily_courier/4acf636990e4540d6fc36684b1256e625c0617d7cb01727e12e3f9606d89fe45/flag)
## Solución

- Usando Linux:

```
Yeef05-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/4acf636990e4540d6fc36684b1256e625c0617d7cb01727e12e3f9606d89fe45/flag

Yeef05-picoctf@webshell:~$ man cat

Yeef05-picoctf@webshell:~$ cat flag

picoCTF{s4n1ty_v3r1f13d_9b8fa0bc}
```

picoCTF{s4n1ty_v3r1f13d_9b8fa0bc}
## Notas adicionales

Para la resolución de este reto en las mismas pistas nos piden usar "wget" para descargar el archivo y "man cat" lo cual nos permite revisar algunas de las funciones de cat, para resolver el reto podemos solo usar "cat flag" y nos arrojara la flag en la consola, de la otra manera es desde "man cat" usar "E" para examinar y escribir el nombre del archivo "flag" y de igual manera tendremos el resultado.
## Referencias
