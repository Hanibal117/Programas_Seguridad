
#### Description

Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/89b371a46702a31aa9931a2a2b12f8bf/pico_img.png).

## Pistas

What does meta mean in the context of files?
Ever heard of metadata?

## Solución

``` 
con  la herramienta binwalk descomprimimos para despues usar 
 file pico_img.png, despues strings pico_img.png | grep pico
y listo
picoCTF{s0_m3ta_eb36bf44}

```

## Bandera
Flag: picoCTF{s0_m3ta_eb36bf44} 


## Notas adicionales


## Referencias
