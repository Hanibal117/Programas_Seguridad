#### Description

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

## Pistas

Try using a tool like Wireshark.


## Solución

``` 
ssldump -r capture.pcap -k picopico.key -d
descargue los paquetes y me dio la bandera 

 picoCTF{nongshim.shrimp.crackers}
```

## Bandera
Flag:  picoCTF{nongshim.shrimp.crackers}


## Notas adicionales


## Referencias
