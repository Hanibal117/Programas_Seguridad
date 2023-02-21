 ## Objetivo
he password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**



## Datos de acceso al nivel 
ssh bandit15@bandit.labs.overthewire.org -p 2220
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

ssh, telnet, nc, openssl, s_client, nmap
 

## Solución

``` 
bandit15@bandit:~$ bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 06:20:29 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 06:20:29 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 06:19:29 2023 GMT; NotAfter: Feb 21 06:20:29 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEA7qUdzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMDYxOTI5WhcNMjMwMjIxMDYyMDI5WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDL
vM0gZzAHdXTeD5t4ruUJo/kRs4UAodA9XcqDhNtW464W0c55RqKLp921syy3Lvjr
8Q9WkqvCFX+efShMd8XnzbT/dyRrD+cZQnSiPJ3bwDdpwqfkl9h3mb609Kb5HI6R
JgogEyuRLJI+HKtr/wXHwo1vBZ0+yaPMX6sdkd6Hu5Ra0L5Q5+E5+3F/8QgvCeVE
hDRIOrh2a7jxykb8G6+xVC6jIZY0YfrZz6LrESyQau256pqyaQPqQoUWTlitxIql
Ym2Baw7vYDxmFZrvj0FkumC6NokX6K2G9bZ0DaKR/DspPdAC4oT81SawJvsBibdN
51VI6dxBn412ZS8bS155AgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQA9
skxWNwZbedjaVTa5yMPUZQ4Nf5/LAAMtS5Q7mzGH5tdQsTGR0Z4n4eA4hzrmzHBF
MVRL5mR9n+sM5pIrKDa6f4zIc5ObxDyN19ie+3SFASCPz9tihK8Js2V8qsR6LHV1
pfD8DSG0hZPtUuK3Mfi+nWqQUFiiTGj30mb9vlS1sSWv5PGznou1gQ3ZfrDs7B4K
ZKZrllPIVV1CrlDw2Bv8Dc432LQuZAmKAjBd6FG0OAboU/WJMTwAfVjlKMtvC8tg
DZ3djSTprq6PrXlI0utw/MsMIh69b61BRXUuDvRxhU11SNmSI8aegjVL8KuK+Euh
sSLPTocV29SY1YXOwEQi
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: E92D8F2719585BAC290E833125B407898DC0ABD877C550C414B21EA565D727D8
    Session-ID-ctx:
    Resumption PSK: 9E9E277C9596DBF4A5974E954A64A22FF021D18132B5404007479D092907971B33CAD6D50BE147356966903BEFF2039D
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - ee ae 09 e4 56 06 6c 9e-c9 80 86 77 50 83 15 59   ....V.l....wP..Y
    0010 - 3d f2 8a 99 45 9d 84 de-0b 7d e3 98 95 da 88 d4   =...E....}......
    0020 - 9c e7 0e 5a 79 bc cb b5-14 c0 6c b7 ee a4 63 8e   ...Zy.....l...c.
    0030 - cb 6a 8b 6c 79 95 5f 58-8e 2b d2 65 58 33 8e db   .j.ly._X.+.eX3..
    0040 - 4f 04 1d b0 3c d8 cb 20-c3 55 28 89 43 6c ee 57   O...<.. .U(.Cl.W
    0050 - f4 fc d1 28 fb 71 26 4c-89 67 2d 94 8f 87 98 df   ...(.q&L.g-.....
    0060 - 82 ca 24 73 29 88 e7 03-cc 29 73 c5 b4 ea 05 60   ..$s)....)s....`
    0070 - 64 2c fc fc 46 42 60 65-6e fe 4b 32 4f d3 23 40   d,..FB`en.K2O.#@
    0080 - 7d 9b 56 81 4f 13 ee c3-9b 24 50 f5 17 ce 85 f3   }.V.O....$P.....
    0090 - f1 64 39 59 3c 7d ca 06-0f db 30 38 42 43 e7 96   .d9Y<}....08BC..
    00a0 - 7d 60 1d 39 47 7a 38 4a-b9 f6 0f e2 99 ae 6f 96   }`.9Gz8J......o.
    00b0 - 99 2f ef 2f 86 59 3a 17-34 3b 96 db bb 65 85 c5   ././.Y:.4;...e..
    00c0 - 9c a4 a2 fb a5 08 bc 43-76 a3 af c4 fd d6 ec 58   .......Cv......X

    Start Time: 1676997690
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: E0FE45620B6B24F2A9B3EC0E64A73CB11BA452CC26020B02AA60A1F96F6A512B
    Session-ID-ctx:
    Resumption PSK: EE1BBA3910C911F3DB22FF84918A6CD24F05F309E3868A92299812577AA852504BB5BB536FB9DAD733ACEA9EBB31FCD7
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - ee ae 09 e4 56 06 6c 9e-c9 80 86 77 50 83 15 59   ....V.l....wP..Y
    0010 - 37 87 8b 6b 28 05 d7 b0-9d bb e6 ae c6 1b be d0   7..k(...........
    0020 - 8c 38 b7 91 1f a0 c9 ad-ae 5b b5 57 27 d9 c4 ec   .8.......[.W'...
    0030 - fd 07 bc 54 f5 c2 42 8d-c5 08 75 15 8b 16 8a 5d   ...T..B...u....]
    0040 - 8f 49 cf 66 4b 6f 9b d0-d7 29 6d a3 bb ab e4 ab   .I.fKo...)m.....
    0050 - 98 71 b1 8c 87 03 ec f9-22 1d d4 34 ae e7 a0 08   .q......"..4....
    0060 - e9 49 38 d4 cd e0 4e 3d-60 11 53 a3 38 53 ec b9   .I8...N=`.S.8S..
    0070 - ac 96 b3 6b 47 e4 ef 9b-5b 80 57 8d 22 d9 27 d5   ...kG...[.W.".'.
    0080 - 2b 46 e5 b0 b0 26 c7 c9-9d 51 32 df 36 57 f2 0f   +F...&...Q2.6W..
    0090 - 5a b7 f0 ee d3 4b 21 5e-a0 62 53 0e 62 97 2f 22   Z....K!^.bS.b./"
    00a0 - 36 90 66 db 5f 1f b4 94-fb 3f 60 b6 14 82 a8 34   6.f._....?`....4
    00b0 - e7 4a dd 77 db b5 ef 07-6e 8f 10 ec 2e 1b 57 e0   .J.w....n.....W.
    00c0 - da 40 83 60 9b 78 97 76-ee 2b 30 1a db ee e8 7c   .@.`.x.v.+0....|

    Start Time: 1676997690
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed

```


## Notas adicionales
- ls listar archivo
- emite contenido de lineas de comando
- ls -lh  Lista el contenido en un tamaño (human readable) más entendible por el usuario. Por defecto el tamaño se muestra en bytes, pero al usar -h nos lo muestra en una unidad más legible para las personas.
- pwd saca la ruta actual
- | wc -l cuenta cunatos archivos hay
- grep  "millionth" data.txt ayuda a buscar y encontrar la coincidencia con lo que buscamos
- sort ordena de manera alfabetica todas las lineas
- uniq -u aparece la unica linea
- strings lista caracteres "data.txt"
- echo imprime un texto a la pantalla
- base64 convierte datos decodificando
- tr permite al Usuario definir explícitamente como estará compuesto el conjunto o bien provee de una colección de caracteres y conjuntos predefinidos, que puede ser utilizados a la hora de definirlos
- xdd Crea un volcado hexadecimal de un archivo 
- No dejar la llave sin cuidar
- 

## Referencias
https://en.wikipedia.org/wiki/Secure_Socket_Layer
https://www.feistyduck.com/library/openssl-cookbook/online/ch-testing-with-openssl.html
