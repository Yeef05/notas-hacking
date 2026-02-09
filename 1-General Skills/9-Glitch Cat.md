# Glitch Cat
## Descripción

Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance.

$ nc saturn.picoctf.net 63276
## Solución

- Usando Linux:

```
Yeef05-picoctf@webshell:~$ nc saturn.picoctf.net 63276
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
```

- Usando Python:

```
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
'picoCTF{gl17ch_m3_n07_bda68f75}'
```

picoCTF{gl17ch_m3_n07_bda68f75}
## Notas adicionales

Como anteriormente resolvimos nos dan el comando nc con un host y un puerto con la flag pero esta "incompleta" ya que muestra algunas letras en hexadecimal pero con el comando de Python para convertirlas a letra "chr" por lo que solo tenemos que copiar la flag glicheada y pegarla en python ya que los comandos de python automáticamente convierten todo a carácter. 
## Referencias