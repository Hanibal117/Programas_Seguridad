#### Description

Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)

## Pistas


## Solución

``` 

hannlec117-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2023-03-25 23:30:27--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.74, 108.156.172.6, 108.156.172.120, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py                                                  100%[==================================================================================================================================>]     270  --.-KB/s    in 0s      

2023-03-25 23:30:27 (109 MB/s) - 'runme.py' saved [270/270]

hannlec117-picoctf@webshell:~$ ls
0x3D  Addadshashanammu  Addadshashanammu.zip  README.txt  file  flag  ltdis.sh  output.txt  python  runme.py  static  strings  warm
hannlec117-picoctf@webshell:~$ python3 runme.py 
picoCTF{run_s4n1ty_run}
hannlec117-picoctf@webshell:~$ 


```

## Bandera
Flag:  picoCTF{run_s4n1ty_run}

## Notas adicionales


## Referencias
