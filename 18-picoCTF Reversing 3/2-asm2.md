# asm2

## Descripción

What does asm2(0xa,0x15) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.picoctf.net/c_fickle_tempest/1b461fce4f77f2756ffeade3af119ec77d49db6fd9831387af61f9e3dec7a839/test.S)
## Solución

```
1.-Descargamos el archivo y lo mostramos

┌──(flavio㉿kali)-[~/picoCTF/Reversing/act3/asm2]
└─$ cat test.S 
asm2:
        <+0>:   endbr32 
        <+4>:   push   ebp
        <+5>:   mov    ebp,esp
        <+7>:   sub    esp,0x10
        <+10>:  mov    eax,DWORD PTR [ebp+0xc]
        <+13>:  mov    DWORD PTR [ebp-0x4],eax
        <+16>:  mov    eax,DWORD PTR [ebp+0x8]
        <+19>:  mov    DWORD PTR [ebp-0x8],eax
        <+22>:  jmp    0x11cd <asm2+32>
        <+24>:  add    DWORD PTR [ebp-0x4],0x1
        <+28>:  add    DWORD PTR [ebp-0x8],0x37
        <+32>:  cmp    DWORD PTR [ebp-0x8],0x84ab
        <+39>:  jle    0x11c5 <asm2+24>
        <+41>:  mov    eax,DWORD PTR [ebp-0x4]
        <+44>:  leave  
        <+45>:  ret  
        
2.-Hacerle un nano y añadir esto al principio (en 0xa y 0x15 van los parametros de picoCTF) que da en la descripción del problema "What does asm2(0xa,0x15) return?"

stack

0000

[ local1] <- ebp - 0x4  (Toma el valor de 0x15)
[ local2] <- ebp - 0x8  (Toma el valor de 0xa)
...
[ ebp   ] <- esp <- ebp
[ ret   ] <- ebp + 0x4
[ 0xa   ] <- ebp + 0x8  (Primer parámetro)
[ 0x15  ] <- ebp + 0xc  (Segundo parámetro)
fffff

registres

3.-Dividimos la terminal y corremos python para realizar el bucle y las comparaciones que nos da asm2

┌──(flavio㉿kali)-[~/picoCTF/Reversing/act3/asm2]
└─$ python3
Python 3.10.8 (main, Nov  4 2022, 09:21:25) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> # Asignamos los valores a las variables locales según las instrucciones <+10> a <+19>
>>> local1 = 0x15
>>> local2 = 0xa
>>> # La instrucción <+22> salta a la <+32> donde inicia un bucle. 
>>> # La instrucción <+39> (jle) nos dice que el bucle continúa mientras local2 <= 0x84ab
>>> while local2 <= 0x84ab:
...     local1 += 0x1   # Instrucción <+24>
...     local2 += 0x37  # Instrucción <+28>
... 
>>> # Al terminar el bucle, la instrucción <+41> mueve local1 a eax para retornarlo
>>> eax = local1
>>> hex(eax)
'0x27f'
>>> exit()
```

0x27f
## Notas adicionales

A diferencia de `asm1` que solo hacía validaciones y saltos condicionales (`if/else`), `asm2` reserva espacio en la pila para variables locales (`sub esp,0x10`) e implementa un bucle `while` que incrementa los valores repetidamente hasta que se rompe la condición.
## Referencias
