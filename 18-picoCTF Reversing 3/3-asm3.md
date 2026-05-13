# asm3

## Descripción

What does asm3(0xc2cb1015,0xb886b227,0xee8ecb38) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/dc2affc42a0374a7e3d3b2f4936eb083fa4ade553b99c00b2002eb3bd024664c/test.S)
## Solución

```
1.-Descargamos el archivo y lo mostramos

┌──(flavio㉿kali)-[~/picoCTF/Reversing/act3/asm3]
└─$ cat test.S   
asm3:
        <+0>:   endbr32 
        <+4>:   push   ebp
        <+5>:   mov    ebp,esp
        <+7>:   xor    eax,eax
        <+9>:   mov    ah,BYTE PTR [ebp+0x9]
        <+12>:  shl    ax,0x10
        <+16>:  sub    al,BYTE PTR [ebp+0xf]
        <+19>:  add    ah,BYTE PTR [ebp+0xe]
        <+22>:  xor    ax,WORD PTR [ebp+0x12]
        <+26>:  nop
        <+27>:  pop    ebp
        <+28>:  ret   
        
2.-Hacerle un nano y añadir esto al principio (los parámetros en Little Endian) que da en la descripción "What does asm3(0xc2cb1015,0xb886b227,0xee8ecb38) return?"

stack

0000

[ ebp ] <- esp <- ebp
[ ret ] <- ebp + 0x4
[ param1 ] <- ebp + 0x8   (0xc2cb1015 -> En memoria: 15 10 cb c2)
[ param2 ] <- ebp + 0xc   (0xb886b227 -> En memoria: 27 b2 86 b8)
[ param3 ] <- ebp + 0x10  (0xee8ecb38 -> En memoria: 38 cb 8e ee)
fffff

registres
eax = 00 00 00 00
(ax son los 16 bits más bajos, ah y al son los 8 bits altos y bajos de ax respectivamente)

3.-Dividimos la terminal y corremos python para simular el comportamiento de los registros y la memoria (Little Endian)

┌──(flavio㉿kali)-[~/picoCTF/Reversing/act3/asm3]
└─$ python3
Python 3.10.8 (main, Nov  4 2022, 09:21:25) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> # <+7>: xor eax,eax -> Limpia el registro eax (eax = 0)
>>> ax = 0x0000
>>> # <+9>: mov ah,BYTE PTR [ebp+0x9]
>>> # param1 (ebp+0x8) en memoria es: [0x8]=0x15, [0x9]=0x10, [0xa]=0xcb, [0xb]=0xc2
>>> # Tomamos el byte en 0x9, que es 0x10
>>> ah = 0x10
>>> ax = 0x1000 # (ax se compone de ah y al, al es 00)
>>> 
>>> # <+12>: shl ax,0x10
>>> # Desplazar 16 bits a la izquierda (shl) un registro de 16 bits (ax) hace que todos los bits salgan. Se convierte en 0.
>>> ax = 0x0000
>>> 
>>> # <+16>: sub al,BYTE PTR [ebp+0xf]
>>> # param2 (ebp+0xc) en memoria: [0xc]=0x27, [0xd]=0xb2, [0xe]=0x86, [0xf]=0xb8
>>> # Restamos a 'al' (0x00) el byte en 0xf (0xb8)
>>> al = (0x00 - 0xb8) & 0xFF  # Simular resta de 8 bits
>>> hex(al)
'0x48'
>>> ax = 0x0048 # (actualizamos ax con el nuevo al)
>>> 
>>> # <+19>: add ah,BYTE PTR [ebp+0xe]
>>> # Sumamos a 'ah' (0x00) el byte en 0xe (0x86)
>>> ah = (0x00 + 0x86) & 0xFF
>>> hex(ah)
'0x86'
>>> ax = 0x8648 # (juntamos ah y al para formar el nuevo ax)
>>> 
>>> # <+22>: xor ax,WORD PTR [ebp+0x12]
>>> # param3 (ebp+0x10) en memoria: [0x10]=0x38, [0x11]=0xcb, [0x12]=0x8e, [0x13]=0xee
>>> # WORD PTR en ebp+0x12 toma 2 bytes leyendo al revés (Little Endian): 0xee8e
>>> ax = ax ^ 0xee8e
>>> hex(ax)
'0x68c6'
>>> exit()
```

0x68c6
## Notas adicionales

La dificultad principal de `asm3` radica en el **Little Endian**. En la arquitectura x86, los valores de varios bytes se guardan en la memoria con el byte menos significativo primero. Por ejemplo, el valor `0xc2cb1015` se guarda en la pila como `15 10 cb c2`. Al usar instrucciones como `BYTE PTR` y `WORD PTR` combinadas con desplazamientos (offsets) extraños como `ebp+0x9` o `ebp+0x12`, el programa te obliga a extraer y operar con bytes específicos que se encuentran a la mitad de los parámetros originales.

También hace uso intensivo de las subdivisiones del registro `eax` (`ax` de 16 bits; `ah` y `al` de 8 bits).
## Referencias
