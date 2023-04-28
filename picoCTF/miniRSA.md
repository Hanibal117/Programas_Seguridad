AUTHOR: SARA

## Description

What happens if you have a small exponent? There is a twist though, we padded the plaintext so that (M ** e) is just barely larger than N. Let's decrypt this: [ciphertext](https://mercury.picoctf.net/static/a9d46a88f2602fa48edf086a5afbfed8/ciphertext)

## Pista 

How could having too small of an `e` affect the security of this key?


## Solución

``` 
Descargue el archivo y puse lo siguiente en python3

>>> from gmpy2 import *
>>> from Crypto.Util.number import  long_to_bytes
>>> 
>>> gmpy2.get_context().precision=2048
>>> e=3
>>> c=2205316413931134031074603746928247799030155221252519872649649212867614751848436763801274360463406171277838056821437115883619169702963504606017565783537203207707757768473109845162808575425972525116337319108047893250549462147185741761825125
>>> 
>>> root, exact = iroot(c,e)
>>> root
mpz(13016382529449106065894479374027604750406953699090365388202874238148389207291005)
>>> 
>>> print(long_to_bytes(root) )
b'picoCTF{n33d_a_lArg3r_e_606ce004}'
>>> 




```

## Bandera
Flag: picoCTF{n33d_a_lArg3r_e_606ce004}



## Notas adicionales


## Referencias
