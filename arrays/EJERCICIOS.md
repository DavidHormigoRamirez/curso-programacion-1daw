# ContactMe

Diseña e implementa una aplicación para la gestión de una agenda de tarjetas de contacto que cumpla los siguientes requisitos:

La aplicación debe poder almacenar hasta 20 contactos. 

Cada tarjeta de contacto tiene lo siguientes datos: Nombre, apellido 1, apellido2, teléfono y email.

Si imprimimos una tarjeta debe salir así:

```
David Hormigo Ramírez
Telf: 600700800
@: dhorram948@g.educaand.es
```

## Fase 1

Debe mostrar un menú con las siguientes opciones:

* Añadir contacto. Si no ha llegado a su limite, pide los datos para crear un contacto y lo almacena en la primera posición libre
* Imprimir agenda. Imprime todos los contactos almacenados. Si la agenda esta vacia, imprime un mensaje diciendolo
* Salir. Termina el programa

## Fase 2

* Añade al menú las siguientes opciones:
* Eliminar contacto por posición. Pide una posición del 1 al 20 y elimina ese contacto.
* Limpiar agenda -> Vacía todos los contactos

## Fase 3

Añade al menú la opciones siguientes:

* Buscar contactos por apellido. Pide un apellido y busca todos los contactos que alguno de sus apellidos coincida.
* Modifica la opción de añadir para que cuando se vaya a añadir un contacto se compruebe que no existe ninguno con el mismo teléfono.

# AEMET Turing!

Desarrollar un programa en Java que gestione y analice las temperaturas diarias de un año completo utilizando una matriz (array bidimensional), aplicando generación de números aleatorios, recorridos por filas/columnas y manejo de calendarios irregulares.

## Contexto y Estructura de Datos

El programa debe utilizar una matriz de enteros o decimales (double[][]) de 12 filas (una por cada mes del año, de enero a diciembre) y 31 columnas (correspondientes a los días del mes).

Dado que no todos los meses tienen 31 días, los días que no existan en un mes concreto (por ejemplo, el 30 de febrero o el 31 de abril) deberán rellenarse con un valor centinela que indique que el día no es válido (por ejemplo, Integer.MIN_VALUE). No se tendrán en cuenta años bisiestos (febrero tendrá siempre 28 días).

## Requisitos del programa

### Generación de datos (Relleno aleatorio) 
Para que los datos sean realistas, las temperaturas de cada mes deben generarse aleatoriamente dentro de un rango basado en las temperaturas medias históricas de Málaga (en grados Celsius):

| Mes | Días | Temp. Mínima (°C) | Temp. Máxima (°C) |
| ---- | :---: | :---: | :---: |
| Enero | 31 | 7 | 17 | 
| Febrero | 28 | 8 | 18| | Marzo | 31 | 10 | 20 | 
| Abril | 30 | 11 | 21 | 
| Mayo | 31 | 14 |  24 | 
| Junio | 30 | 18 | 28 | 
| Julio | 31 | 20 | 31 | 
| Agosto | 31 | 21 | 31 | 
| Septiembre | 30 | 18 | 28 | 
| Octubre | 31 | 15 | 24 | 
| Noviembre | 30 | 11 | 20 | 
| Diciembre | 31 | 8 | 17 | 

(Sugerencia: Puedes guardar los días de cada mes y los rangos de temperaturas mínimas y máximas en arrays unidimensionales auxiliares para facilitar el relleno de la matriz).

### Menú de operaciones
 
Una vez rellena la matriz, el programa mostrará un menú interactivo en bucle hasta que el usuario decida salir, con las siguientes opciones:

1. Mostrar tabla anual: Imprimir por consola las temperaturas de todo el año organizadas por meses y días. En las posiciones no válidas (como el 31 de noviembre) se debe mostrar un guion (--) en lugar del valor centinela.

