# where are the robots
## Descripción

Can you find the robots?

http://fickle-tempest.picoctf.net:56854
## Solución

```
ingresamos a la página y le añadimos un /robots.txt para que muestre que es lo que esconde 

Nos arroja 
User-agent: *
Disallow: /cc6b1.html

Buscamos la misma página con esa extensión al final y nos da la flag 

http://fickle-tempest.picoctf.net:56854/cc6b1.html

Guess you found the robots  
picoCTF{ca1cu1at1ng_Mach1n3s_cc6b1}
```

picoCTF{ca1cu1at1ng_Mach1n3s_cc6b1}
## Notas adicionales

Aprendimos el uso de robots.txt
## Referencias

https://developers.google.com/crawling/docs/robots-txt/create-robots-txt?hl=es
