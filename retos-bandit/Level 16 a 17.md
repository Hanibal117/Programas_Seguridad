 ## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Datos de acceso al nivel 
ssh bandit16@bandit.labs.overthewire.org -p 2220
JQttfApK4SeyHwDlI9SXGR50qclOAil1

ssh, telnet, nc, openssl, s_client, nmap
 

## Solución

``` 
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 22:02:58 2023 GMT; NotAfter: Feb 21 22:03:58 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIELZxFNDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMjIwMjU4WhcNMjMwMjIxMjIwMzU4WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC8
C8jJ2//6TxiFBwjuC7+xUcu293V+n8pLxHfVnpZG9fvlOBG3nA3hm2/iNYybZNla
R58hZmfPWEKcuX7GZGvNUOAa6wOg2WYrMo1+6NCcynmCdJEabv2kemvOtBQFeV43
EUW+BW/+6903QuSHsjDewSoljGtmRGjg0oXUgyOlzGDQR/EfX7N8KGubYzZcHf+i
uZ35xMF5HQWi7Zf2ObapcbIfyjw2JWQLVqa8eDbZ4R4HKXYBLeJ4rZoYbPO1JUuX
IY6g+zV0yrgeX3EE36S4fYG/c5eixWRsA+KMYdJjtd2JTvEyyU9kSRQBNIJQOlmH
956MMGFmMqXn+kus9wgbAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCQ
ZF30iIq43MI9neBsmpAg3W5GsZzzV/JVOPDK1BG1ynEF5hqd6SFuRRSNXXy1AN3O
jL5m5B8sIh53vzfDBhv5XgSeKDm8KPqNn9CF5yP+neVglcJh3frf6DX4yE4yntHZ
SyxWErfMX/s5P1W4NdNoph6zNWBN5EjPls9mYo4gfkUnS72FDLfyGmPan8WKUP00
hhK6TdtbcetA/9HODOD2QL82tugZvCK9qPnNHG9TkcgaJ8LW9AY/ZCwnIYsODUQi
gYSDr2Ya4GuSAp2Vn4KkaJ1+NGmE+AxUMJ0rNsKUg6JelZ6vZ4TcFNbOSqaiCOtj
5xezGlZxL+dTerQ6hBwn
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
    Session-ID: 493A15C5D0EA663CA176F9EF1AB05EB9258BAB859CCF971834ACD9684150335E
    Session-ID-ctx:
    Resumption PSK: E66303AB7A2134E9A1FB7CDEE3666E50AB80F35A69D761F231EC952F7A069FCE9201C011275C571A8B2573E62B7BF372
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 95 2e e7 a1 1d 80 9c 03-72 3e 59 c8 7b 8a 46 77   ........r>Y.{.Fw
    0020 - 77 f8 e9 2f 53 44 69 6d-10 a0 49 fb c5 18 32 c4   w../SDim..I...2.
    0030 - c5 4d 35 a7 ee ae 2e 70-8b 19 2b ac 16 dd b9 06   .M5....p..+.....
    0040 - dd 33 46 e9 85 ff c5 29-76 8c d2 b8 90 79 62 1d   .3F....)v....yb.
    0050 - 7e 05 7a 13 0d 39 b4 b0-4c 97 0b f0 7d c5 79 85   ~.z..9..L...}.y.
    0060 - 25 c5 fc ff 80 e1 64 c7-4b 58 69 77 e2 ae 4d 40   %.....d.KXiw..M@
    0070 - 34 78 f0 02 dc d8 9d 18-0c 65 f4 e1 e5 ff 3a 40   4x.......e....:@
    0080 - 11 bf 6e ca 1d 5f 7a 4f-e4 70 7b 8d 73 8e 4e 74   ..n.._zO.p{.s.Nt
    0090 - 8c 85 55 e9 33 18 f4 69-51 1e fd 43 b5 70 4e 71   ..U.3..iQ..C.pNq
    00a0 - 1e ff 7b 3e 96 17 af b4-ff b2 00 34 2c 88 a2 43   ..{>.......4,..C
    00b0 - 95 3b 13 30 99 cc 81 e6-b9 5d 14 22 c2 27 fd ad   .;.0.....].".'..
    00c0 - 10 39 ee 20 29 e0 d7 25-d3 97 84 de 8c 8c e6 e2   .9. )..%........

    Start Time: 1677162393
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
    Session-ID: 626A26A195BC9BF4541FE016AC815CFDCB585BFE21BBF60F77569F00CD897507
    Session-ID-ctx:
    Resumption PSK: 4348A0A149951C1261AF25559AABEC589A3E30DF6C5770B068B9BF14B63072346EDDD3283819ADCCC3B17AA1B8BE7C01
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 24 3a 1f 3c 34 12 55 d9-49 99 c9 64 d6 20 25 ea   $:.<4.U.I..d. %.
    0020 - fa 27 fe b8 71 28 94 d1-cb 1b 84 49 00 6a aa f2   .'..q(.....I.j..
    0030 - 61 0a 79 f7 73 f2 db d4-73 08 52 fe b7 4c 93 55   a.y.s...s.R..L.U
    0040 - a9 4b 3a 11 be 7f a6 aa-96 d8 c0 a4 2b cd 73 96   .K:.........+.s.
    0050 - ad df 41 29 89 32 4c 1a-51 35 32 55 f1 62 73 b7   ..A).2L.Q52U.bs.
    0060 - 48 dd 19 be e4 48 3e 85-a1 d6 36 9c cc e7 af 8f   H....H>...6.....
    0070 - cc ee 02 43 bb 14 00 17-a0 1e 05 52 03 81 04 ec   ...C.......R....
    0080 - b2 e1 4a c5 35 d7 24 66-b9 8a a8 ac 99 40 21 50   ..J.5.$f.....@!P
    0090 - c7 59 ce 09 25 99 ac 20-a7 ea a2 37 30 17 88 5f   .Y..%.. ...70.._
    00a0 - 2b ed 7d 4a ff 30 82 e5-8e 98 86 00 a0 1b 91 cc   +.}J.0..........
    00b0 - 57 7d 3d 92 c1 f8 22 3e-db 91 ef c4 8a e2 7f ce   W}=...">........
    00c0 - fe 4c d2 43 fc 55 d5 6a-49 e4 9b 0e 29 7e 5a c9   .L.C.U.jI...)~Z.

    Start Time: 1677162393
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK

Wrong! Please enter the correct current password
closed
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 22:02:58 2023 GMT; NotAfter: Feb 21 22:03:58 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIELZxFNDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMjIwMjU4WhcNMjMwMjIxMjIwMzU4WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC8
C8jJ2//6TxiFBwjuC7+xUcu293V+n8pLxHfVnpZG9fvlOBG3nA3hm2/iNYybZNla
R58hZmfPWEKcuX7GZGvNUOAa6wOg2WYrMo1+6NCcynmCdJEabv2kemvOtBQFeV43
EUW+BW/+6903QuSHsjDewSoljGtmRGjg0oXUgyOlzGDQR/EfX7N8KGubYzZcHf+i
uZ35xMF5HQWi7Zf2ObapcbIfyjw2JWQLVqa8eDbZ4R4HKXYBLeJ4rZoYbPO1JUuX
IY6g+zV0yrgeX3EE36S4fYG/c5eixWRsA+KMYdJjtd2JTvEyyU9kSRQBNIJQOlmH
956MMGFmMqXn+kus9wgbAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCQ
ZF30iIq43MI9neBsmpAg3W5GsZzzV/JVOPDK1BG1ynEF5hqd6SFuRRSNXXy1AN3O
jL5m5B8sIh53vzfDBhv5XgSeKDm8KPqNn9CF5yP+neVglcJh3frf6DX4yE4yntHZ
SyxWErfMX/s5P1W4NdNoph6zNWBN5EjPls9mYo4gfkUnS72FDLfyGmPan8WKUP00
hhK6TdtbcetA/9HODOD2QL82tugZvCK9qPnNHG9TkcgaJ8LW9AY/ZCwnIYsODUQi
gYSDr2Ya4GuSAp2Vn4KkaJ1+NGmE+AxUMJ0rNsKUg6JelZ6vZ4TcFNbOSqaiCOtj
5xezGlZxL+dTerQ6hBwn
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
    Session-ID: 74A807D6357907325EADCEFD74205777E4C3E1D1907D1E99AE3F973E4703E707
    Session-ID-ctx:
    Resumption PSK: C886E6359A4EF38C7B7C0D18B8412B60A3C3E425FA09A7B54FF14ABE62D14C21CAE8D61FDDDE8E08CF9EB9DCFC7E0C30
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 16 36 93 cf 44 be 4c 74-22 79 36 a7 d2 48 84 d0   .6..D.Lt"y6..H..
    0020 - 83 40 33 f5 e8 76 c5 66-7b 2b 6c d3 2c 5c c2 2b   .@3..v.f{+l.,\.+
    0030 - 61 ab 7b 06 90 60 7e ad-c9 6f 8a 7c 37 99 cd 40   a.{..`~..o.|7..@
    0040 - f0 c6 34 8e 7c 00 ed 1a-a4 aa cd c9 57 e7 84 ec   ..4.|.......W...
    0050 - c2 d2 82 b7 bb c9 ad 7a-0a 2b 1e 98 54 74 b6 0d   .......z.+..Tt..
    0060 - 12 69 d6 35 ca 60 e9 6b-76 7c 30 c0 44 84 96 d7   .i.5.`.kv|0.D...
    0070 - 19 55 47 40 ed b9 34 fd-69 46 0f ae 22 71 e0 1e   .UG@..4.iF.."q..
    0080 - d3 6d c5 74 96 eb d5 c9-c8 08 8f c6 4b 23 1a 14   .m.t........K#..
    0090 - 2e d8 00 e9 07 fe 20 97-8d 10 99 4c 37 9d 8f 66   ...... ....L7..f
    00a0 - 3b ee 99 15 5f b8 b3 39-61 89 1f 53 db b0 f6 f5   ;..._..9a..S....
    00b0 - f2 b4 07 7a ef e7 54 3b-11 50 22 56 fb 98 84 37   ...z..T;.P"V...7
    00c0 - be f1 5a 95 91 a1 ce dd-b9 9f 6e 33 5a d9 bd b1   ..Z.......n3Z...

    Start Time: 1677162424
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
    Session-ID: FBE68BBBE0773649B568B87FEBC356B38480AA20D4B050116FDC04F60BF1DD30
    Session-ID-ctx:
    Resumption PSK: 295BC70F17AF67E10B6ED5CFB94229ED232D73EA15BCE74BF171F1D02D3D8CC374F3C48A724C02950BE2B15E55C7A533
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 4d af f8 9e 50 51 24 5b-8b 35 ab 9a 21 4a 90 b3   M...PQ$[.5..!J..
    0020 - 0c b5 59 13 df 33 76 4b-92 f5 f1 0e 12 61 af 47   ..Y..3vK.....a.G
    0030 - b1 46 52 f1 8b 37 f2 1c-06 3a 40 a3 37 20 55 1c   .FR..7...:@.7 U.
    0040 - a8 bf 2a 15 2e 43 4f 8f-10 d9 de 7e e4 85 20 1c   ..*..CO....~.. .
    0050 - b8 44 9c 2f ce af 36 52-d2 07 44 82 56 7f e7 03   .D./..6R..D.V...
    0060 - ce 08 72 fb 1c 37 f4 d2-47 68 24 56 50 94 1f 81   ..r..7..Gh$VP...
    0070 - 17 10 86 36 c6 39 58 a7-99 d7 0f 10 1d b7 5f 9d   ...6.9X......._.
    0080 - 50 be bd 8f 4a b5 7d 93-42 e7 c5 20 09 fa ec 7e   P...J.}.B.. ...~
    0090 - a0 81 5a 91 a8 9c f7 55-70 7f e1 ef 4d 84 50 ad   ..Z....Up...M.P.
    00a0 - 20 b9 9c c1 be b9 f0 bf-c0 04 45 ed dd f9 6f 38    .........E...o8
    00b0 - 73 57 f6 a3 1f 78 a9 05-ad d0 41 43 01 b2 75 3e   sW...x....AC..u>
    00c0 - d3 93 4d 42 b7 d4 20 2c-20 3c 49 f8 a2 08 a5 82   ..MB.. , <I.....

    Start Time: 1677162424
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
bandit16@bandit:~$ exit



C:\Users\castr>notepad llave.txt C:\Users\JESUS>type llave.txt
-----BEGIN RSA PRIVATE KEY----- MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama +TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT 8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM 77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3 vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY= 
-----END RSA PRIVATE KEY----- 

C:\Users\JESUS>ssh -i llave.txt 
bandit17@bandit.labs.overthewire.org -p2220 
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17 
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e 
bandit17@bandit:~$ exit


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
https://en.wikipedia.org/wiki/Port_scanner
