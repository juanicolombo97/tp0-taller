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

C- Que representa sizeof? cual es el valor sizeof(char) y sizeof(int)
El sizeof es una funcion que viene con c que se utiliza para obvetener el numero de bytes que posee una variable o un ttipo de dato. En el caso del int devuelve 4 bytes ya que es la cantidad de bytes que ocupa un int en memoria. Por otro lado sizeof char devolvera 1 byte ya que es lo que pesa un caracter.

D-

El sizeof de una struct en C no es igual a la suma de los sizeof de sus miembros, ya que a veces se agrega padding a los elementos de la estructura haciendo que el sizeof struct sea mas grande que el de la suma de sus elementos.

E-

En el caso de stdin es la entrada estandar del programa, por este medio el programa puede aceptar texto o archivos a leer. Por otro lado esta la salida que retorna el codigo que es atraves de stdout en la cual, vemos si anduvo el programa bien o tuvo alguna falla. Por ultimo esta el stderr que es donde van a parar los mensajes de error del programa. Para rediccionar la entrada  se utiliza el caracter <, esto permite pasarle archivos al programa a ejecutarse. Por otro lado esta el redirrecionamiento de salidas con el caracter >. Tambien podemos conectar la salida estandar de un proceso a la entrada estandar de otro mediante un pipe, que seria el caracter |.Esto permite que la salida de un proceso pueda ser la entrada de otro.


### PASO 1
