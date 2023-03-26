
#### Description

There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 22342`, but it doesn't speak English...

## Pistas

You can practice using netcat with this picoGym problem: [what's a netcat?](https://play.picoctf.org/practice/challenge/34)

You can practice reading and writing ASCII with this picoGym problem: [Let's Warm Up](https://play.picoctf.org/practice/challenge/22)

## Solución

``` 
ingrese al nc dado para que me diera los siguientes numeros:
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
53 
102 
98 
53 
101 
53 
49 
100 
125 
10 

despues los puse en la siguiente pagina para hacer la conversion: https://gchq.github.io/CyberChef/#recipe=From_Decimal('Line%20feed',false)&input=MTEyIA0KMTA1IA0KOTkgDQoxMTEgDQo2NyANCjg0IA0KNzAgDQoxMjMgDQoxMDMgDQo0OCANCjQ4IA0KMTAwIA0KOTUgDQoxMDcgDQo0OSANCjExNiANCjExNiANCjEyMSANCjMzIA0KOTUgDQoxMTAgDQo0OSANCjk5IA0KNTEgDQo5NSANCjEwNyANCjQ5IA0KMTE2IA0KMTE2IA0KMTIxIA0KMzMgDQo5NSANCjUzIA0KMTAyIA0KOTggDQo1MyANCjEwMSANCjUzIA0KNDkgDQoxMDAgDQoxMjUgDQoxMCA

## Bandera
Flag: picoCTF{g00d_k1tty!_n1c3_k1tty!_5fb5e51d}



## Notas adicionales




## Referencias
https://gchq.github.io/CyberChef/#recipe=From_Decimal('Line%20feed',false)&input=MTEyIA0KMTA1IA0KOTkgDQoxMTEgDQo2NyANCjg0IA0KNzAgDQoxMjMgDQoxMDMgDQo0OCANCjQ4IA0KMTAwIA0KOTUgDQoxMDcgDQo0OSANCjExNiANCjExNiANCjEyMSANCjMzIA0KOTUgDQoxMTAgDQo0OSANCjk5IA0KNTEgDQo5NSANCjEwNyANCjQ5IA0KMTE2IA0KMTE2IA0KMTIxIA0KMzMgDQo5NSANCjUzIA0KMTAyIA0KOTggDQo1MyANCjEwMSANCjUzIA0KNDkgDQoxMDAgDQoxMjUgDQoxMCA