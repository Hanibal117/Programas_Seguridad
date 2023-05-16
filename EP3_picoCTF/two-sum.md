
 
#### Description

Can you solve this?What two positive numbers can make this possible: `n1 > n1 + n2 OR n2 > n1 + n2`Enter them here `nc saturn.picoctf.net 63253`. [Source](https://artifacts.picoctf.net/c/456/flag.c)


## Pistas

Integer overflow



## Solución

```
a; cehcar el codigo vemos que requerimos de 2 numeros para la bandera uno que haga overflow y otro menor positivo, en este caso el 1
2147483647 y 1.
por lo que ingresamos con un echo
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ echo -e "2147483647\n1" | nc saturn.picoctf.net 63253
n1 > n1 + n2 OR n2 > n1 + n2 
What two positive numbers can make this possible: 
You entered 2147483647 and 1
You have an integer overflow
YOUR FLAG IS: picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_ccd078bd}

                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ 
```

## Bandera
Flag: picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_ccd078bd}


## Notas adicionales


## Referencias
