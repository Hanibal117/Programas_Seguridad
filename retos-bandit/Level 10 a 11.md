 ## Objetivo

 The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Datos de acceso al nivel 
ssh bandit10@bandit.labs.overthewire.org -p 2220
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s 

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
 

## Solución

``` 
bandit10@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Jan 11 19:18 .
drwxr-xr-x 70 root     root     4096 Jan 11 19:19 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit11 bandit10   69 Jan 11 19:18 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ echo "hola mundo"
hola mundo
bandit10@bandit:~$ echo "hola mundo" | base64
aG9sYSBtdW5kbwo=
bandit10@bandit:~$ echo -n aG9sYSBtdW5kbwo= | base64 -d
hola mundo
bandit10@bandit:~$ base64  -d data.txt
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ cat data.txt  | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$

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

## Referencias
https://en.wikipedia.org/wiki/Base64
