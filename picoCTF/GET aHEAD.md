
#### Description

Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:15931/](http://mercury.picoctf.net:15931/)

## Pistas


Check out tools like Burpsuite to modify your requests and look at the responses
## Solución


con  el software burp suite accedi con el proxy a la pagina para cambiar el SEND A HEAD pasandola a Repeater para obtener la bandera
```
HTTP/1.1 200 OK

flag: picoCTF{r3j3ct_th3_du4l1ty_82880908}

Content-type: text/html; charset=UTF-8

flag: picoCTF{r3j3ct_th3_du4l1ty_82880908}
```

## Bandera
flag: picoCTF{r3j3ct_th3_du4l1ty_82880908}


## Notas adicionales


## Referencias
