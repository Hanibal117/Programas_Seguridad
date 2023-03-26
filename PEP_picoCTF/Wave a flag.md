
## Pistas

#### Description

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm) has extraordinarily helpful information...

## Solución

``` 
hannlec117-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm
--2023-03-25 22:21:12--  https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                                                      100%[==================================================================================================================================>]  10.68K  --.-KB/s    in 0s      

2023-03-25 22:21:13 (295 MB/s) - 'warm' saved [10936/10936]

hannlec117-picoctf@webshell:~$ ls
0x3D  README.txt  file  flag  output.txt  python  strings  warm
hannlec117-picoctf@webshell:~$ ./warm
-bash: ./warm: Permission denied
hannlec117-picoctf@webshell:~$ ./warm -h
-bash: ./warm: Permission denied
hannlec117-picoctf@webshell:~$ chmod +x warm
hannlec117-picoctf@webshell:~$ 
hannlec117-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_d6969390}
hannlec117-picoctf@webshell:~$ 
hannlec117-picoctf@webshell:~$ 
```
usamos el chmod +x warm para dar permiso
despues con ./warm  -h nos da la  bandera

## Bandera
Flag: picoCTF{b1scu1ts_4nd_gr4vy_d6969390}


## Notas adicionales
Los  Pipes **te permiten procesar secuencialmente una serie de comandos referentes a un conjunto de datos, o mover eficazmente los datos de un lado a otro entre comandos**



## Referencias
