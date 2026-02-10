# Based
## Descripción

To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337?

Additional details will be available after launching your challenge instance.

Connect with nc fickle-tempest.picoctf.net 53255.
## Solución

- Usando Cyberchef: 
Binario: https://gchq.github.io/CyberChef/#recipe=From_Binary('Space',8)&input=MDExMDAwMDEgMDExMDExMTAgMDExMDEwMDEgMDExMDExMDEgMDExMDAwMDEgMDExMTAxMDAgMDExMDEwMDEgMDExMDExMTEgMDExMDExMTA
Octal: https://gchq.github.io/CyberChef/#recipe=From_Octal('Space')&input=MTY0IDE0MSAxNDIgMTU0IDE0NQ
Hexadecimal: https://gchq.github.io/CyberChef/#recipe=From_Hex('None')&input=NzA2NTYxNzI&oeol=CRLF

```
Yeef05-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 53255
Let us see how data is stored
animation
Please give the 01100001 01101110 01101001 01101101 01100001 01110100 01101001 01101111 01101110 as a word.
...
you have 45 seconds.....

Input:
animation
Please give me the  o164 o141 o142 o154 o145 as a word.
Input:
table
Please give me the 70656172 as a word.
Input:
pear
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_acdCcfCa}
```

picoCTF{learning_about_converting_values_acdCcfCa}
## Notas adicionales
 
En este reto nos proponen convertir ciertos valores a ASCII desde Binario, pasando por Octal y terminando en Hexadecimal.
## Referencias

https://es.wikipedia.org/wiki/Sistema_octal
