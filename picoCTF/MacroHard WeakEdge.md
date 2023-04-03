#### Description

I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/3944a59474f9f676942282c50b9c3675/Forensics%20is%20fun.pptm)


## Pistas



## Solución

``` 
Descargamos el archivo de la pagina despues extraemos como si fuera un zip 
binwalk -e "Forensics is fun.pptm"
luego abrimos para encontrar lo siguiente Hidden encontrando 
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q esto es base 64 por lo que usaremos una pagina para desencriptar  
a lo  que nos arroja 
picoCTF{D1d_u_kn0w_ppts_r_z1p5}
```


## Bandera
Flag: picoCTF{61}


## Notas adicionales


## Referencias
