# Salida por pantalla
## Herramientas básicas para desarrollo

Cualquier profesión se ejerce haciendo uso de unas herramientas propias para el trabajo. La profesión de ingeniero de software no es diferente en esto y tiene sus propias herramientas. Hay muchas y dependen de cada ingeniero, el sector donde trabaje, las tecnologías que use e incluso la empresa para la que trabaje. Las aquí indicadas son las que consideró esenciales para el desarrollo.

### Entorno Integrado de Desarrollo (IDE)

Esta herramienta consiste en una especie de editor de texto orientado al desarrollo de código. Su nombre viene por que, en principio, incluye todas las herramientas necesarias para poder programar. Existen multitud de IDEs en el mercado: algunos generales para cualquier lenguaje, otros diseñados específicamente para un lenguaje en concreto, algunos de pago, otro gratuitos ... Nosotros para programar en Java podemos usar Visual Studio Code o IntelliJ IDEA, aunque existen muchísimos más.

### Kits de Desarrollo de Sofware

Un kit de desarrollo de software (en inglés: software development kit o SDK) es generalmente un conjunto de herramientas de desarrollo de software que permite a los programadores crear una aplicación informática para un sistema concreto, por ejemplo ciertos paquetes de software, entornos de trabajo, plataformas de hardware, computadoras, videoconsolas, sistemas operativos, etcétera.

### Herramientas de Control de Versiones

Son herramientas de Software que nos permite controlar los cambios que se van produciendo en el código fuente que desarrollemos. 

## Salida por pantalla en Java
En Java contamos con la clase `System` que nos permite comunicarnos a traves de su atributo `out` con la salida estándar: es decir, nos permite escribir en un terminal.
La manera más sencilla es usar la función `print`
```java
System.out.print("Esto es lo que se va a imprimir por pantalla");
// Si además queremos que imprima e introduza un salto de linea podemos usar println
System.out.println("Esto se imprimie y además salta a la siguiente linea");
```
### Salida formateada
**Java** nos permite imprimir cadenas que son como plantillas: podemos definir un patrón con los "huecos" que queremos rellenar y Java completará el patrón:
```java
System.out.printf("La edad del profesor es %d años",46);
La edad del profesor es 46 años
```
Esta cadena acepta los siguientes "placeholders":
* %s -> Cuando queremos imprimir una cadena
* %d -> Cuando queremos imprimir un entero
* %c -> Cuando queremos imprimir un carácter
* %f -> Cuando queremos imprimir un real

Además tenemos las siguientes opciones de formato:
#### Cadenas
* %s : Imprime la cadena tal cual.
* %S: Convierte toda la cadena a mayúsculas.
* %10s: Alinea a la derecha con un ancho mínimo de 10 caracteres (añade espacios al principio).
* %-10s: Alinea a la izquierda con un ancho mínimo de 10 caracteres (añade espacios al final).
#### Enteros
* %d: Imprime el entero en base decimal de forma estándar.
* %,d: Añade el separador de miles configurado en el sistema (por ejemplo: 1,000 o 1.000).
* %05d: Rellena con ceros a la izquierda hasta alcanzar un ancho mínimo de 5 dígitos (ej. 00042).
#### Reales
* %f: Imprime el número decimal con el formato estándar (por defecto muestra 6 decimales).
* .2f: Limita el número exactamente a 2 decimales (aplica redondeo automático). Puede cambiarse el número (ej: .4f para cuatro decimales).
* %,.2f: Combina el separador de miles con el límite de 2 decimales (ej: 1,250.45).










