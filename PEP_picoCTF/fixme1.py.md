#### Description

Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)


## Pistas

Indentation is very meaningful in Python
To view the file in the webshell, do: `$ nano fixme1.py`
To exit `nano`, press Ctrl and x and follow the on-screen prompts.
The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución

``` 
Edite el codigo de la siguiente manera:

import random



def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)
        
    print("XD")    
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])


flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + chr(0x07) + chr(0x00) + chr(0x46) + chr(0x0b) + chr(0x1a) + chr(0x5a) + chr(0x1d) + chr(0x1d) + chr(0x2a) + chr(0x0>

  
flag = str_xor(flag_enc, 'enkidu')

print('That is correct! Here\'s your flag: ' + flag)




XD
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/hacking/EP1]
└─$ 

```

## Bandera
Flag:  picoCTF{1nd3nt1ty_cr1515_09ee727a}


## Notas adicionales


## Referencias
