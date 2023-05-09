
 
#### Description

We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev_this). Can you reverse the flag.


## Pistas
objdump and Gihdra are some tools that could assist with this


## Solución

``` 
descargamos los archivos y cramos el siguiente script:

import os
import mmap

def memory_map(filename, access=mmap.ACCESS_READ):
    size = os.path.getsize(filename)
    fd = os.open(filename, os.O_RDONLY)
    return mmap.mmap(fd, size, access=access)

with memory_map("rev_this") as bin_file:
    for i in range(8):
        print(chr(bin_file[i]), end = '')
    for i in range(8, 23):
        if (i & 1) == 0:
            print(chr(bin_file[i] - 5), end = '')
        else:
            print(chr(bin_file[i] + 2), end = '')
    print (chr(bin_file[23]))
    Ejecutamos y listo
    
┌──(kali㉿kali)-[~/…/333/aaa/w/aaawww]
└─$ nano solve.py               
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/333/aaa/w/aaawww]
└─$ python3 solve.py                 
picoCTF{r3v3rs36ad73964}


```

## Bandera
Flag: picoCTF{r3v3rs36ad73964}


## Notas adicionales


## Referencias
