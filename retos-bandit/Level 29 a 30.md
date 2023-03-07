 ## Objetivo
 
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.


## Datos de acceso al nivel 
ssh bandit29@bandit.labs.overthewire.org -p 2220
tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S

git

## Solución

``` 
bandit29@bandit:~$ mkdir /tmp/bandit29
mkdir: cannot create directory ‘/tmp/bandit29’: File exists
bandit29@bandit:~$ mkdir /tmp/banditt
bandit29@bandit:~$ cd banditt
-bash: cd: banditt: No such file or directory
bandit29@bandit:~$ cd banditt
-bash: cd: banditt: No such file or directory
bandit29@bandit:~$ cd /tmp/banditt
bandit29@bandit:/tmp/banditt$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit29/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit29/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit29-git@localhost's password:
Permission denied, please try again.
bandit29-git@localhost's password:
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (11/11), done.
Receiving objects: 100% (16/16), 1.44 KiB | 1.44 MiB/s, done.
remote: Total 16 (delta 2), reused 0 (delta 0), pack-reused 0
Resolving deltas: 100% (2/2), done.
bandit29@bandit:/tmp/banditt$ ls
repo
bandit29@bandit:/tmp/banditt$ ls -la
total 124
drwxrwxr-x    3 bandit29 bandit29   4096 Mar  2 19:22 .
drwxrwx-wt 1559 root     root     114688 Mar  2 19:23 ..
drwxrwxr-x    3 bandit29 bandit29   4096 Mar  2 19:23 repo
bandit29@bandit:/tmp/banditt$ cd repo
bandit29@bandit:/tmp/banditt/repo$ ls
README.md
bandit29@bandit:/tmp/banditt/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/banditt/repo$ git log
commit 0afe3501277395fbfa017480925edee3df6e8bb5 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    fix username

commit c2606dfc0aef7179bf1ccd6cffa9ed19151facb4
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/banditt/repo$ git diff 0afe3501277395fbfa017480925edee3df6e8bb5
bandit29@bandit:/tmp/banditt/repo$ git diff 0afe3501277395fbfa017480925edee3df6e8bb5 c2606dfc0aef7179bf1ccd6cffa9ed19151facb4
diff --git a/README.md b/README.md
index 1af21d3..2da2f39 100644
--- a/README.md
+++ b/README.md
@@ -3,6 +3,6 @@ Some notes for bandit30 of bandit.

 ## credentials

-- username: bandit30
+- username: bandit29
 - password: <no passwords in production!>

bandit29@bandit:/tmp/banditt/repo$ git branch
* master
bandit29@bandit:/tmp/banditt/repo$ git show-branch
[master] fix username
bandit29@bandit:/tmp/banditt/repo$ git show-branch -a
* [master] fix username
 ! [origin/HEAD] fix username
  ! [origin/dev] add data needed for development
   ! [origin/master] fix username
    ! [origin/sploits-dev] add some silly exploit, just for shit and giggles
-----
    + [origin/sploits-dev] add some silly exploit, just for shit and giggles
  +   [origin/dev] add data needed for development
  +   [origin/dev^] add gif2ascii
*++++ [master] fix username
bandit29@bandit:/tmp/banditt/repo$ git remote origin
error: Unknown subcommand: origin
usage: git remote [-v | --verbose]
   or: git remote add [-t <branch>] [-m <master>] [-f] [--tags | --no-tags] [--mirror=<fetch|push>] <name> <url>
   or: git remote rename <old> <new>
   or: git remote remove <name>
   or: git remote set-head <name> (-a | --auto | -d | --delete | <branch>)
   or: git remote [-v | --verbose] show [-n] <name>
   or: git remote prune [-n | --dry-run] <name>
   or: git remote [-v | --verbose] update [-p | --prune] [(<group> | <remote>)...]
   or: git remote set-branches [--add] <name> <branch>...
   or: git remote get-url [--push] [--all] <name>
   or: git remote set-url [--push] <name> <newurl> [<oldurl>]
   or: git remote set-url --add <name> <newurl>
   or: git remote set-url --delete <name> <url>

    -v, --verbose         be verbose; must be placed before a subcommand

bandit29@bandit:/tmp/banditt/repo$ git remote show origin
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit29/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit29/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit29-git@localhost's password:
* remote origin
  Fetch URL: ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
  Push  URL: ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
  HEAD branch: master
  Remote branches:
    dev         tracked
    master      tracked
    sploits-dev tracked
  Local branch configured for 'git pull':
    master merges with remote master
  Local ref configured for 'git push':
    master pushes to master (up to date)
bandit29@bandit:/tmp/banditt/repo$ git checkout dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/banditt/repo$ ls
code  README.md
bandit29@bandit:/tmp/banditt/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS

bandit29@bandit:/tmp/banditt/repo$
```
Son los mismos pasos del bandit anterior solo que  se uso el comando
git diff 0afe3501277395fbfa017480925edee3df6e8bb5 c2606dfc0aef7179bf1ccd6cffa9ed19151facb4
de alli usamos cat README.md
de alli usamos  git branch
luego git show branch -a
luego git remote origin
y luego hacer git remote show origin
nos pedira la contrasena ya dada anteriormente
para despues acceder a git checkout dev
al final  ponemos un ls, para encontrarnos con un README.md
donde estara la contrasena



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
