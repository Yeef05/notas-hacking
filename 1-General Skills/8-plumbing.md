# plumbing
## Descripción

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?

Additional details will be available after launching your challenge instance.

Connect to fickle-tempest.picoctf.net 61279.
## Solución

- Usando Linux:

```
Yeef05-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 61279 | grep picoCTF
picoCTF{digital_plumb3r_8c8f3412}
```

picoCTF{digital_plumb3r_8c8f3412}
## Notas adicionales

Este reto pone a prueba lo aprendido anteriormente, nos da un host y puerto para conectarnos pero tiene muchas salidas así que hacemos uso de grep aprendido anteriormente para filtrar las salidas a una que tenga como coincidencia el inicio de la flag "picoCTF"
## Referencias
