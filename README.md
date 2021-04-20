# Trabajo Practico 0 para Taller de Programacion

## Nombre: Juan Ignacio Colombo
## Padron: 103471
## Link GitHub: https://github.com/juanicolombo97/tp0-taller/



### Paso 0

A-
Captura sin valgrind:
![Screenshot from 2021-04-19 20-06-05](https://user-images.githubusercontent.com/49823710/115314388-79063080-a14b-11eb-8c01-da95239ac9e0.png)

Captura con valgrind:

![Screenshot from 2021-04-19 20-13-10](https://user-images.githubusercontent.com/49823710/115314501-b66abe00-a14b-11eb-9dfc-31075ee14010.png)


B- Para que sirve valgrind.

Valgring es un programa utilizado para detectar fallar en el codigo como por ejemplo errores de memoria o rendimiento de un programa.
Uno de los usos mas comunes de valgrind es el memcheck o cachegrind.

C-

Que representa sizeof? cual es el valor sizeof(char) y sizeof(int)
El sizeof es una funcion que viene con c que se utiliza para obvetener el numero de bytes que posee una variable o un ttipo de dato. En el caso del int devuelve 4 bytes ya que es la cantidad de bytes que ocupa un int en memoria. Por otro lado sizeof char devolvera 1 byte ya que es lo que pesa un caracter.

D-

El sizeof de una struct en C no es igual a la suma de los sizeof de sus miembros, ya que a veces se agrega padding a los elementos de la estructura haciendo que el sizeof struct sea mas grande que el de la suma de sus elementos.

E-

En el caso de stdin es la entrada estandar del programa, por este medio el programa puede aceptar texto o archivos a leer. Por otro lado esta la salida que retorna el codigo que es atraves de stdout en la cual, vemos si anduvo el programa bien o tuvo alguna falla. Por ultimo esta el stderr que es donde van a parar los mensajes de error del programa. Para rediccionar la entrada  se utiliza el caracter <, esto permite pasarle archivos al programa a ejecutarse. Por otro lado esta el redirrecionamiento de salidas con el caracter >. Tambien podemos conectar la salida estandar de un proceso a la entrada estandar de otro mediante un pipe, que seria el caracter |.Esto permite que la salida de un proceso pueda ser la entrada de otro.


### PASO 1

A- 

![Screenshot 2021-04-19 204701](https://user-images.githubusercontent.com/49823710/115317010-ea94ad80-a150-11eb-8d07-93973c135232.png)

Misssing space before: Este error dice que no se puso un espacio despues del "(algo" en el statement del while. Tendria que ser "( algo".

Mismatching spaces inside (): Este error se genera en  (  c == EOF), ya que al ver se dejo correctamente el espacio despues del (, pero no al finalizar el statement, ya que deberia quedar, ( c == EOF ).

Should have zero or one space...: Este error se genera ya que como vemos en la porcion del codigo que genera el error "(  c == EOF)" como despues del primer parentesis se deja dos espacios en ves de uno lo cual genera el error.

An else should appear....: Este error salta porque el else de la linea 47 no esta a continuacion del } que se encuentra en la linea 46. Deberia ser } else y no } \n else.

If an else has a brace....: Este error se debe a que el else tiene un { al finalizar pero no el } al comenzar.

Extra space befor...: Esto se debe a que se deja un espacio antes de poner el ; al final una linea de codigo.

Almost always snp...: Este error se da ya que nos aconseja que no usemos strcpy sino que usemos snprintf.

B-

![Screenshot 2021-04-19 204732](https://user-images.githubusercontent.com/49823710/115320011-65f95d80-a157-11eb-9a57-68679c5f9ec3.png)

 error: unknown type name 'wordscounter_t': Este error se debe a que el compilador no puede reconocer a wordscounter_t, esto se debe a que no se incluyo el .h donde se declaran estos metodos.
 
error: implicit declaration of function: Este errror se debe a que el programa quiere llamar a un metodo que no esta declarado. Nuevamente se debe a que no se incluyo el .h.

C- 

El sistema no reporto ningun warning ya que se el error ocurrio al momento de compilar con lo cual la linkedicion no llego a hacerse, es por esto que no encontramos ningun WARNING.

### Paso 2

