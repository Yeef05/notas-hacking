# picobrowser
## Descripción

This website can be rendered only by picobrowser, go and catch the flag!
http://fickle-tempest.picoctf.net:50487
## Solución

- Usando la terminal para cambiar el agente

```
┌──(flavio㉿kali)-[~/Escritorio]
└─$ curl -s http://fickle-tempest.picoctf.net:50487/flag -H 'User-Agent: picobrowser' | grep pico
         <!-- <strong>Title</strong> --> picobrowser!
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}</code></p>

```

picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}
## Notas adicionales

En este caso usamos la terminal para cambiar el agente y filtrar la bandera con grep.
## Referencias

https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Headers/User-Agent
