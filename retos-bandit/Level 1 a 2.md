## Objetivo
The password for the next level is stored in a file called **-** located in the home directory
## Datos de acceso al nivel 
 ssh bandit1@bandit.labs.overthewire.org -p 2220
 NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
 ls, cd, cat , file , du, find
 

## Solución

```
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```
Tambien se podria con cat . /-

## Notas adicionales
- ls listar archivo
- ls -la  listar archivos en forma extendida (ocultos)
- pwd saca la ruta

## Referencias

