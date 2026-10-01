# Variables

En programación, una variable está formada por un espacio en el sistema de almacenaje y un nombre simbólico que está asociado a dicho espacio. Ese espacio contiene una cantidad de información conocida o desconocida, es decir un valor

## Tipos de datos

La mayoría de los lenguajes de programación incluyen tipos de datos a la hora de definir una variable. El tipo de datos determina que clase de valores puede almacenar una variable y definen cuanto espacio se reserva en memoria para guardar esa información. 

### Tipos de datos primitivos

Hay ciertos tipos de datos comunes a todos los lenguajes de programación.

#### Tipos numéricos
##### Entero 

Un entero es un tipo de dato numérico que representa números enteros sin componentes fraccionarios. Dependiendo del lenguaje y la arquitectura, los enteros pueden ser de diferentes tamaños: 8 bits (byte), 16 bits (short), 32 bits (int) y 64 bits (long). 

##### Punto flotante

Los tipos de datos de punto flotante representan números reales con partes fraccionarias. Se utilizan para cálculos que requieren precisión decimal. Los lenguajes suelen tener el float y el double como tipos de punto flotante.

#### Tipo de dato lógico o boolean

El tipo booleano representa valores de verdad lógicos: verdadero o falso.

#### Tipos de dato de texto
##### Tipo de dato carácter

El tipo de dato carácter representa un solo símbolo Unicode. En muchos lenguajes, los caracteres se almacenan utilizando el conjunto de caracteres ASCII o Unicode.

##### Tipo de dato cadena de caracteres

Este tipo de dato representa una frase o palabra completa. La implementación depende del lenguaje 

## Variables en Java
```
tipo identificador;
tipo identificador = valor_inicial;
```

```java
// La variable edad es de tipo entero para representar una edad en años
int edad;
```
### Tipos primitivos Java
```java
// Numéricos enteros
byte entero1Byte = 0; // -128 hasta 127
short entero2Bytes = 10; // -32768 hasta 32767:
int entero4Bytes = 0; // -2147483648 hasta 2147483647. Tipo Preferido
long entero8Bytes = 1000L; // -9223372036854775808 hasta 9223372036854775807

// Numéricos reales
float real4Bytes = 10.6f; // 6 o 7 decimales, menos precisión
double real8Bytes = 15.901d; // 16 decimales, más preciso. Tipo preferido

// Carácter
char letra = 'a'; // Se asignan con comillas simples
char otraLetra = 67; // 67 es el valor del caracter ASCII 'C'
String cadena = "Hola Mundo!"; // String en realidad no es primitivo, pero su uso es tan común que podemos considerarlo así

// Lógico
boolean esVerdad = true; // Dos posibles valores, falso y verdero 
boolean noEsVerdad = false;
```
### Operaciones
#### Asignación
Las operaciones de asignación sirven para almacenar un valor en una variable:
```java
int edad;
edad = 46; // La variable edad pasa a contener el valor 46
edad = 45; // Podemos cambiar el valor todas las veces que queremos

// También podemos asignar un valor a una variable cuando la declaramos
int mesActual = 9;
```
#### Operaciones aritméticas
Podemos realizar estas operaciones sobre variables númericas
```java
int x = 10;
int y = 100;
int z;
// Suma
z = x + y; 
// Resta
z = z - x;
// Multiplicación 
z = x * y;
// División
z = x / y;
// Módulo, se obtiene el resto
z = x % y; 
// Incremento y decremento
x++; // Es equivalente a x = x +1;
x--; // Es equivalente a x = x - 1;
++x:
--x;
```
#### Operaciones relacionales y de comparación
Podemos comparar variables entre si o con literales. Esto es crucial a la hora de construir programas donde alteremos el flujo de ejecución mediante condicionales o bucles.
```java
// Las comparaciones dan como resultado verdadero o falso, por eso nuestro resultado es booleano
boolean resultadoLogico;
int numeroPrimero = 100;
int numeroSegundo = 25;

// == ¿Son iguales?
resultadoLogico = numeroPrimero == numeroSegundo;

// != Son diferentes
resultadoLogico = numeroPrimero != numeroSegundo;

// Mayor, menor, mayor o igual y menor o igual
resultadoLogico = numeroPrimero < numeroSegundo;
resultadoLogico = numeroPrimero > numeroSegundo;
resultadoLogico = numeroPrimero <=  numeroSegundo;
resultadoLogico = numeroPrimero >= numeroSegundo;
```
#### Operadores Booleanos
Operadores Booleanos

En Java tenemos tres operadores booleanos:

* && -> Y lógico
* || -> O lógico
* ! -> Negación
```java
bool puedenTodosEntrar = false;
final int edadMinima = 18;
int edadJuan = 18;
int edadDavid = 26;
int edadSara = 17;

// Estas dos operaciones son equivalentes
// Podrán entrar si TODOS son mayores de edad 
puedenTodosEntrar = (edadJuan >= edadMinima) && (edadDavid >= edadMinima) && (edadSara >= edadMinima);
// Podrán entrar si NINGUNO es menor de edad
puedenTodosEntrar = !((edadJuan < edadMinima) || (edadDavid< edadMinima) || (edadSara < edadMinima));
```
### Casting