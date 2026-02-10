# repetitions
## Descripción

Can you make sense of this file?Download the file [here](https://artifacts.picoctf.net/c/471/enc_flag).
## Solución

```
Yeef05-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/471/enc_flag

Yeef05-picoctf@webshell:~$ ls
Addadshashanammu      README.txt  ltdis.sh  strings
Addadshashanammu.zip  enc_flag    static    warm

Yeef05-picoctf@webshell:~$ cat enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_9b59b35c}
```

picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_9b59b35c}
## Notas adicionales

El texto estaba cifrado varias veces en base64 por lo que se decodifico hasta llegar a la flag.
## Referencias