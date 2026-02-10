# Wave a flag
## Descripción

Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...[warm](https://challenge-files.picoctf.net/c_wily_courier/70013ed41d4cfe2bb48628471dac6fc12238b5dbe164301ae3b4e35277b1e80b/warm)
## Solución

```
Yeef05-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/70013ed41d4cfe2bb48628471dac6fc12238b5dbe164301ae3b4e35277b1e80b/warm

Yeef05-picoctf@webshell:~$ chmod +x warm
Yeef05-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!

Yeef05-picoctf@webshell:~$ ./warm --help
I don't know what '--help' means! I do know what -h means though!

Yeef05-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
```

picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
## Notas adicionales

Una introducción a como hacer un archivo ejecutable y como correrlo
## Referencias
