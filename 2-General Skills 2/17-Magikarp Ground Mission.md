# Magikarp Ground Mission
## Descripción

Do you know how to move between directories and read files in the shell? Start the container, `ssh`to it, and then `ls` once connected to begin.

Additional details will be available after launching your challenge instance.

Login via `ssh` as `ctf-player` with the password, `8c606eb1` on the host `wily-courier.picoctf.net` and port `50682`.
## Solución

```
Yeef05-picoctf@webshell:~$ ssh -p 55072 ctf-player@wily-courier.picoctf.net

ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt

ctf-player@pico-chall$ cat 1of3.flag.txt
picoCTF{xxsh_

ctf-player@pico-chall$ cat instructions-to-2of3.txt
Next, go to the root of all things, more succinctly `/`

ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  challenge  home                      lib64  opt   run   sys  var
bin            dev        instructions-to-3of3.txt  media  proc  sbin  tmp
boot           etc        lib                       mnt    root  srv   usr

ctf-player@pico-chall$ cat 2of3.flag.txt
0ut_0f_//4t3r_

ctf-player@pico-chall$ cat instructions-to-3of3.txt
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd ~

ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in

ctf-player@pico-chall$ cat 3of3.flag.txt
0b24fc4f}
```

picoCTF{xxsh_0ut_0f_//4t3r_0b24fc4f}
## Notas adicionales

Una vez que entramos al puerto vamos a estar comprobando archivos
## Referencias