2. Temperatura media de un mes: Pedir al usuario el número de un mes (1 a 12) y calcular la temperatura media de ese mes (asegurándose de dividir solo entre los días reales de ese mes).

3. Día más caluroso y más frío del año: Buscar en toda la matriz cuál ha sido la temperatura máxima y mínima registrada, indicando exactamente en qué día y mes ocurrieron (ej. "Máxima: 31°C el 14 de agosto").

4. Días de calor extremo (Terral): Contar e indicar cuántos días del año la temperatura ha superado los 30°C.

5. Comparativa de estaciones: Calcular y mostrar la temperatura media del verano (junio, julio, agosto) frente a la del invierno (diciembre, enero, febrero).

6. Salir.

## Sistema de Gestión de Mediateca

### Descripción del problema

Una mediateca municipal necesita informatizar su gestión diaria y nos ha encargado el desarrollo de una aplicación de consola en Java que será utilizada exclusivamente por el personal bibliotecario.

El sistema debe permitir administrar el fondo documental de la mediateca, compuesto actualmente por tres tipos de obras: **libros, DVDs y vinilos**. Aunque todas las obras comparten información básica de catalogación (como su identificador, título o autor), cada formato requiere registrar sus propios datos específicos (por ejemplo, la editorial en los libros, la productora en los DVDs o la discográfica en los vinilos).

Para organizar el almacenamiento físico y lógico del catálogo en memoria, la dirección técnica exige que todas las obras se guarden en una **única matriz bidimensional** de 3 filas (una fila destinada a cada tipo de obra) y 100 columnas (capacidad máxima por tipo).

### Funcionamiento y reglas de negocio

El programa debe ofrecer un menú operativo para que el bibliotecario pueda realizar las siguientes gestiones:

* **Gestión del catálogo:** Dar de alta nuevas obras en la fila correspondiente de la matriz (controlando que no se supere el espacio disponible),consultar qué obras se encuentran actualmente prestadas, detallando toda su información.
* **Gestión de socios:** Dar de alta a nuevos usuarios y dar de baja a socios existentes (siempre que no tengan ninguna obra pendiente de devolver). También debe ser posible localizar rápidamente a un usuario buscando por su apellido.
* **Préstamos:** Registrar el préstamo de una obra disponible a un socio. De cada préstamo debe quedar constancia de qué obra se ha llevado, qué usuario la tiene y cuál es su fecha límite de devolución, que será siempre de **15 días** a partir del momento en que se realiza el préstamo. Un mismo socio nunca podrá tener más de **5 obras prestadas** simultáneamente.
* **Reservas:** Si un socio solicita una obra que ya está prestada, el sistema permitirá dejársela reservada (siempre que no haya sido reservada ya por otra persona). Un socio puede acumular un máximo de **2 reservas** activas.
* **Devoluciones y sanciones:** Cuando un socio devuelve una obra, el sistema comprobará si se entrega en plazo. En caso de retraso, se aplicará automáticamente una penalización de **3 días de sanción por cada día de demora**. Mientras un usuario esté sancionado, no podrá realizar nuevos préstamos ni reservas.

### Requisitos técnicos y entregables

1. **Diseño previo (Modelado):** Antes de escribir el código, deberás analizar el problema y diseñar la arquitectura de clases aplicando **herencia y polimorfismo**. Decide qué atributos y métodos van en cada clase, qué visibilidad tendrán y cómo se relacionarán los objetos entre sí (obras, usuarios, préstamos, reservas, etc.).
2. **Implementación en Java:** Desarrolla la aplicación respetando la restricción de la matriz de $3 \times 100$ para el catálogo. Incluye una carga inicial de datos de prueba (algunas obras de cada tipo y varios usuarios) para poder probar todas las opciones del menú nada más arrancar el programa.
3. **Robustez:** El programa debe controlar posibles errores de entrada del usuario y mostrar mensajes claros cuando una operación no se pueda llevar a cabo por incumplir alguna regla de la mediateca.