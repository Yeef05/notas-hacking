# useless
## Descripción

There's an interesting script in the user's home directory

Additional details will be available after launching your challenge instance.

The work computer is running SSH. We've been given a script which performs some basic calculations, explore the script and find a flag.

```
Hostname: saturn.picoctf.net
Port:     56269
Username: picoplayer
Password: password
```
## Solución

```
Yeef05-picoctf@webshell:~$ ssh -p 57831 picoplayer@saturn.picoctf.net

picoplayer@challenge:~$ ls
useless

picoplayer@challenge:~$ cat uselness #No se encuentra nada en el codio

picoplayer@challenge:~$ man useless #Pero la flag esta en la documentación 

picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_5657}
```

picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_5657}
## Notas adicionales

Usamos un comando para conectarnos por ssh gracias a "-p", nos metemos con la contraseña, checamos el directorio y vemos el script, para ejecutarlo con cat o man.
## Referencias