#### Description

#### Description

Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)
## Pistas


## Solución

``` 
hannlec117-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2023-03-25 23:47:18--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.42, 108.156.172.6, 108.156.172.120, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                                              100%[==================================================================================================================================>]   1.16K  --.-KB/s    in 0s      

2023-03-25 23:47:18 (452 MB/s) - 'convertme.py' saved [1189/1189]

hannlec117-picoctf@webshell:~$ ls
0x3D  Addadshashanammu  Addadshashanammu.zip  README.txt  convertme.py  file  flag  ltdis.sh  output.txt  python  runme.py  static  strings  warm
hannlec117-picoctf@webshell:~$ ls -la
total 860
drwxr-xr-x 3 hannlec117-picoctf hannlec117-picoctf   4096 Mar 25 23:47 .
drwxr-xr-x 3 root               root                   32 Mar  2 14:53 ..
-rw------- 1 hannlec117-picoctf hannlec117-picoctf   1343 Mar 25 23:23 .bash_history
-rw-r--r-- 1 hannlec117-picoctf hannlec117-picoctf    220 Mar  2 14:53 .bash_logout
-rw-r--r-- 1 hannlec117-picoctf hannlec117-picoctf   3771 Mar  2 14:53 .bashrc
-rw------- 1 hannlec117-picoctf hannlec117-picoctf     20 Mar 25 23:23 .lesshst
-rw-r--r-- 1 hannlec117-picoctf hannlec117-picoctf    807 Mar  2 14:53 .profile
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf    215 Mar 25 23:01 .wget-hsts
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf      0 Mar  2 15:06 0x3D
drwxr-xr-x 3 hannlec117-picoctf hannlec117-picoctf     28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 hannlec117-picoctf hannlec117-picoctf   4521 Mar 16  2021 Addadshashanammu.zip
-rw-r--r-- 1 root               root                 4443 Mar 25 23:30 README.txt
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
hannlec117-picoctf@webshell:~$ python3 convertme.py 
If 32 is in decimal base, what is it in binary base?
Answer: 100000
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
hannlec117-picoctf@webshell:~$ 
```
Descargue el archipo de la web shell
para despues usar python3 convertme.py
me pidio transfommrar el 32 a binario, despues use una pagina para convertir de dec a bin , puse : 100000
y me dio la flag

## Bandera
Flag:  picoCTF{4ll_y0ur_b4535_722f6b39}

## Notas adicionales


## Referencias
https://www.rapidtables.org/convert/number/decimal-to-binary.html
