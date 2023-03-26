#### Description

This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/2d24d50b4ebed90c704575627f1f57b2/flag).

## Pistas

Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.

To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/2d24d50b4ebed90c704575627f1f57b2/flag`

$ man cat

## Solución

``` 
hannlec117-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/2d24d50b4ebed90c704575627f1f57b2/flag
--2023-03-25 22:19:19--  https://mercury.picoctf.net/static/2d24d50b4ebed90c704575627f1f57b2/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                                                      100%[==================================================================================================================================>]      34  --.-KB/s    in 0s      

2023-03-25 22:19:19 (27.4 MB/s) - 'flag' saved [34/34]

hannlec117-picoctf@webshell:~$ ls
0x3D  README.txt  file  flag  output.txt  python  strings
hannlec117-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_f28ac910}
hannlec117-picoctf@webshell:~$ 

```

## Bandera
Flag: picoCTF{s4n1ty_v3r1f13d_f28ac910}


## Notas adicionales
Los  Pipes **te permiten procesar secuencialmente una serie de comandos referentes a un conjunto de datos, o mover eficazmente los datos de un lado a otro entre comandos**



## Referencias
