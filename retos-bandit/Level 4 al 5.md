## Objetivo
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

## Datos de acceso al nivel 
 ssh bandit4@bandit.labs.overthewire.org -p 2220
 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
 ls, cd, cat , file , du, find
 

## Solución

```
bandit4@bandit:~$ file inhere/*
inhere/-file00: data
inhere/-file01: data
inhere/-file02: data
inhere/-file03: data
inhere/-file04: data
inhere/-file05: data
inhere/-file06: data
inhere/-file07: ASCII text
inhere/-file08: data
inhere/-file09: data
bandit4@bandit:~$ cat inhere/-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~$

```
con el comando file inhere/* buscamos los atchivos y se listan que hay en la carpeta 
despues observamos que el file 07 es de diferente extencion
procedemos a abrirlo con cat inhere/-file07 y nos muestra la contrasena
y con el comando find .  -name .hidden buscamos ese archivo olculto
para proceder y hacer un cat ./inhere/ .hidden para obtener la cotrasena como el ejercicio anterior


## Notas adicionales
- ls listar archivo
- emite contenido de lineas de comando
- ls -lh  Lista el contenido en un tamaño (human readable) más entendible por el usuario. Por defecto el tamaño se muestra en bytes, pero al usar -h nos lo muestra en una unidad más legible para las personas.
- pwd saca la ruta actual

## Referencias

