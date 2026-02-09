# whats a net cat
## Descripción

Additional details will be available after launching your challenge instance.

This challenge launches an instance on demand.  
Its current status is: `NOT_RUNNING`

Using netcat (nc) is going to be pretty important. Can you connect to fickle-tempest.picoctf.net at port 49888 to get the flag?
## Solución

- Usando Linux:

```
Yeef05-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 49888
You're on your way to becoming the net cat master
picoCTF{nEtCat_Mast3ry_95035DAa}
```

picoCTF{nEtCat_Mast3ry_95035DAa}
## Notas adicionales

Para este reto es parecido al anterior solamente debemos tener en cuenta como funciona nc, una vez que sabemos como funciona solo es usarlo con el host y el puerto que nos den y nos da de resultado la flag
## Referencias

https://linuxize.com/post/netcat-nc-command-with-examples/

Con esta pagina enseña algunos usos y como funciona netcat

"nc [options] host port"