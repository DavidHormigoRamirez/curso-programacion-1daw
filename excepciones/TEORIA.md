# Excepciones
Hasta ahora hemos escrito nuestro programas pensando en el *happy path*, es decir, programamos pensando que todo va a ir bien. Pero esto dista mucho de lo que va a pasar en realidad: el usuario va escribir mal ese número entero que esperamos, o el fichero que queremos abrir ya esta siendo editado por otro proceso, o ese directorio donde queremos leer no existe, etc ...
Es por ello que tenemos que programar teniendo en cuenta la ley de Murphy:

> Si algo puede salir mal, saldrá mal

Pongamos el siguiente código de ejemplo:

```java
Scanner sc = new Scanner(System.in);
int entero = sc.nextInt()
```

Hemos visto que este código funciona correctamente **si y solo si** el usuario tiene la buena intención de introducir por teclado texto que se puede interpretar como un entero. ¿Pero qué ocurre cuando el usuario comete un error y mete un número real?¿o una cadena de texto?

```
Exception in thread "main" java.util.InputMismatchException
	at java.base/java.util.Scanner.throwFor(Scanner.java:947)
	at java.base/java.util.Scanner.next(Scanner.java:1602)
	at java.base/java.util.Scanner.nextInt(Scanner.java:2267)
	at java.base/java.util.Scanner.nextInt(Scanner.java:2221)
	at Main.main(Main.java:12)
```

Pues se produce un error en **tiempo de ejecución**. En Java este tipo de errores se modelan usando un tipo de clase especial llamadas *excepciones*: situaciones que no se deben producir y tenemos que manejar para evitar errores. En este caso concreto, la excepción que se ha lanzado es **java.util.InputMismatchException**, así sabemos que lo que ha ocurrido que la entrada introducida y la esperada no son la misma.

## Uso de condicionales

Para realizar este tipo de tarea podriamos intentar usar los [condicionales](../condicionales/TEORIA.md) que nos permite verificar si cierta operación es segura si se cumple ciertas condiciones. Esto, tiene como requisito que tengamos alguna manera de verificar que antes de que se ejecute el código que puede fallar se cumplen las condiciones adecuadas.

En este caso concreto, la clase Scanner tiene el método **hasNextInt** que nos devuelve **true** si lo que hay en la entrada es un texto interpretable como un entero.

```java
// El condicional evalúa si el siguiente dato es un entero SIN consumirlo todavía
if (scanner.hasNextInt()) {
	// Ahora sí lo leemos con seguridad
	int numero = scanner.nextInt(); 
    System.out.println("¡Gracias! El número es: " + numero);
} else {
	String entradaInvalida = scanner.next(); // Consumimos el texto incorrecto para limpiar el scanner
    System.out.println("Error: '" + entradaInvalida + "' no es un número entero válido.");
}

```

