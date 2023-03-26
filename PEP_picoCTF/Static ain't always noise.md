
#### Description

Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/static)? This [BASH script](https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/ltdis.sh) might help!

## Pistas



## Solución

``` 
                hannlec117-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/static
--2023-03-25 22:58:51--  https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static'

static                                                    100%[==================================================================================================================================>]   8.18K  --.-KB/s    in 0s      

2023-03-25 22:58:51 (333 MB/s) - 'static' saved [8376/8376]

hannlec117-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/ltdis.sh
--2023-03-25 22:59:03--  https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh                                                  100%[==================================================================================================================================>]     785  --.-KB/s    in 0s      

2023-03-25 22:59:03 (420 MB/s) - 'ltdis.sh' saved [785/785]

hannlec117-picoctf@webshell:~$ ls
0x3D  README.txt  file  flag  ltdis.sh  output.txt  python  static  strings  warm
hannlec117-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_98d35619}
```

## Bandera
Flag: picoCTF{d15a5m_t34s3r_98d35619}


## Notas adicionales


## Referencias
