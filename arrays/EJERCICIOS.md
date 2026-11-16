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