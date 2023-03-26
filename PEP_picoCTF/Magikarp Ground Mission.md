#### Description

Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `481e7b14`

Additional details will be available after launching your challenge instance.


## Pistas

This challenge launches an instance on demand.  
Its current status is: `NOT_RUNNING`

## Solución

``` 
accediendo a los directorios y haciendo cats encontre la contrasena
ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt
picoCTF{xxsh_
ctf-player@pico-chall$ cat instructions-to-2of3.txt
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cd ..
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ ls -a
.  ..  .cache  .profile  .ssh  3of3.flag.txt  drop-in
ctf-player@pico-chall$ cd 3of3.flag.txt 
-bash: cd: 3of3.flag.txt: Not a directory
ctf-player@pico-chall$ cat 3of3.flag.txt
1118a9a4}
ctf-player@pico-chall$ cd ..
ctf-player@pico-chall$ ls -a
.  ..  ctf-player
ctf-player@pico-chall$ cat ctf-player
cat: ctf-player: Is a directory
ctf-player@pico-chall$ ls
ctf-player
ctf-player@pico-chall$ cd ..
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat 2of3.flag.txt
0ut_0f_\/\/4t3r_
ctf-player@pico-chall$ Connection to venus.picoctf.net closed by remote host.
Connection to venus.picoctf.net closed.
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/hacking]

```

## Bandera
flag: picoCTF{xxsh_0ut_0f_\/\/4t3r_1118a9a4}
0ut_0f_\/\/4t3r_



## Notas adicionales


## Referencias
