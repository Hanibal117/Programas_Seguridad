
#### Description

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.


## Pistas


## Solución

 
```
from scapy.all import *

packets = rdpcap('capture.pcap')

flag =''

for p in packets :
         if UDP in p and p[UDP].dport ==22 :
          if p[UDP].sport>5000:
                flag += chr(p[UDP].sport - 5000)
                
print(flag)

## Bandera
Flag: picoCTF{p1LLf3r3d_data_v1a_st3g0}



## Notas adicionales


## Referencias
[picoCTF 2019 writeup [23] - Forensic - shark on wire 2 - YouTube](https://www.youtube.com/watch?v=WcMl1SvQ6hI&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=24)

