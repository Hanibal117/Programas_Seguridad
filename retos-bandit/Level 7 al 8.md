## Objetivo
 The password for the next level is stored in the file **data.txt** next to the word **millionth**
## Datos de acceso al nivel 
 ssh bandit7@bandit.labs.overthewire.org -p 2220
 z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
 
  ls, cd, cat , file , du, find, grep
 

## Solución

``` 
 bandit7@bandit:~$ bandit7@bandit:~$ cat data.txt |wc -l
98567
bandit7@bandit:~$ grep "millionth" data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$

```

 con ayuda del comendo grep buscamos la coincidencia para el archivo data.txt para poder encontrar la contrasena

## Notas adicionales
- ls listar archivo
- emite contenido de lineas de comando
- ls -lh  Lista el contenido en un tamaño (human readable) más entendible por el usuario. Por defecto el tamaño se muestra en bytes, pero al usar -h nos lo muestra en una unidad más legible para las personas.
- pwd saca la ruta actual
- | wc -l cuenta cunatos archivos hay
- grep  "millionth" data.txt ayuda a buscar y encontrar la coincidencia con lo que buscamos
- 

## Referencias

