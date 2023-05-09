
 
#### Description

The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/27dd5548b14661f65ce3ac6a8a8f575b/need-for-speed).


## Pistas
What is the final key?

## Solución

``` 
Con un └─$ readelf -S need-for-speed 
There are 29 section headers, starting at offset 0x1b78:

Section Headers:
  [Nr] Name              Type             Address           Offset
       Size              EntSize          Flags  Link  Info  Align
  [ 0]                   NULL             0000000000000000  00000000
       0000000000000000  0000000000000000           0     0     0
  [ 1] .interp           PROGBITS         0000000000000238  00000238
       000000000000001c  0000000000000000   A       0     0     1
  [ 2] .note.ABI-tag     NOTE             0000000000000254  00000254
       0000000000000020  0000000000000000   A       0     0     4
  [ 3] .note.gnu.bu[...] NOTE             0000000000000274  00000274
       0000000000000024  0000000000000000   A       0     0     4
  [ 4] .gnu.hash         GNU_HASH         0000000000000298  00000298
       000000000000001c  0000000000000000   A       5     0     8
  [ 5] .dynsym           DYNSYM           00000000000002b8  000002b8
       0000000000000108  0000000000000018   A       6     1     8
  [ 6] .dynstr           STRTAB           00000000000003c0  000003c0
       00000000000000a3  0000000000000000   A       0     0     1
  [ 7] .gnu.version      VERSYM           0000000000000464  00000464
       0000000000000016  0000000000000002   A       5     0     2
  [ 8] .gnu.version_r    VERNEED          0000000000000480  00000480
       0000000000000020  0000000000000000   A       6     1     8
  [ 9] .rela.dyn         RELA             00000000000004a0  000004a0
       00000000000000c0  0000000000000018   A       5     0     8
  [10] .rela.plt         RELA             0000000000000560  00000560
       0000000000000078  0000000000000018  AI       5    22     8
  [11] .init             PROGBITS         00000000000005d8  000005d8
       0000000000000017  0000000000000000  AX       0     0     4
  [12] .plt              PROGBITS         00000000000005f0  000005f0
       0000000000000060  0000000000000010  AX       0     0     16
  [13] .plt.got          PROGBITS         0000000000000650  00000650
       0000000000000008  0000000000000008  AX       0     0     8
  [14] .text             PROGBITS         0000000000000660  00000660
       0000000000000372  0000000000000000  AX       0     0     16
  [15] .fini             PROGBITS         00000000000009d4  000009d4
       0000000000000009  0000000000000000  AX       0     0     4
  [16] .rodata           PROGBITS         00000000000009e0  000009e0
       000000000000008f  0000000000000000   A       0     0     16
  [17] .eh_frame_hdr     PROGBITS         0000000000000a70  00000a70
       0000000000000074  0000000000000000   A       0     0     4
  [18] .eh_frame         PROGBITS         0000000000000ae8  00000ae8
       00000000000001e8  0000000000000000   A       0     0     8
  [19] .init_array       INIT_ARRAY       0000000000200d98  00000d98
       0000000000000008  0000000000000008  WA       0     0     8
  [20] .fini_array       FINI_ARRAY       0000000000200da0  00000da0
       0000000000000008  0000000000000008  WA       0     0     8
  [21] .dynamic          DYNAMIC          0000000000200da8  00000da8
       00000000000001f0  0000000000000010  WA       6     0     8
  [22] .got              PROGBITS         0000000000200f98  00000f98
       0000000000000068  0000000000000008  WA       0     0     8
  [23] .data             PROGBITS         0000000000201000  00001000
       0000000000000058  0000000000000000  WA       0     0     32
  [24] .bss              NOBITS           0000000000201058  00001058
       0000000000000008  0000000000000000  WA       0     0     4
  [25] .comment          PROGBITS         0000000000000000  00001058
       0000000000000029  0000000000000001  MS       0     0     1
  [26] .symtab           SYMTAB           0000000000000000  00001088
       0000000000000738  0000000000000018          27    43     8
  [27] .strtab           STRTAB           0000000000000000  000017c0
       00000000000002b4  0000000000000000           0     0     1
  [28] .shstrtab         STRTAB           0000000000000000  00001a74
       00000000000000fe  0000000000000000           0     0     1
Key to Flags:
  W (write), A (alloc), X (execute), M (merge), S (strings), I (info),
  L (link order), O (extra OS processing required), G (group), T (TLS),
  C (compressed), x (unknown), o (OS specific), E (exclude),
  D (mbind), l (large), p (processor specific)

da lo siguiente:

┌──(kali㉿kali)-[~/hacking/333/aaa/w]
└─$ objdump -t  need-for-speed | grep ' F .text'
0000000000000690 l     F .text  0000000000000000              deregister_tm_clones
00000000000006d0 l     F .text  0000000000000000              register_tm_clones
0000000000000720 l     F .text  0000000000000000              __do_global_dtors_aux
0000000000000760 l     F .text  0000000000000000              frame_dummy
00000000000009d0 g     F .text  0000000000000002              __libc_csu_fini
000000000000076a g     F .text  0000000000000087              decrypt_flag
000000000000080e g     F .text  0000000000000021              alarm_handler
00000000000008d8 g     F .text  0000000000000042              header
000000000000087d g     F .text  000000000000002f              get_key
0000000000000960 g     F .text  0000000000000065              __libc_csu_init
0000000000000660 g     F .text  000000000000002b              _start
000000000000091a g     F .text  000000000000003e              main
00000000000007f1 g     F .text  000000000000001d              calculate_key
00000000000008ac g     F .text  000000000000002c              print_flag
000000000000082f g     F .text  000000000000004e              set_timer
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/hacking/333/aaa/w]
└─$ 


┌──(kali㉿kali)-[~/hacking/333/aaa/w]
└─$ gdb need-for-speed          
GNU gdb (Debian 13.1-2) 13.1
Copyright (C) 2023 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from need-for-speed...
(No debugging symbols found in need-for-speed)
(gdb) set dissasembly-flavor intel
No symbol table is loaded.  Use the "file" command.
(gdb) set dissasembly-flavor intel
No symbol table is loaded.  Use the "file" command.
(gdb) 
No symbol table is loaded.  Use the "file" command.
(gdb) set dissasembly-flavor intel
No symbol table is loaded.  Use the "file" command.
(gdb) set disassembly-flavor intel
(gdb) disassemble main
Dump of assembler code for function main:
   0x000000000000091a <+0>:     push   rbp
   0x000000000000091b <+1>:     mov    rbp,rsp
   0x000000000000091e <+4>:     sub    rsp,0x10
   0x0000000000000922 <+8>:     mov    DWORD PTR [rbp-0x4],edi
   0x0000000000000925 <+11>:    mov    QWORD PTR [rbp-0x10],rsi
   0x0000000000000929 <+15>:    mov    eax,0x0
   0x000000000000092e <+20>:    call   0x8d8 <header>
   0x0000000000000933 <+25>:    mov    eax,0x0
   0x0000000000000938 <+30>:    call   0x82f <set_timer>
   0x000000000000093d <+35>:    mov    eax,0x0
   0x0000000000000942 <+40>:    call   0x87d <get_key>
   0x0000000000000947 <+45>:    mov    eax,0x0
   0x000000000000094c <+50>:    call   0x8ac <print_flag>
   0x0000000000000951 <+55>:    mov    eax,0x0
   0x0000000000000956 <+60>:    leave
   0x0000000000000957 <+61>:    ret
End of assembler dump.
(gdb) break main
Breakpoint 1 at 0x91e
(gdb) info breakpoints
Num     Type           Disp Enb Address            What
1       breakpoint     keep y   0x000000000000091e <main+4>
(gdb) run
Starting program: /home/kali/hacking/333/aaa/w/need-for-speed 
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".

Breakpoint 1, 0x000055555540091e in main ()
(gdb) disassemble main
Dump of assembler code for function main:
   0x000055555540091a <+0>:     push   rbp
   0x000055555540091b <+1>:     mov    rbp,rsp
=> 0x000055555540091e <+4>:     sub    rsp,0x10
   0x0000555555400922 <+8>:     mov    DWORD PTR [rbp-0x4],edi
   0x0000555555400925 <+11>:    mov    QWORD PTR [rbp-0x10],rsi
   0x0000555555400929 <+15>:    mov    eax,0x0
   0x000055555540092e <+20>:    call   0x5555554008d8 <header>
   0x0000555555400933 <+25>:    mov    eax,0x0
   0x0000555555400938 <+30>:    call   0x55555540082f <set_timer>
   0x000055555540093d <+35>:    mov    eax,0x0
   0x0000555555400942 <+40>:    call   0x55555540087d <get_key>
   0x0000555555400947 <+45>:    mov    eax,0x0
   0x000055555540094c <+50>:    call   0x5555554008ac <print_flag>
   0x0000555555400951 <+55>:    mov    eax,0x0
   0x0000555555400956 <+60>:    leave
   0x0000555555400957 <+61>:    ret
End of assembler dump.
(gdb) call (int) get_key()
Creating key...
Finished
$1 = 9
(gdb) call (int) print_flag
$2 = 1430259884
(gdb) call (int) print_flag()
Printing flag:
PICOCTF{Good job keeping bus #1f2ac4ec speeding along!}
$3 = 56
(gdb) 
Printing flag:
pDcBbYdvebLigKofChVdIo]~        .▒lH9In
                                       ~]hKiGcH-Qa_cV,O
$4 = 56
(gdb) q
PICOCTF{Good job keeping bus #1f2ac4ec speeding along!}


seguimos los pasos del siguiente video: https://www.youtube.com/watch?v=2LRa9WLu51c&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=57&ab_channel=hackadvisermx


```

## Bandera
Flag: PICOCTF{Good job keeping bus #1f2ac4ec speeding along!}



## Notas adicionales


## Referencias
