 ## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Datos de acceso al nivel 
ssh bandit12@bandit.labs.overthewire.org -p 2220
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file
 

## Solución

``` 
bandit12@bandit:~$ xxd -r data.txt | file -
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Wed Jan 11 19:18:38 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat |file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat |file -
/dev/stdin: gzip compressed data, was "data4.bin", last modified: Wed Jan 11 19:18:38 2023, max compression, from Unix
bandit12@bandit:~$  xxd -r data.txt | zcat | bzcat | zcat |file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$
bandit12@bandit:~$  xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat |file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | file -
/dev/stdin: gzip compressed data, was "data9.bin", last modified: Wed Jan 11 19:18:38 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file -
/dev/stdin: ASCII text
bandit12@bandit:~$  xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
bandit12@bandit:~$
```
Se averigua el tipo del fichero extraído y operamos sobre él de manera correcta
Se averigua el tipo del fichero extraído y operamos sobre él de manera correcta:
Se averigua el tipo del fichero extraído y operamos sobre él de manera correcta
Se averigua el tipo del fichero extraído y operamos sobre él de manera correcta
Se averigua el tipo del fichero extraído y operamos sobre él de manera correcta
Se averigua el tipo del fichero extraído y operamos sobre él de manera correcta


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

## Referencias
https://en.wikipedia.org/wiki/Hex_dump