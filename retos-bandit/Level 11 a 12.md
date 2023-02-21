 ## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Datos de acceso al nivel 
ssh bandit11@bandit.labs.overthewire.org -p 2220
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
 

## Solución

``` 
bandit11@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Jan 11 19:18 .
drwxr-xr-x 70 root     root     4096 Jan 11 19:19 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit12 bandit11   49 Jan 11 19:18 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$


```
se busco el archivo data.txt para mostrarlo con cat data.txt
despues con tr buscamos y descomprimimos


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

## Referencias
https://en.wikipedia.org/wiki/Rot13
