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