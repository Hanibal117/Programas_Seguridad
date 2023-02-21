 ## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.


## Datos de acceso al nivel 
ssh bandit14@bandit.labs.overthewire.org -p 2220
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

ssh, telnet, nc, openssl, s_client, nmap
 

## Solución

``` 
bandit14@bandit:~$
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

```
A continuación, debemos enviar la contraseña al puerto 30000 en localhost. Usé nc para conectarme al puerto localhost 3000 y escribir la contraseña.

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
- No dejar la llave sin cuidar
- 

## Referencias
https://www.youtube.com/watch?v=7_LPdttKXPc
http://computer.howstuffworks.com/web-server5.htm
https://en.wikipedia.org/wiki/IP_address
https://en.wikipedia.org/wiki/Localhost
http://computer.howstuffworks.com/web-server8.htm
https://en.wikipedia.org/wiki/Port_(computer_networking)
