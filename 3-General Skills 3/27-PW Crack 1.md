# PW Crack 1
## Descripción

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.
## Solución

```
Yeef05-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.py

Yeef05-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc

Yeef05-picoctf@webshell:~$ nano level1.py

Yeef05-picoctf@webshell:~$ python3 level1.py
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
```

picoCTF{545h_r1ng1ng_fa343060}
## Notas adicionales

Al igual que los retos anteriores tenemos que meternos al archivo .py con "nano" para así ver cual es la contraseña.
## Referencias