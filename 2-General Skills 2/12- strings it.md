# strings it
## Descripción

Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/a35dc624cfda858ed12a4bce57f832dad3b433bad6cde2b98e25fae4bc8ff760/strings) without running it?
## Solución

```
Yeef05-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_fickle_tempest/a35dc624cfda858ed12a4bce57f832dad3b433bad6cde2b98e25fae4bc8ff760/strings

Yeef05-picoctf@webshell:~$ grep -ao "picoCTF{[^}]*}" strings
picoCTF{5tRIng5_1T_60eA8fdA}
```

picoCTF{5tRIng5_1T_60eA8fdA}
## Notas adicionales
 
Seguimos usando grep pero con 2 opciones nuevas "-a" para que muestre binarios y "-o" para que muestre solo el texto solicitado y por ultimo "[^}]*" que mostrara todo lo que haya entre las llaves.

## Referencias

