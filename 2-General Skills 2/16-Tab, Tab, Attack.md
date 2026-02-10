# Tab, Tab, Attack
## Descripción

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames.[Addadshashanammu.zip](https://challenge-files.picoctf.net/c_wily_courier/56f53a4189949d066fe969e998769a4e0390123be59782c06e6c0a52c78403e2/Addadshashanammu.zip)

## Solución

```
Yeef05-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/56f53a4189949d066fe969e998769a4e0390123be59782c06e6c0a52c78403e2/Addadshashanammu.zip

picoplayer@challenge:~$ unzip Addadshashanammu.zip

Yeef05-picoctf@webshell:~$ ls 
Addadshashanammu  Addadshashanammu.zip  README.txt  ltdis.sh  static  strings  warm

Yeef05-picoctf@webshell:~$ cd Addadshashanammu
Yeef05-picoctf@webshell:~/Addadshashanammu$ cd Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/

Yeef05-picoctf@webshell:~/Addadshashanammu$ cd Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/

Yeef05-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitash
pi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet  fang-of-haynekhtnamet.c

Yeef05-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitash
pi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet

*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
```

picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
## Notas adicionales

Descargamos un archivo zip, lo descomprimimos y posteriormente llegamos hasta la ultima carpeta con varios tap, comprobamos que archivos hay con un "ls" y ejecutamos el script que hay ahí el cual nos da la flag.
## Referencias