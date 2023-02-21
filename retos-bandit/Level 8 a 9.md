## Objetivo

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

## Datos de acceso al nivel 
ssh bandit8@bandit.labs.overthewire.org -p 2220
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
 
  ls, cd, cat , file , du, find, grep
 

## Solución

``` 
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$

```
con el comando cat data.txt | sort | uniq -u se muestra  el resultado a raiz de sort y uniq
 

## Notas adicionales
- ls listar archivo
- emite contenido de lineas de comando
- ls -lh  Lista el contenido en un tamaño (human readable) más entendible por el usuario. Por defecto el tamaño se muestra en bytes, pero al usar -h nos lo muestra en una unidad más legible para las personas.
- pwd saca la ruta actual
- | wc -l cuenta cunatos archivos hay
- grep  "millionth" data.txt ayuda a buscar y encontrar la coincidencia con lo que buscamos
- sort ordena de manera alfabetica todas las lineas
- uniq -u aparece la unica linea
- 

## Referencias
https://ryanstutorials.net/linuxtutorial/piping.php

