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

## Recorrer arrays

```java
int[] edades = {18,19,18,32,21,20,18,25};

// La manera tradicional con un bucle for
// El array comienza en el indice 0
for (int i = 0; i < edades.length; i++) {
    System.out.println("Elemento en la posición " + i + ": " + edades[i]);
}

// Otra forma es con un bucle for-each
// En este caso la variable edad va tomando el valor de cada elemento del array edades desde la primera posición hasta la última
for (int edad : edades) {
  // ...
}
```

## Arrays bidimensioaneles

Podemos declarar arrays de dos dimensiones o matrices. Tenemos que verlo que una matriz es en realidad un array de arrays: Cada elemento del primer array es un array.

```java
// Declaramos una matríz con una celda por cada dia del año:
// 12 filas
// 31 columnas
int[][] daysOfYear = new int[12][31];
// 1 fila, 1 columna (1 de enero?)
daysOfYear[0][0] = 10;


// Para recorrer una matriz lo hacemos con bucles anidados
int contador = 1;
for (int i=0;i < days.length;i++) {
  for (int j=0;j < days[i].length;j++) {
    days[i][j] = ++contador;
  }
}

```