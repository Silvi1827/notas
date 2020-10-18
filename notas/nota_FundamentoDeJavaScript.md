# Fundamentos de JavaScript
## Modulo 1. Introducción al curso
### Clase 1 *Bienvenidos al Curso de Fundamentos de JavaScript*

Nuestro profesor será Sacha Lifszyc y es desarrollador Full Stack desde hace varios años, hoy en día trabaja en Restorando un startup dedicado a hacer reservas para restaurantes.

A lo largo del curso aprenderemos las bases sólidas para dominar el lenguaje JavaScript. Veremos desde lo más básico como: variables, tipos de datos y operadores, e iremos avanzando con los condicionales y las estructuras de control. Luego veremos los conceptos relacionados con asincronismo, uno de los aspectos fundamentales de JavaScript, usando callbacks, promesas y async await. Y finalmente crearemos un juego de Simón dice en el que pondremos en práctica todo lo aprendido.

### Clase 2 *Repositorio del curso*

Bienvenidos de nuevo al curso.

En este material van a encontrar el enlace directo al repositorio que el profesor va a estar mencionando y utilizando a lo largo de todo el curso: https://github.com/platzi/FundamentosJSCurso

Están todos los archivos de los que se hará mención. En caso de que tengan alguna duda, usen el sistema de discusiones y estaremos respondiendo a la brevedad

Recuerden compartir sus proyectos con la comunidad.

¡Comencemos!

## Modulo 2. Primeros pasos en JavaScript
### Clase 3 *Variables*
A lo largo de todo el curso estaremos utilizando las siguientes herramientas:

- **Navegador:** Durante el curso se utiliza el navegador Chrome, aunque no hay preferencias y puede usar cualquiera. La razón por la se seleccionó Chrome se debe a que está disponible en todos los sistemas operativos y va a permitir que todos el mismo código, además ya incorporo mucho de las nuevas funcionales que trae el nuevo lenguaje de JavaScript.
- **Editor de texto:** Nuevamente no hay preferencias, pueden usar cualquier editor (Atom, Bloc de Nota, Sublime Text, Visual Studio Code).

**Primeros pasos**

Creamos un archivo de tipo html (que nos permitirá visualizar todo) y otro archivo de tipo javascript (que es donde trabajaremos).

Si abrimos el archivo Clase1.html en el navegador:

![src/fundamentosJavascript_1.png](src/fundamentosJavascript_1.png)

Y damos inspeccionar nos permitirá interactuar con el html:

![src/fundamentosJavascript_2.png](src/fundamentosJavascript_2.png)

Vamos a nuestro editor de texto, el archivo html creamos un esqueleto básico:

![src/fundamentosJavascript_3.png](src/fundamentosJavascript_3.png)

En el cuerpo (body) escribimos script que nos permitirá incluir o llamar nuestro código de tipo JavaScript.

**Hola mundo**

Para imprimir algo en la consola, es decir, darle un mensaje 'secreto' al usuario usamos el comando: ***console.log()***

Siempre que empezamos en un nuevo lenguaje o un framework nuevo es bueno hacer un 'hola mundo' como práctica, en JavaScript es de la siguiente manera:

***console.log('Hola mundo JS')***

Al guardar y cargar nuevamente la página html, podemos ver el resultado en la consola:

![src/fundamentosJavascript_4.png](src/fundamentosJavascript_4.png)

**Definir una variable**

Una de las manera de declarar y asignar una variable en JavaScript es la siguiente:

![src/fundamentosJavascript_5.png](src/fundamentosJavascript_5.png)

Esto nos imprimirá un 'Hola nombre'.

Otra manera también es:

![src/fundamentosJavascript_6.png](src/fundamentosJavascript_6.png)

Concatenamos el texto con el signo + (más).

Si por ejemplo deseamos concatenar dos variables y decir 'Hola nombre apellido', es:

![src/fundamentosJavascript_7.png](src/fundamentosJavascript_7.png)

- De la primera forma nos queda pegado el nombre y el apellido.
- De la segunda forma ponemos un espacio en blanco entre el nombre y el apellido.

También podemos declarar y asignar todo en una misma línea:

![src/fundamentosJavascript_8.png](src/fundamentosJavascript_8.png)

**Débilmente tipado**

JavaScript es un lenguaje débilmente tipado, es decir, no hay nada que me diga que la variable nombre tiene que ser texto y solo acepta valores de tipo string.

![src/fundamentosJavascript_9.png](src/fundamentosJavascript_9.png)

Esto nos imprimirá un 'Hola Sacha Lifszyc' y un 'Tengo 28 años'.

Pero si hacemos lo siguiente:

![src/fundamentosJavascript_10.png](src/fundamentosJavascript_10.png)

Aunque nos imprime lo mismo, podemos ver como nuestra edad empieza como un número y termina siendo un string. Esto es algo que no debemos perder de vista a la hora de desarrollar en JavaScript.

**NOTA**

- El string puede ser con comilla doble o simple, es totalmente indistinto pero por convicción el más usado es la comilla simple.
- Se puede ver que no se ha escrito el punto y coma al final de cada sentencia o línea del programa. Se podría incluir y el programa seguirá funcionando correctamente. En JavaScript el punto y coma es algo visual o una convección el si deseamos escribirlo o no, si bien hay algunos casos en donde no funciona pero son casos muy puntuales.

### Clase 4 *Variables: Strings*
### Clase 5 *Variables: Números*
### Clase 6 *Funciones*
### Clase 7 *El alcance de las funciones*
### Clase 8 *Objetos*
### Clase 9 *Desestructurar objetos*
### Clase 10 *Parámetros como referencia o como valor*
### Clase 11 *Comparaciones en JavaScript*

## Modulo 3. Estructuras de Control y Funciones
### Clase 12 **
