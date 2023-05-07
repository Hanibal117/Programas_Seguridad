
 
#### Description

This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://jupiter.challenges.picoctf.org/static/c695ee23309d453a3ef369c34cc1bccb/VaultDoor4.java)

## Pistas

Use a search engine to find an "ASCII table".


## Solución

``` 
Descargamos el archivo
     byte[] myBytes = {
            106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0142, 0131, 0164, 063 , 0163, 0137, 070 , 0146,
            '4' , 'a' , '6' , 'c' , 'b' , 'f' , '3' , 'b' ,
            aquie esta la bandera
usamos un convertidor de decimal a ascii :
luego de hexa a ascii
https://onlineasciitools.com/convert-decimal-to-ascii
https://www.binaryhexconverter.com/hex-to-ascii-text-converter
https://onlineasciitools.com/convert-octal-to-ascii

al final de octal a ascii

picoCTF{jU5t_4_bUnCh_0f_bYt3s_8f4a6cbf3b}


```

## Bandera
Flag: picoCTF{jU5t_4_bUnCh_0f_bYt3s_8f4a6cbf3b}


## Notas adicionales


## Referencias
