 ## Objetivo
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level. 



## Datos de acceso al nivel 
ssh bandit31@bandit.labs.overthewire.org -p 2220
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
git

## Solución

``` bandit31@bandit:~$ bandit31@bandit:~$ mktemp -d
/tmp/tmp.YHi0TKK3lq
bandit31@bandit:~$ cd /tmp/tmp.YHi0TKK3lq
bandit31@bandit:/tmp/tmp.YHi0TKK3lq$  git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
Permission denied, please try again.
bandit31-git@localhost's password:
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), 382 bytes | 382.00 KiB/s, done.
bandit31@bandit:/tmp/tmp.YHi0TKK3lq$ cd repo/
bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$ ls -la
total 20
drwxrwxr-x 3 bandit31 bandit31 4096 Mar  7 02:32 .
drwx------ 3 bandit31 bandit31 4096 Mar  7 02:32 ..
drwxrwxr-x 8 bandit31 bandit31 4096 Mar  7 02:32 .git
-rw-rw-r-- 1 bandit31 bandit31    6 Mar  7 02:32 .gitignore
-rw-rw-r-- 1 bandit31 bandit31  147 Mar  7 02:32 README.md
bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$ cat README.md
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master

bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$ echo 'May I come in?' > key.txt
bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$ ls -la
total 24
drwxrwxr-x 3 bandit31 bandit31 4096 Mar  7 02:36 .
drwx------ 3 bandit31 bandit31 4096 Mar  7 02:32 ..
drwxrwxr-x 8 bandit31 bandit31 4096 Mar  7 02:32 .git
-rw-rw-r-- 1 bandit31 bandit31    6 Mar  7 02:32 .gitignore
-rw-rw-r-- 1 bandit31 bandit31   15 Mar  7 02:36 key.txt
-rw-rw-r-- 1 bandit31 bandit31  147 Mar  7 02:32 README.md
bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$ cat key.txt
May I come in?
bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$ cat .gitignore
*.txt
bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$ git add -f key.txt
bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$ git commit -a
Unable to create directory /home/bandit31/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

Aborting commit due to empty commit message.
Aborting commit due to empty commit message.
bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$ git commit -a
Unable to create directory /home/bandit31/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

Aborting commit due to empty commit message.
bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$ git commit -a
Unable to create directory /home/bandit31/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

[master 0d7a8c2] Added the file
 1 file changed, 1 insertion(+)
 create mode 100644 key.txt
bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$ git push
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 324 bytes | 324.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'
bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$ git push -u origin master
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
Permission denied, please try again.
bandit31-git@localhost's password:
Permission denied, please try again.
bandit31-git@localhost's password:
bandit31-git@localhost: Permission denied (publickey,password).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$ git push -u origin master
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 324 bytes | 324.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'
bandit31@bandit:/tmp/tmp.YHi0TKK3lq/repo$
```

## Notas adicionales
- ls listar archivo
- emite contenido de lineas de comando
- ls -lh  Lista el contenido en un tamaño (human readable) más entendible por el usuario. Por defecto el tamaño se muestra en bytes, pero al usar -h nos lo muestra en una unidad más legible para las personas.
- pwd saca la ruta actual
- | wc -l cuenta cunatos archivos hay
- grep  "millionth" data.txt ayuda a buscar y encontrar la coincidencia con lo que buscamos
- sort ordena de manera alfabetica todas las lineas
- uniq -u aparece la unica linea
- strings lista caracteres "data.txt"
- echo imprime un texto a la pantalla
- base64 convierte datos decodificando
- tr permite al Usuario definir explícitamente como estará compuesto el conjunto o bien provee de una colección de caracteres y conjuntos predefinidos, que puede ser utilizados a la hora de definirlos
- xdd Crea un volcado hexadecimal de un archivo 
- No dejar la llave sin cuidar
- diff compara directorios
- cron demonio de linux que ejecuta comandos cada cierto momento del dia
- mkdir  crear directorios o carpetas en Linux
- grep  permite filtrar y eliminar la información inútil que se produce tras ejecutar un comando. Para usar grep como filtro
- mktemp -d  crea archivos temporalmente
- git branch modifica cambiando nombres de ramas
- 


## Referencias
