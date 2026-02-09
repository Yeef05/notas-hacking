# Nice netcat
## Descripción

There is a nice program that you can talk to by using this command in a shell:

Additional details will be available after launching your challenge instance.

$ nc wily-courier.picoctf.net 60057, but it doesn't speak English...
## Solución

- Usando Linux:

```
Yeef05-picoctf@webshell:~$ nc wily-courier.picoctf.net 60057
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
100 
57 
52 
55 
54 
125 
10
```

- Usando Python:

```
>>> numeros = [112, 105, 99, 111, 67, 84, 70, 123, 103, 48, 48, 100, 95, 107, 49, 116, 116, 121, 33, 95, 110, 49, 99, 51, 95, 107, 49, 116, 116, 121, 33, 95, 100, 57, 52, 55, 54, 125]
>>> mensaje = "".join(chr(n) for n in numeros)
>>> print(mensaje)
picoCTF{g00d_k1tty!_n1c3_k1tty!_d9476}
```

picoCTF{g00d_k1tty!_n1c3_k1tty!_d9476}

## Notas adicionales
 
En este reto usamos lo aprendido de "nc- Netcat" y lo aprendido de ASCII en Python hacemos uso de netcat usando el host y puerto que nos dan, en las pistas nos dicen casi directamente que tendremos que convertir ASCII por lo que podemos intuir que nos dan números en base10 y que solo tenemos que pasar a ASCII, por lo que python por defecto tiene el comando "chr()" para transformar en ASCII así que solo hacemos un ciclo rápido para convertir y sacar la flag  
## Referencias