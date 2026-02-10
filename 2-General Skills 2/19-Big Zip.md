# Big Zip
## Descripción

Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/503/big-zip-files.zip)
## Solución

```
Yeef05-picoctf@webshell:~$ grep -r "picoCTF{[^}]*}"

big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
```

picoCTF{gr3p_15_m4g1c_ef8790dc}
## Notas adicionales

Se usa grep para buscar en carpetas con "-r".
## Referencias