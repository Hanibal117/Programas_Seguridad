## Objetivo
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Datos de acceso al nivel 
 bandit.labs.overthewire.org
 bandit0
 ls, cd, cat , file , du, find
 

## Solución
Realice los pasos del bandit 1
```
bandit0@bandit:~$ ls -l
total 4
-rw-r----- 1 bandit1 bandit0 33 Jan 11 19:18 readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```


## Notas adicionales
- ls listar archivo
- ls -la  listar archivos en forma extendida (ocultos)
- cat imprime datos a la pantalla

## Referencias

