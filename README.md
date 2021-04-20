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

A-

Las correcciones que primero notamos son las de sintaxis, ya que vemos que al subir el codigo, cpplint no tira ningun error. Luego otro problema que soluciona es la de agregar los includes de wordcopunter, que era lo que nos rompia el compilador en el paso 1.

B-

![Screenshot 2021-04-19 214854](https://user-images.githubusercontent.com/49823710/115320902-1b78e080-a159-11eb-9956-4013086c2a7f.png)


C- 

![Screenshot 2021-04-19 215027](https://user-images.githubusercontent.com/49823710/115321014-54b15080-a159-11eb-857d-e5944e79fb88.png)
![Screenshot 2021-04-19 215036](https://user-images.githubusercontent.com/49823710/115321016-5549e700-a159-11eb-80b9-39d365d7db5d.png)


error: unknown type name 'size_t' o 'FILE': Este error se debe a que no se importo la libreria que permite utilizar size_t o FILE(stddef.h - stdio.h).


error: implicit declaration of function 'malloc': Este errir se debe a qye bi se incluyo la libreria que tiene a malloc.


### Paso 3

A-

Los cambios que se realizaron fue la importacion de las librerias que faltaban en el codigo.


B-

![Screenshot 2021-04-19 220702](https://user-images.githubusercontent.com/49823710/115322075-9b07af00-a15b-11eb-8091-c7347bc758d1.png)

undefined reference to "wordscounter_destroy": Este error se debe a que el "wordscounter_destroy" esta declarado en el .h pero no en el .c entonces cuando en el main se quiere usar este no esta definido.Es un error del compilador.


### Paso 4

A-
Los cambios realizados en esta correcion es el agregado de la definicion del wordscounter_destroy que era lo que lanzaba error en el paso anterior.

B-

![Screenshot 2021-04-19 222423](https://user-images.githubusercontent.com/49823710/115323217-14a09c80-a15e-11eb-91cb-31e33baf29ef.png)
![Screenshot 2021-04-19 222448](https://user-images.githubusercontent.com/49823710/115323219-15d1c980-a15e-11eb-8685-bc9e5f0b8ca6.png)

ERRORES:

1- 472 bytes in 1 blocks are still reachable in loss record 1 of 2 y
2-  1,505 bytes in 215 blocks are definitely lost in loss record 2 of 2

Estos errores se deben a que cuando uno pide memoria, una ves terminada de usar la misma se la debe liberar con free, al no hacer esto nos tira errores de perdida de memoria como los que vemos. Basta con solo hacer free para la memoria alocada y se arreglara el problema.

C-

![Screenshot 2021-04-19 223300](https://user-images.githubusercontent.com/49823710/115323852-3bab9e00-a15f-11eb-8ce9-95bcefd5a78d.png)


memcpy_chk: buffer overflow detected ***: Este error se debe a que se le esta asignando a la variable que va a almacenar el nombre del archivo un espacio menor al que necesita, enconcesa al querer copiar algo de mayor tamanio a una variable de menor salta el buffer overflow.

D-

El error no se solucionaria con strncpy ya que lo que hace esta funcion es copiar los caracteres hasta la cantidad que se le pasa a copiar o hasta que llegue a un valor nulo, en este caso entonces tambien abria un buffer overflow, ya que denuievo se trataria de copiar 32 caracteres en una variable que se reservo 30.

E-

Buffer Overflow: Este error se muestra cuando se trata de copiar a un buffer datos que pasan la capacidad del mismo y entonces pisan memoria adyacente a este.

Segmentation Fault: Este es un error que aparece cuando se trata de acceder a memoria que no nos pertenece. Esto puede ser cuando queremos acceder a memoria que no reservamos por ejemplo.


### Paso 5

A-

Se agregaron la variable delim_words con todos los delimitadores que existe, y a la ves el input ahora se le pasa el argv directamente y no el filepath.

B-

Las pruebas fallaron debido a que se obtuvieron distintos resultados de los esperados.

![Screenshot 2021-04-19 231048](https://user-images.githubusercontent.com/49823710/115326955-8380f400-a164-11eb-9266-e005382c0b99.png)


C-

![Screenshot from 2021-04-19 23-14-19](https://user-images.githubusercontent.com/49823710/115327284-073ae080-a165-11eb-947f-d92be59b0879.png)

Como podemos ver el ultimo caracter es 00000004, el cual si lo pasamos de hexadecimal a caracter nos da que es basura.


D-

![Screenshot from 2021-04-19 23-22-42](https://user-images.githubusercontent.com/49823710/115327940-33a32c80-a166-11eb-8be3-2cb08e4c4006.png)

Info functions: Devuelve las funciones que posee cada archivo en el programa.

List ...: Este comando imprime por defecto 10 lineas de codigo y en el caso de pasarle una variable, imprime las 10 apartir de la variable recibvida.

Break: Establece un ckeckpoint en la linea pasada como parametro.

Run: Este comando corre el programa o en este caso el txt pasado.

No se detuvo en el breakpoint debido a que al correr run se piso el mismo.


### Paso 6

A-

Las diferencias que podemos encontrar son que se cambia la constante delim_words en ves de ser un array de caracteres ahora es un string. Tambien se agrega mas validaciones al leer el caracter y compararlo con distintos valores.

B-

![Screenshot 2021-04-19 234439](https://user-images.githubusercontent.com/49823710/115329846-4e2ad500-a169-11eb-848d-de1becc69667.png)
![Screenshot 2021-04-19 234448](https://user-images.githubusercontent.com/49823710/115329849-4ec36b80-a169-11eb-8357-0800f9303485.png)


C-

![Screenshot from 2021-04-19 23-44-09](https://user-images.githubusercontent.com/49823710/115329896-600c7800-a169-11eb-9bb5-5707cb6e5be4.png)
 
Aca podemos ver como la execucion del ultimo me redirecciona la salida del programa al archivo output_single_word.txt
