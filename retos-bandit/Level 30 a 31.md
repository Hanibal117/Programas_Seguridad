 ## Objetivo
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level. 



## Datos de acceso al nivel 
ssh bandit30@bandit.labs.overthewire.org -p 2220
xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
git

## Solución

``` 
bandit30@bandit:~$ mktemp -d
/tmp/tmp.PYNeKpq7X0
bandit30@bandit:~$ cd /tmp/tmp.PYNeKpq7X0
bandit30@bandit:/tmp/tmp.PYNeKpq7X0$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit30/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit30/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit30-git@localhost's password:
Permission denied, please try again.
bandit30-git@localhost's password:
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), 299 bytes | 299.00 KiB/s, done.
bandit30@bandit:/tmp/tmp.PYNeKpq7X0$ ls
repo
bandit30@bandit:/tmp/tmp.PYNeKpq7X0$ cd repo
bandit30@bandit:/tmp/tmp.PYNeKpq7X0/repo$ ls -la
total 16
drwxrwxr-x 3 bandit30 bandit30 4096 Mar  7 01:50 .
drwx------ 3 bandit30 bandit30 4096 Mar  7 01:50 ..
drwxrwxr-x 8 bandit30 bandit30 4096 Mar  7 01:50 .git
-rw-rw-r-- 1 bandit30 bandit30   30 Mar  7 01:50 README.md
bandit30@bandit:/tmp/tmp.PYNeKpq7X0/repo$ git tag
secret
bandit30@bandit:/tmp/tmp.PYNeKpq7X0/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
bandit30@bandit:/tmp/tmp.PYNeKpq7X0/repo$
```

accedemos a la repo y  no aparecera un archivo secret al tecleatr el comando git tag
ponemos git show secret y listo nos da la password




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
