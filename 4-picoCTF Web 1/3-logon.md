# logon
## Descripción

The factory is hiding things from all of its users.

Can you login as Joe and find what they've been looking at? http://fickle-tempest.picoctf.net:54315
## Solución

- Usando cookie editor

```
https://addons.mozilla.org/en-US/firefox/addon/cookie-editor/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search

ingresamos a la página como 
admin
1234

como admin tiene cookies False con cookie editor las cambiamos a True y refresacmos la página

**Flag**: `picoCTF{th3_c0nsp1r4cy_l1v3s_4d184b0d}`
```

picoCTF{th3_c0nsp1r4cy_l1v3s_4d184b0d}
## Notas adicionales

Aprendemos el uso de headers y cookies
## Referencias

https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Headers

https://developer.mozilla.org/en-US/docs/Glossary/Request_header

https://developer.mozilla.org/es/docs/Web/HTTP/Guides/Cookies