 ## Descripcion
 
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?

## Pistas
https://linux.die.net/man/1/strings

## Solución

``` 
hannlec117-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
--2023-03-02 15:30:48--  https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings'

strings                                                   100%[==================================================================================================================================>] 757.84K  1.81MB/s    in 0.4s    

2023-03-02 15:30:49 (1.81 MB/s) - 'strings' saved [776032/776032]

hannlec117-picoctf@webshell:~$ strings strings | grep picoCTF
picoCTF{5tRIng5_1T_d66c7bb7}
hannlec117-picoctf@webshell:~$ 

```
Con wget y poniendo el link del archivo a descargar lo cargo al shell
## Bandera
Flag: picoCTF{5tRIng5_1T_d66c7bb7}


## Notas adicionales


## Referencias
