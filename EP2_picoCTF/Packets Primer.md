
 
#### Description

Download the packet capture file and use packet analysis software to find the flag.
  [Download packet capture](https://artifacts.picoctf.net/c/196/network-dump.flag.pcap)


## Pistas
Wireshark, if you can install and use it, is probably the most beginner friendly packet analysis software product.


## Solución

```
observamos al descargar el archivo despues de analizar, que el TCP No.4 tiene la flag

0000   08 00 27 93 ce 73 08 00 27 af 39 9f 08 00 45 00   ..'..s..'.9...E.
0010   00 70 50 c2 40 00 40 06 d1 b3 0a 00 02 0f 0a 00   .pP.@.@.........
0020   02 04 be 6e 23 28 27 ec d4 b7 bd 26 99 bc 80 18   ...n#('....&....
0030   01 f6 18 75 00 00 01 01 08 0a 8d cf e9 65 68 f0   ...u.........eh.
0040   f1 c3 70 20 69 20 63 20 6f 20 43 20 54 20 46 20   ..p i c o C T F 
0050   7b 20 70 20 34 20 63 20 6b 20 33 20 37 20 5f 20   { p 4 c k 3 7 _ 
0060   35 20 68 20 34 20 72 20 6b 20 5f 20 30 20 31 20   5 h 4 r k _ 0 1 
0070   62 20 30 20 61 20 30 20 64 20 36 20 7d 0a         b 0 a 0 d 6 }.

```

## Bandera
Flag: picoCTF{p4ck37_5h4rk_01b0a0d6}

## Notas adicionales


## Referencias
