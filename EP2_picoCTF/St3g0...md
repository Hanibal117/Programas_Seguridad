
 
#### Description

Download this image and find the flag.

-   [Download image](https://artifacts.picoctf.net/c/217/pico.flag.png)

## Pistas
We know the end sequence of the message will be `$t3g0`.


## Solución

``` 
Descargamos el archivo, que es una iamgen, procedemos a instalar la herramienta zteg y luego tecleamos lo siguiente.
┌──(kali㉿kali)-[~/hacking/333/aaa]
└─$ zsteg -a -v pico.flag.png
b1,r,lsb,xy         .. text: "~__B>VG?G@"
    00000000: 5e 35 3f 06 7e 5f 5f 42  3e 56 47 3f 47 40 00 00  |^5?.~__B>VG?G@..|
    00000010: 00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
    *
    00000050: 00 04 ff ff ff f9 00 00  00 00 00 00 00 00 00 00  |................|
    00000060: 00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
    *
    00000090: 00 00 00 00 00 00 00 00  00 00 1f ff ff ff ff f8  |................|
    000000a0: 00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
    *
    000000e0: 00 00 00 7f ff ff ff ff  fe c0                    |..........      |
b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_a9a181eb}$t3g0"
    00000000: 70 69 63 6f 43 54 46 7b  37 68 33 72 33 5f 31 35  |picoCTF{7h3r3_15|
    00000010: 5f 6e 30 5f 35 70 30 30  6e 5f 61 39 61 31 38 31  |_n0_5p00n_a9a181|
    00000020: 65 62 7d 24 74 33 67 30  00 00 00 00 00 00 00 00  |eb}$t3g0........|
    00000030: 00 00 00 00 00 00 00 00  00 00 00 00 00 00 00 00  |................|
    *
    000000f0: 00 00 00 00 01 42 f3 6d  b6 db 6d b6 db 6d b6 db  |.....B.m..m..m..|
b1,abgr,lsb,xy      .. text: "E2A5q4E%uSA"
    00000000: 61 03 15 16 66 31 45 21  24 17 51 37 62 06 45 32  |a...f1E!$.Q7b.E2|
    00000010: 41 35 71 34 45 25 75 53  41 05 71 35 61 06 00 30  |A5q4E%uSA.q5a..0|
    00000020: 66 15 75 14 43 a3 01 3c  4b 86 05 95 68 97 b1 99  |f.u.C..<K...h...|
    00000030: ed 06 45 17 41        

```

## Bandera
Flag: picoCTF{7h3r3_15_n0_5p00n_a9a181eb}


## Notas adicionales


## Referencias
