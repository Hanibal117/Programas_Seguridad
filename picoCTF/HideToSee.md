
 
#### Description

How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/237/atbash.jpg).

## Pistas
Download the image and try to extract it.


## Solución

``` 
Descargamos el archivo y tecleamos lo siguiente:
steghide extract -sf atbash.jpg
luego damos enter
se genera lo siguiente:
wrote extracted data to "encrypted.txt".
le damos cat encrypted.txt
para que nos arroje: krxlXGU{zgyzhs_xizxp_05y2z65z}
ya nadamas nos metemos al link: https://www.dcode.fr/atbash-cipher
para meter el mensaje y que nos de la password
```

## Bandera
Flag: picoCTF{atbash_crack_05b2a65a}


## Notas adicionales


## Referencias
