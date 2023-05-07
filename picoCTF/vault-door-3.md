
 
#### Description

This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://jupiter.challenges.picoctf.org/static/943ea40e3f54fca6d2145fa7aadc5e09/VaultDoor3.java)

## Pistas
Make a table that contains each value of the loop variables and the corresponding buffer index that it writes to.


## Solución

``` 
Descargamos el archivo para luego acceder a firefox en consola para javascript para copiar el siguiente codigo:

var password = "jU5t_a_sna_3lpm18g947_u_4_m9r54f";
undefined
var buffer = Array(32);
undefined
for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        }
'g'
despues con: buffer.join("")
y nos da la bandera
picoCTF{U5t_a_s1mpl3_an4gr4m_4_u_79958f}
"jU5t_a_s1mpl3_an4gr4m_4_u_79958f"
```

## Bandera
Flag: picoCTF{U5t_a_s1mpl3_an4gr4m_4_u_79958f}



## Notas adicionales


## Referencias
