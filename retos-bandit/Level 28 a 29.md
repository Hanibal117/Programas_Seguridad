 ## Objetivo
 
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel 
ssh bandit28@bandit.labs.overthewire.org -p 2220
AVanL161y9rsbcJIsFHuw35rjaOM19nR


git

## Solución

``` 
bandit28@bandit:~$ cd /tmp
bandit28@bandit:/tmp$ mkdir cell
bandit28@bandit:/tmp$ cd cell
bandit28@bandit:/tmp/cell$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit28/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit28/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit28-git@localhost's password:
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (9/9), done.
Resolving deltas: 100% (2/2), done.
bandit28@bandit:/tmp/cell$ ls
repo
bandit28@bandit:/tmp/cell$ cd repo/
bandit28@bandit:/tmp/cell/repo$ ls
README.md
bandit28@bandit:/tmp/cell/repo$ ls -la
total 16
drwxrwxr-x 3 bandit28 bandit28 4096 Mar  2 19:01 .
drwxrwxr-x 3 bandit28 bandit28 4096 Mar  2 19:01 ..
drwxrwxr-x 8 bandit28 bandit28 4096 Mar  2 19:01 .git
-rw-rw-r-- 1 bandit28 bandit28  111 Mar  2 19:01 README.md
bandit28@bandit:/tmp/cell/repo$ cat readme.md
cat: readme.md: No such file or directory
bandit28@bandit:/tmp/cell/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/cell/repo$ cd .git/
bandit28@bandit:/tmp/cell/repo/.git$ ls -la
total 52
drwxrwxr-x 8 bandit28 bandit28 4096 Mar  2 19:01 .
drwxrwxr-x 3 bandit28 bandit28 4096 Mar  2 19:01 ..
drwxrwxr-x 2 bandit28 bandit28 4096 Mar  2 19:01 branches
-rw-rw-r-- 1 bandit28 bandit28  281 Mar  2 19:01 config
-rw-rw-r-- 1 bandit28 bandit28   73 Mar  2 19:01 description
-rw-rw-r-- 1 bandit28 bandit28   23 Mar  2 19:01 HEAD
drwxrwxr-x 2 bandit28 bandit28 4096 Mar  2 19:01 hooks
-rw-rw-r-- 1 bandit28 bandit28  137 Mar  2 19:01 index
drwxrwxr-x 2 bandit28 bandit28 4096 Mar  2 19:01 info
drwxrwxr-x 3 bandit28 bandit28 4096 Mar  2 19:01 logs
drwxrwxr-x 4 bandit28 bandit28 4096 Mar  2 19:01 objects
-rw-rw-r-- 1 bandit28 bandit28  114 Mar  2 19:01 packed-refs
drwxrwxr-x 5 bandit28 bandit28 4096 Mar  2 19:01 refs
bandit28@bandit:/tmp/cell/repo/.git$ git log
commit 104db85a904e9691ff22aafe1a96124c88f75afa (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    fix info leak

commit 6c3c5e485cc531e5d52c321587ce1103833ab7c3
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    add missing data

commit cd3b97ef95879ec34df0d6c82f2a96d552f0e56c
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    initial commit of README.md
bandit28@bandit:/tmp/cell/repo/.git$ git show 104db85a904e9691ff22aafe1a96124c88f75afa
commit 104db85a904e9691ff22aafe1a96124c88f75afa (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    fix info leak

diff --git a/README.md b/README.md
index b302105..5c6457b 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials

 - username: bandit29
-- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
+- password: xxxxxxxxxx

bandit28@bandit:/tmp/cell/repo/.git$
```
Creamos una carpeta temporal cell donde clonaremos el git `ssh://bandit28-git@localhost:2220/home/bandit28-git/repo`
despues accedemos al repositorio que esta en la carpeta
despues con .git/ accedemos
despues con git log checamos los logeos
luego copiamos el commit 104db85a904e9691ff22aafe1a96124c88f75afa
para luego poner git show 104db85a904e9691ff22aafe1a96124c88f75afa
donde nos arrojara la contrasena: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S



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
- 


## Referencias
