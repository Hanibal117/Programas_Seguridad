#### Description

To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 15130`.

## Pistas

I hear python can convert things.
It might help to have multiple windows open.


## Solución

``` 
son 3 conversiones

1: Binario to text
2: Octal to text
3: Hexa to ascii


hannlec117-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 15130
Let us see how data is stored
lime
Please give the 01101100 01101001 01101101 01100101 as a word.
...
you have 45 seconds.....

Input:
lime
Please give me the  143 157 155 160 165 164 145 162 as a word.
Input:
computer
Please give me the 736c75646765 as a word.
Input:
sludge
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_02167de8}

```

## Bandera
Flag: picoCTF{learning_about_converting_values_02167de8}


## Notas adicionales



## Referencias
https://www.rapidtables.com/convert/number/binary-to-ascii.html
http://www.unit-conversion.info/texttools/octal/
https://onlinehextools.com/convert-hex-to-ascii
