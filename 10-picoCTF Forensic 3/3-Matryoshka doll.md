# Matryoshka doll

## Descripción

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [dolls.jpg](https://challenge-files.picoctf.net/c_wily_courier/feaddb84eaaa2f8d6b83bda9e7a9c46a86474361e095fea9ee3840873f3506b4/dolls.jpg)
## Solución

```
┌──(flavio㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ ls
4_c.jpg  _4_c.jpg.extracted
                                                                                                                                                                                                                                           
┌──(flavio㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ cd _4_c.jpg.extracted 
                                                                                                                                                                                                                                           
┌──(flavio㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ la                   
136DA.zip  flag.txt
                                                                                                                                                                                                                                           
┌──(flavio㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ cat flag.txt         
picoCTF{LL9lb1dR4QbGe4l4iWCvGq9pdtwt7392}
```

picoCTF{LL9lb1dR4QbGe4l4iWCvGq9pdtwt7392}
## Notas adicionales

Usamos binwalk para extraer archivos dentro de una imagen hasta que encontramos un archivo .txt con la flag.
## Referencias
