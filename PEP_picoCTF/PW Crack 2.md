#### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## Pistas
To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`
To exit `bvi` type `:q` and press enter.
The `str_xor` function does not need to be reverse engineered for this challenge.



## Solución

``` 
Descargue los archivos, analice el archivo con nano level3.py
para encontrarme con que hay 7 posibilidades de la password
pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]
siendo 87ab

hannlec117-picoctf@webshell:~$ nano level3.py
hannlec117-picoctf@webshell:~$ bvi level3.hash.bin

[2]+  Stopped                 bvi level3.hash.bin
hannlec117-picoctf@webshell:~$ python3 level3.py
Please enter correct password for flag: f09e
That password is incorrect
hannlec117-picoctf@webshell:~$ python3 level3.py
Please enter correct password for flag: 4dcf
That password is incorrect
hannlec117-picoctf@webshell:~$ python3 level3.py
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
hannlec117-picoctf@webshell:~$ 




```

## Bandera
Flag: picoCTF{m45h_fl1ng1ng_cd6ed2eb}



## Notas adicionales


## Referencias
