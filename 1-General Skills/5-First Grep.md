# First Grep
## Descripción

Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way. The flag is in this [file](https://challenge-files.picoctf.net/c_fickle_tempest/b4b27010334d190b82728db534d40ba520fbcc0b90469bf7db1456c768476c17/file).
## Solución

- Usando Linux:

```
Yeef05-picoctf@webshell:~$ wget https://challenge files.picoctf.net/c_fickle_tempest/b4b27010334d190b82728db534d40ba520f
bcc0b90469bf7db1456c768476c17/file

Yeef05-picoctf@webshell:~$ grep "picoCTF" file

Yeef05-picoctf@webshell:~$ picoCTF{grep_is_good_to_find_things_cEDf1591}
```

picoCTF{grep_is_good_to_find_things_cEDf1591}
## Notas adicionales

Podemos realizar este reto desde la terminal Linux en picoCTF donde tendremos que descargar el archivo con el comando wget "link", y con el comando grep "string a buscar" "archivo" entonces nos muestra el contenido del archivo pero resaltado con rojo la bandera.
## Referencias

https://www.gnu.org/software/grep/manual/grep.html

Manual de como funciona el comando Grep