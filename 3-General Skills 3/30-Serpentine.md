# Serpentine
## Descripción

Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/36/serpentine.py)
## Solución

```
Yeef05-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/36/serpentine.py

Yeef05-picoctf@webshell:~$ nano serpentine.py
Yeef05-picoctf@webshell:~$ python3 serpentine.py

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_aa2340b2}
```

picoCTF{7h3_r04d_l355_7r4v3l3d_aa2340b2}
## Notas adicionales

Solamente hace falta llamar la función donde esta la flag, ya que por defecto no la llama en ninguna opción.
## Referencias

