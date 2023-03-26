#### Description

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 14291`.

## Pistas

What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)

## Solución

``` 
hannlec117-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 14291 | grep "pico"
picoCTF{digital_plumb3r_ea8bfec7}
```

## Bandera
Flag: picoCTF{digital_plumb3r_ea8bfec7}


## Notas adicionales
Los  Pipes **te permiten procesar secuencialmente una serie de comandos referentes a un conjunto de datos, o mover eficazmente los datos de un lado a otro entre comandos**



## Referencias
