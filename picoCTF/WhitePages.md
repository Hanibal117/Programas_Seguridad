#### Description

I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt) is all blank!

## Pistas

-   How did pictures from the moon landing get sent back to Earth?
-   What is the CMU mascot?, that might help select a RX option


## Solución

descargamos el archivo para instalar el sstv e ingresa el comando 

```
hacemos un exploit con lo siguiente

  GNU nano 6.4                                                                                 e.py                                                                                          
from pwn import *

file   = open('whitepages.txt', 'rb')
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83', b'0')
data = data.replace(b'\x20', b'1')
data = data.decode('ascii')
data = unbits(data)
print(data)




b'\n\t\tpicoCTF\n\n\t\tSEE PUBLIC RECORDS & BACKGROUND REPORT\n\t\t5000 Forbes Ave, Pittsburgh, PA 15213\n\t\tpicoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}\n\t\t'
              
```

## Bandera
Flag:  picoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}


## Notas adicionales


## Referencias
