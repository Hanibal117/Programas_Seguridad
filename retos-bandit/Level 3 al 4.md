## Objetivo
The password for the next level is stored in a hidden file in the **inhere** directory.

## Datos de acceso al nivel 
 ssh bandit3@bandit.labs.overthewire.org -p 2220
 aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
 ls, cd, cat , file , du, find
 

## Solución

```
bandit3@bandit:~$ ls -la inhere/
total 12
drwxr-xr-x 2 root    root    4096 Jan 11 19:19 .
drwxr-xr-x 3 root    root    4096 Jan 11 19:19 ..
-rw-r----- 1 bandit4 bandit3   33 Jan 11 19:19 .hidden
bandit3@bandit:~$ find . -name .hidden
./inhere/.hidden
bandit3@bandit:~$ cat ./inhere/.hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~$
```
con el comando ls -la inhere/ estamos queriendo visualizar los archivos que hay en esa carpeta
y con el comando find .  -name .hidden buscamos ese archivo olculto
para proceder y hacer un cat ./inhere/ .hidden para obtener la cotrasena como el ejercicio anterior


## Notas adicionales
- ls listar archivo
- emite contenido de lineas de comando
- ls -la  listar archivos en forma extendida (ocultos)
- pwd saca la ruta

## Referencias

