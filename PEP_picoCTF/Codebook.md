#### Description

Run the Python script `code.py` in the same directory as `codebook.txt`.

-   [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
-   [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)

## Pistas

On the webshell, use `ls` to see if both files are in the directory you are in


## Solución

``` 
hannlec117-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/codebook.txt
--2023-03-26 00:06:52--  https://artifacts.picoctf.net/c/1/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.120, 108.156.172.42, 108.156.172.6, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.120|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                                              100%[==================================================================================================================================>]      27  --.-KB/s    in 0s      

2023-03-26 00:06:52 (1.68 MB/s) - 'codebook.txt' saved [27/27]

hannlec117-picoctf@webshell:~$ ls -la
total 868
drwxr-xr-x 3 hannlec117-picoctf hannlec117-picoctf   4096 Mar 26 00:06 .
drwxr-xr-x 3 root               root                   32 Mar  2 14:53 ..
-rw------- 1 hannlec117-picoctf hannlec117-picoctf   1498 Mar 26 00:03 .bash_history
-rw-r--r-- 1 hannlec117-picoctf hannlec117-picoctf    220 Mar  2 14:53 .bash_logout
-rw-r--r-- 1 hannlec117-picoctf hannlec117-picoctf   3771 Mar  2 14:53 .bashrc
-rw------- 1 hannlec117-picoctf hannlec117-picoctf     20 Mar 25 23:23 .lesshst
-rw-r--r-- 1 hannlec117-picoctf hannlec117-picoctf    807 Mar  2 14:53 .profile
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf    215 Mar 25 23:01 .wget-hsts
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf      0 Mar  2 15:06 0x3D
drwxr-xr-x 3 hannlec117-picoctf hannlec117-picoctf     28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf   4521 Mar 16  2021 Addadshashanammu.zip
-rw-r--r-- 1 root               root                 4443 Mar 26 00:06 README.txt
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf   1278 Mar 16 03:15 code.py
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf     27 Mar 16 03:15 codebook.txt
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf   1189 Mar 16 03:15 convertme.py
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf     34 Mar 16  2021 flag
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf    785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf      0 Mar  2 15:24 output.txt
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf      0 Mar  2 15:06 python
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf    270 Mar 16 03:15 runme.py
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf   8376 Mar 16  2021 static
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf 776032 Oct 26  2020 strings
-rwxrwxr-x 1 hannlec117-picoctf hannlec117-picoctf  10936 Mar 16  2021 warm
hannlec117-picoctf@webshell:~$ python3 code.py 
picoCTF{c0d3b00k_455157_d9aa2df2}
hannlec117-picoctf@webshell:~$ 

solo corri python3 code.py  despues de descargar os archivos con wget en la web shell

picoCTF{c0d3b00k_455157_d9aa2df2}

```

## Bandera
Flag: picoCTF{c0d3b00k_455157_d9aa2df2}


## Notas adicionales


## Referencias
