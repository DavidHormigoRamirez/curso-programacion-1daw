# Arrays

Hasta ahora en el curso hemos aprendido a declarar una variable que nos permite almacenar un valor en la memoria del programa. Sin embargo, hay ocasiones que necesitaremos tener una colección de valores. Una de las formas que tenemos es el uso de **arrays** o vectores: una estructura de datos que almacena elementos de forma ordenada.

## Arrays en Java

Practicamente todos los lenguajes de programación de alto nivel cuentan con este tipo de estructura y tienen ciertas diferencias. Nos centraremos en Java:
1. Los arrays en Java tienen una longitud **fija**. Cuando se inician no se puede cambiar a posteriori
2. El índice comienza en 0. Es decir el primer elemento del array esta en la posición 0. De esta manera el ultimo esta en la posición longitud - 1.
3. Tipo estricto. Los arrays en Java son **homogeneos**: todos los elementos son del mismo tipo o clase y no puede cambiar.
4. Son objetos. En realidad la variable almacena una referencia a un espacio de memoria

Veamos como trabajar con arrays:
```java
// Declaramos un array de 10 posiciones de números enteros
int[] numeros = new int[10];

// Podemos declarar un array indicando sus valores iniciales
int[] pares = {2,4,6,8,10,12,14,16,18,20};

// para Cambiar el valor de una posición accedemos por indice
numeros[0] = 25;

// Lo mismo para leerlo, se hace por índice
System.out.println(numero[0]); //
```
