# PW Crack 3
## Descripción

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución

```
Yeef05-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.py

Yeef05-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc

Yeef05-picoctf@webshell:~$ wget
https://artifacts.picoctf.net/c/17/level3.hash.bin

Yeef05-picoctf@webshell:~$ bvi level3.hash.bin

Yeef05-picoctf@webshell:~$ python3 level3.py
Please enter correct password for flag: 87ab             
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
```

picoCTF{m45h_fl1ng1ng_cd6ed2eb}
## Notas adicionales

Nos metemos al archivo hash que descargamos el cual esta en hexadecimal esa linea la juntamos y ponemos todo en minúsculas, posteriormente usamos una pagina convertidora de hash para que nos de la contraseña y nos den la flag con el programa .py
## Referencias

https://crackstation.net