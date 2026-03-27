# hideme

## Descripción

Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/257/flag.png).
## Solución

```
┌──(flavio㉿kali)-[~/picoCTF/t3forensic/hideme]
└─$ binwalk -e flag.png    

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2959, uncompressed size: 3108, name: secret/flag.png

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented

                                                                                                                                                                                                                                           
┌──(flavio㉿kali)-[~/picoCTF/t3forensic/hideme]
└─$ ls
flag.png  _flag.png.extracted
                                                                                                                                                                                                                                           
┌──(flavio㉿kali)-[~/picoCTF/t3forensic/hideme]
└─$ cd _flag.png.extracted 
                                                                                                                                                                                                                                           
┌──(flavio㉿kali)-[~/picoCTF/t3forensic/hideme/_flag.png.extracted]
└─$ ls
29  29.zlib  9B3B.zip  secret
                                                                                                                                                                                                                                           
┌──(flavio㉿kali)-[~/picoCTF/t3forensic/hideme/_flag.png.extracted]
└─$ cd secret             
                                                                                                                                                                                                                                           
┌──(flavio㉿kali)-[~/…/t3forensic/hideme/_flag.png.extracted/secret]
└─$ ls
flag.png

┌──(flavio㉿kali)-[~/…/t3forensic/hideme/_flag.png.extracted/secret]
└─$ open flag.png 
```

picoCTF{Hiddinng_An_imag3_within_@n_ima9e_dc2ab58f}
## Notas adicionales

Extraemos archivos ocultos en una imagen
## Referencias
