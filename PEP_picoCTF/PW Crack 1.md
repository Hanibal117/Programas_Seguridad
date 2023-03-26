#### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.


## Pistas

To view the file in the webshell, do: `$ nano level1.py`
To exit `nano`, press Ctrl and x and follow the on-screen prompts.
The `str_xor` function does not need to be reverse engineered for this challenge.


## Solución

``` 
Descargue los 2 archivos

hannlec117-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.py
--2023-03-26 01:23:29--  https://artifacts.picoctf.net/c/11/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.6, 108.156.172.120, 108.156.172.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.6|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py                                                 100%[==================================================================================================================================>]     876  --.-KB/s    in 0s      

2023-03-26 01:23:29 (4.39 MB/s) - 'level1.py' saved [876/876]

hannlec117-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
--2023-03-26 01:23:42--  https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.42, 108.156.172.6, 108.156.172.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc                                       100%[==================================================================================================================================>]      30  --.-KB/s    in 0s      

2023-03-26 01:23:42 (184 KB/s) - 'level1.flag.txt.enc' saved [30/30]

hannlec117-picoctf@webshell:~$ python3 level1.py 
Please enter correct password for flag: lele
That password is incorrect
hannlec117-picoctf@webshell:~$ nano level1.py
hannlec117-picoctf@webshell:~$ python3 level1.py 
Please enter correct password for flag: lela
That password is incorrect
hannlec117-picoctf@webshell:~$ nano level1.py
hannlec117-picoctf@webshell:~$ python3 level1.py 
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
hannlec117-picoctf@webshell:~$ 

accedi con nano al archivo level1.py y mire que la contrasena era 1e1a
despues la puse y me dio la bandera



```

## Bandera
Flag: picoCTF{545h_r1ng1ng_fa343060}



## Notas adicionales


## Referencias
