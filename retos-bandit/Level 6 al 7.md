## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size
 
## Datos de acceso al nivel 
 ssh bandit6@bandit.labs.overthewire.org -p 2220
 P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
 
  ls, cd, cat , file , du, find, grep
 

## Solución

``` 
bandit6@bandit:~$ bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$
```

con find / -user bandit7 -group bandit6 -size 33c 2>/dev/null  mandamos lo que no sirve o no funciona, a la par de qeu nos meustra lo que si

## Notas adicionales
- ls listar archivo
- emite contenido de lineas de comando
- ls -lh  Lista el contenido en un tamaño (human readable) más entendible por el usuario. Por defecto el tamaño se muestra en bytes, pero al usar -h nos lo muestra en una unidad más legible para las personas.
- pwd saca la ruta actual

## Referencias

