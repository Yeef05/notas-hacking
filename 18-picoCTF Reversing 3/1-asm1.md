# asm1

## Descripción

What does asm1(0x36e) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/742701d2dc84a01fe69c48228c14feafdcd3658f83e99b887c550bed0302419e/test.S)
## Solución

```
1.-Descargamos el archivo y lo mostramos

┌──(flavio㉿kali)-[~/picoCTF/Reversing/act3/asm1]
└─$ cat test.S     
asm1:
        <+0>:   endbr32 
        <+4>:   push   ebp
        <+5>:   mov    ebp,esp
        
        <+7>:   cmp    DWORD PTR [ebp+0x8],0x6c8
        <+14>:  jg     0x11d6 <asm1+41>
        <+16>:  cmp    DWORD PTR [ebp+0x8],0x36e
        <+23>:  jne    0x11ce <asm1+33>
        <+25>:  mov    eax,DWORD PTR [ebp+0x8]
        <+28>:  add    eax,0x6
        <+31>:  jmp    0x11ed <asm1+64>
        <+33>:  mov    eax,DWORD PTR [ebp+0x8]
        <+36>:  sub    eax,0x6
        <+39>:  jmp    0x11ed <asm1+64>
        <+41>:  cmp    DWORD PTR [ebp+0x8],0xbef
        <+48>:  jne    0x11e7 <asm1+58>
        <+50>:  mov    eax,DWORD PTR [ebp+0x8]
        <+53>:  sub    eax,0x6
        <+56>:  jmp    0x11ed <asm1+64>
        <+58>:  mov    eax,DWORD PTR [ebp+0x8]
        <+61>:  add    eax,0x6
        <+64>:  pop    ebp
        <+65>:  ret
        
2.-Hacerle un nano y añadir esto al principio (en 0x36e va el parametro de picoCTF) que da en la descripción del problema "What does asm1(0x36e) return?"

stack

0000


[ ebp ] <-esp <- ebp
[ ret ] <- ebp + 0x4
[0x36e] <- ebp + 0x8
fffff

registres

3.-Dividimos la terminal y corremos python para realizar las comparaciones que nos da asm1

┌──(flavio㉿kali)-[~/picoCTF/Reversing/act3/asm1]
└─$ python3
Python 3.10.8 (main, Nov  4 2022, 09:21:25) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> # Primera comparación <+7> y <+14>: ¿0x36e es mayor (jg) que 0x6c8?
>>> 0x36e > 0x6c8
False
>>> # Como es False, no salta. Pasamos a la segunda comparación <+16> y <+23>.
>>> # ¿0x36e es diferente (jne) a 0x36e?
>>> 0x36e != 0x36e
False
>>> # Como es False, tampoco salta y entra directo a la instrucción <+25> y <+28>.
>>> eax = 0x36e
>>> eax += 0x6
>>> # El programa salta al final (jmp <asm1+64>) y retorna eax. Lo imprimimos en hex.
>>> hex(eax)
'0x374'
>>> exit()
```

0x374
## Notas adicionales

Son diferentes operaciones para cada caso, dependiendo que pida hacer el archivo test
## Referencias
