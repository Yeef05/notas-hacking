# PW Crack 2
## Descripción

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
## Solución

```
Yeef05-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/14/level2.py

Yeef05-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/14/level2.flag.txt.enc

Yeef05-picoctf@webshell:~$ nano level2.py

Yeef05-picoctf@webshell:~$ python3
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39)
'4ec9'
>>> exit()
>>> 
Yeef05-picoctf@webshell:~$ python3 level2.py
Please enter correct password for flag: 4ec9     
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}
```

picoCTF{tr45h_51ng1ng_9701e681}
## Notas adicionales

De igual manera nos metemos con "nano" vemos que la contraseña esta en hexadecimal, la convertimos a carácter con python y ya podemos meter la contraseña para recibir la flag. 
## Referencias

