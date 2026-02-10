# Static ain't always noise
## Descripción

Can you look at the data in this binary? The bash script might help![static](https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/static), [ltdis.sh](https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/ltdis.sh)
## Solución

```
Yeef05-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/ad443900e4d8d8e6d0f3250730125d24ce6ceaf10ab38658eaafc175eee37422/static

Yeef05-picoctf@webshell:~$ grep -a "picoCTF" static

?      oooo=@picoCTF{d15a5m_t34s3r_20335e41}GCC: (Ubuntu 9.4.0-1ubuntu1~20.04.2) 9.4.08X|p
```

picoCTF{d15a5m_t34s3r_20335e41}
## Notas adicionales

Sin necesidad de la herramienta ltdish.sh podemos hacer que muestre los valores binarios con un "-a" y al ver que no tiene mucho texto resalta la flag inmediatamente.
## Referencias