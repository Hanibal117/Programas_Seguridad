#### Description

an you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.


## Pistas
Does that encoding look familiar
The `str_xor` function does not need to be reverse engineered for this challenge.



## Solución

``` 

al ingresar a nano level2.py notamos que hay una codifocacion
asi que la ponemos en un print de python para que nos traduzca
print(chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36))
el resultado es : de76
ese lo ingresamos en python3 level3.py
y nos dara la bandera


hannlec117-picoctf@webshell:~$ nano level.py
hannlec117-picoctf@webshell:~$ pyton3 level2.py
-bash: pyton3: command not found
hannlec117-picoctf@webshell:~$ nano level.pypython3 level2.py
hannlec117-picoctf@webshell:~$ python3 level2.py
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
hannlec117-picoctf@webshell:~$ 



```

## Bandera
Flag: picoCTF{tr45h_51ng1ng_489dea9a}



## Notas adicionales


## Referencias
