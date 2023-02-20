## Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

-   human-readable
-   1033 bytes in size
-   not executable
## Datos de acceso al nivel 
 ssh bandit5@bandit.labs.overthewire.org -p 2220
 lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
 ls, cd, cat , file , du, find
 

## Solución

```

bandit5@bandit:~$ find . -type f -readable ! -executable -size 1033c
./inhere/maybehere07/.file2
bandit5@bandit:~$ cat ./inhere/maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU 
```
con este comando procedemos a cumplir los requiusitos de busqueda: find . -type f -readable ! -executable -size 1033c
para proceder y hacer un cat ./inhere/maybehere07/.file2 para obtener la cotrasena como el ejercicio anterior


## Notas adicionales
- ls listar archivo
- emite contenido de lineas de comando
- ls -la  listar archivos en forma extendida (ocultos)
- pwd saca la ruta actual

## Referencias

