# Super SSH
## Descripción

Using a Secure Shell (SSH) is going to be pretty important.

Additional details will be available after launching your challenge instance.

Can you `ssh` as `ctf-player` to `titan.picoctf.net` at port `55122` to get the flag?You'll also need the password `1ad5be0d`. If asked, accept the fingerprint with `yes`.If your device doesn't have a shell, you can use: [https://webshell.picoctf.org](https://webshell.picoctf.org/)

If you're not sure what a shell is, check out our Primer: [https://primer.picoctf.com/#_the_shell](https://primer.picoctf.com/#_the_shell)

## Solución

```
Yeef05-picoctf@webshell:~$ ssh -p 55122 ctf-player@titan.picoctf.net
The authenticity of host '[titan.picoctf.net]:55122 ([3.139.174.234]:55122)' can't be established.

ED25519 key fingerprint is SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

Warning: Permanently added '[titan.picoctf.net]:55122' (ED25519) to the list of known hosts.

ctf-player@titan.picoctf.net's password:
 
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_8306c99d}
Connection to titan.picoctf.net closed.
```

picoCTF{s3cur3_c0nn3ct10n_8306c99d}
## Notas adicionales

Nos conectamos a un puerto como ssh, ya lo hicimos varias veces en retos pasados.
## Referencias

https://linux.die.net/man/1/ssh

