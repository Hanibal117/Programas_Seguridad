
 
### Description
Can you get the flag?Go to this [website](http://saturn.picoctf.net:64710/) and see what you can discover.

## Pistas
This can be solved online if you don't want to do it by hand!




## Solución

``` 
Nos meteremos a la pagina y pondremos un usuario y password cualquiera, despues inspeccinamos elementos de la pagina, alli buscamos una archivo llamado secure.js
alli esta el user y la password:
  

function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
ya solo regresamos a la pagina para poner esos datos y con ellos la bandera



```

## Bandera
Flag: picoCTF{j5_15_7r4n5p4r3n7_b0c2c9cb}


## Notas adicionales


## Referencias
