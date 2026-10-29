#  Núermos aleatorios
**aleatorio, ria**

*Del lat. aleatorius, der. de alea 'juego de azar', 'azar, suerte'.*
1. **adj.** Que depende del azar

Hay veces que vamos a necesitar la generación de números aleatorios en nuestros programas. Esto puede ser para simular situaciones que pueden tener diferentes valores de manera imprevisible.
Para ello en **Java** contamos con varias formas de generar estos números. 

## El método Math.random

Quizas la manera más sencilla es usar el método random de la clase Math. Esté metodo genera números **reales** entre 0 (incluido) y 1 (**no incluido**). 

```java
// El numéro esta en el rango [0,1)
double aleatorio = Math.random();
```

## La clase Random
La clase **Random** nos da una manera más comoda de trabajar con aleatorios.
```java
Random rand = new Random();
int enteroAleatorio = rand.nextInt(15); // Entre 0 y 14 incluidos
double realAleatorio = rand.nextDouble(); // Entre 0 y 1
boolean booleanoAleatorio = rand.nextBoolean();
```