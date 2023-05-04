
 
#### Description

The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:55771/) out.

## Pistas




## Solución

``` 
Ponemos robots.txt al link para acceder
http://saturn.picoctf.net:55771/robots.txt
y nos mostrara lo siguiente:
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/
con ayuda de un decodifciador en base64 online nos arroja lo siguiente:
js/myfile.tx
se lo ponemos al link priginal y alli esta la flag
http://saturn.picoctf.net:55771/js/myfile.txt

```

## Bandera
Flag: picoCTF{Who_D03sN7_L1k5_90B0T5_22ce1f22}


## Notas adicionales


## Referencias
