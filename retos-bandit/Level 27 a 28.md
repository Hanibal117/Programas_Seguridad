 ## Objetivo
 
There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel 
ssh bandit27@bandit.labs.overthewire.org -p 2220
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS

git

## Solución

``` 
bandit27@bandit:/tmp/tmp.bMYODQDT3s$ cd ..
bandit27@bandit:/tmp$ cd ..
bandit27@bandit:/$ mktemp -d
/tmp/tmp.j1DmtZhUjc
bandit27@bandit:/$ cd /tmp/tmp.j1DmtZhUjc
bandit27@bandit:/tmp/tmp.j1DmtZhUjc$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...
kex_exchange_identification: read: Connection reset by peer
Connection reset by 127.0.0.1 port 2220
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
bandit27@bandit:/tmp/tmp.j1DmtZhUjc$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit27/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit27/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit27-git@localhost's password:
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
bandit27@bandit:/tmp/tmp.j1DmtZhUjc$ ls -la
total 112
drwx------    3 bandit27 bandit27   4096 Feb 28 15:14 .
drwxrwx-wt 2819 root     root     106496 Feb 28 15:14 ..
drwxrwxr-x    3 bandit27 bandit27   4096 Feb 28 15:14 repo
bandit27@bandit:/tmp/tmp.j1DmtZhUjc$ ls
repo
bandit27@bandit:/tmp/tmp.j1DmtZhUjc$ cd repo
bandit27@bandit:/tmp/tmp.j1DmtZhUjc/repo$ ls -la
total 16
drwxrwxr-x 3 bandit27 bandit27 4096 Feb 28 15:14 .
drwx------ 3 bandit27 bandit27 4096 Feb 28 15:14 ..
drwxrwxr-x 8 bandit27 bandit27 4096 Feb 28 15:14 .git
-rw-rw-r-- 1 bandit27 bandit27   68 Feb 28 15:14 README
bandit27@bandit:/tmp/tmp.j1DmtZhUjc/repo$ cat README
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR
bandit27@bandit:/tmp/tmp.j1DmtZhUjc/repo$
```
Desde el editor del cmd reducimos la pantalla para el bandit


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
