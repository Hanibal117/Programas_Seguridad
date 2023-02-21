## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory.

## Datos de acceso al nivel 
 ssh bandit2@bandit.labs.overthewire.org -p 2220
 rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
 ls, cd, cat , file , du, find
 

## Solución

```
bandit2@bandit:~$ bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$
```
con el comando cat seguido de espacion diagonal invertida me aparece el resultado

## Notas adicionales
- ls listar archivo
- emite contenido de lineas de comando
- ls -la  listar archivos en forma extendida (ocultos)
- pwd saca la ruta

## Referencias
https://www.google.com/search?q=spaces+in+filename

