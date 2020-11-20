# Curso de Programación Estructurada
## Modulo 1. Introducción
### Clase 1 *Introducción al curso*

¡Bienvenidos al curso de Programación Estructurada!

Te presentamos a la profesora de este curso: Daniela Coyotzi Borja, ella es programadora de juegos en el estudio HyperBeard, también es desarrolla certificada en Unity.

La programación estructurada es una técnica para escribir programas orientados a mejorar la claridad, calidad y tiempo de desarrollo de un programa de computadora recurriendo únicamente a subrutinas y tres estructuras básicas: secuencia, selección (if y switch) e iteración (bucles for y while).

## Modulo 2. Conceptos básicos
### Clase 2 *Set up de codeblocks y compilador*

Lo que vamos aprender antes de comenzar a programar es como hacer el set up de codeblocks y el compilador que vamos a utilizar.

Nosotros usaremos el IDE un programa llamado codeblocks. Un IDE (Integrated Development Environment, Entorno de Desarrollo Integrado o Entorno de Desarrollo Interactivo) es una aplicación informática que proporciona servicios integrales para facilitarle al desarrollador o programador el desarrollo de software.

Un compilador es un software que traduce un programa escrito en un lenguaje de programación de alto nivel (C / C ++, COBOL, etc.) en lenguaje de máquina. Un compilador generalmente genera lenguaje ensamblador primero y luego traduce el lenguaje ensamblador al lenguaje máquina. 

Code :: Blocks es un IDE multiplataforma gratuito y de código abierto que admite múltiples compiladores, incluidos GCC, Clang y Visual C ++.

Se desarrolla en C ++ usando wxWidgets como el kit de herramientas GUI.

**Instalación**

Vamos a la página de codeblocks (http://www.codeblocks.org/) y vamos a Descargar o Downloads:

![src/programacionEstructurada_1.png](src/programacionEstructurada_1.png)

Damos click en «Download the binary release» y ahí elegimos el sistema operativo que cada uno tenga:

![src/programacionEstructurada_2.png](src/programacionEstructurada_2.png)

Tenemos varias opciones, nosotros seleccionaremos «codeblocks-20.03mingw-setup.exe» porque nos descarga automáticamente todo lo que necesitemos para poder instalar codeblocks:

![src/programacionEstructurada_3.png](src/programacionEstructurada_3.png)

Una vez descargamos es simplemente una instalación estándar, damos doble click o ejecutamos como administrador el programa descargado y nos aparece una ventana:

![src/programacionEstructurada_4.png](src/programacionEstructurada_4.png)

Damos click en Next, la siguiente es la ventana de licencia en la que damos click en I Agree:

![src/programacionEstructurada_5.png](src/programacionEstructurada_5.png)

Verificamos que este palomeado todo la instalación por defecto y damos click en Next:

![src/programacionEstructurada_6.png](src/programacionEstructurada_6.png)

Nos muestra la carpeta en la que se guardara el programa, damos click en Install:

![src/programacionEstructurada_7.png](src/programacionEstructurada_7.png)

Y ya está, el programa será instalado en tu computadora o laptop.

### Clase 3 *Variables y tipos de datos (Asignación y clasificación)*

**Diseño de programas de software**

Los programas tienen una secuencia de secuencia de actividades (fases) que deben ser seguida para generar un conjunto coherente de productos.

Estas fases son:

- Análisis
- Diseño
- Programación
- Codificación
- Prueba
- Mantenimiento
- Documentación

En la fase de Análisis y Diseño nos concentramos en el concepto y diseño del programa, software, aplicación o juego estamos creando.

Las siguientes fases, Programación y Codificación, es la parte que creamos el código para el software en el que estemos trabajando. La fase de Prueba es una fase muy importante porque tenemos que probar que nuestro software funciona correctamente, es cuando compilamos el código, la programación, y vemos que funciona bien. También hacemos cambios si es necesario.

La fase de Mantenimiento cambia mucho dependiendo del tipo de programa que nosotros tengamos. Por ejemplo, en los juegos en línea pasan mucho tiempo en mantenimiento porque están constantemente expuestos a los usuarios, o los programas que tengan poco mantenimiento, programas pasan mucho tiempo en desarrollo y al momento son sacadas al público no tengan mantenimiento más allá de unos pequeños bugs.

Finalmente esta la fase de Documentación, es importante porque si estamos trabajando con otras personas necesitamos documentar nuestro trabajo para que ellos también puedan entender correctamente lo que estamos haciendo.

**¿Qué es un tipo de dato?**

Es una clasificación que el programador le da a la información almacenada para avisarle al compilador como va a ser interpretada.

Un tipo de dato es, en esencia, un espacio en memoria con restricciones.

**Tipos de datos primitivos**

- **Numérico:** Este tipo de datos se divide en enteros y reales.

  - **int:** Son los números enteros, es decir, aquellos que no tienen fracciones o decimales. Pueden ser negativos o positivos y el rango puede variar de un compilador a otro. Se almacenan internamente en 2 o 4 bytes de memoria y pueden ser: unsigned int, short int, int, unsigned long o long (cada uno de estos datos puede almacenar un rango diferente de valores). Cuando el rango de los tipos básicos no es suficientemente grande para sus necesidades, se consideran tipos enteros largos. Ambos tipos long requieren 4 bytes de memoria (32 bits) de almacenamiento.

  Algunos ejemplos de números enteros pueden ser: 3, 27, -18, 0

	- **float / double:** Son los números reales o de coma flotante. Los tipos de datos flotantes contienen una coma (un punto) decimal, pueden ser positivos y negativos formando el subconjunto de los números reales. Para representar números muy pequeños o muy grandes se emplea la notación de punto flotante, que es una generalización de la notación científica. El lenguaje C soporta tres formatos de coma flotante; el tipo float requiere 4 bytes de memoria, double 8 bytes, y long double 10 bytes.

  Algunos ejemplos de números flotantes o dobles pueden ser: 3.14, -0.01, 1.8, 0.27

- **Caracteres:** El almacenamiento de caracteres en el interior de la computadora se hace en “palabras” de 8 bits (1 byte). Este tipo representa valores enteros en el rango 2128 a 1127. El lenguaje C proporciona el tipo unsigned char para representar valores de 0 a 255 y así representar todos los caracteres ASCII.

  Una característica de la parte estándar del conjunto de caracteres (los 128 primeros) es que contiene las letras mayúsculas, las minúsculas y los dígitos, y que cada uno de estos tres subconjuntos está ordenado en su forma natural, por lo que podemos manejar rangos de caracteres bien definidos. Los caracteres se almacenan internamente como números y por lo tanto se pueden realizar operaciones aritméticas con datos tipo char. Existe también el dato tipo cadena (compuesto), que es una sucesión de caracteres que se encuentran delimitados por comillas; la longitud de una cadena es el número de caracteres comprendidos entre los  delimitadores "[long_cad]".

  - **char:** Una variable tipo char se representa como un solo carácter encerrado entre comillas simples.

  Algunos ejemplos son: 'P', 'L', 'A', 'T', 'Z', 'I'

- **Booleanos:** Hay lenguajes que sólo pueden tomar uno de dos valores: verdadero (true) o falso ( false ). En lenguaje C no existe el tipo lógico pero se puede implementar con un número entero, 0 es falso y cualquier número diferente de cero es verdadero. Algunos compiladores utilizan el bool.

  - **bool:** Tipo de dato que representa algo que puede ser verdadero o falso.

**¿Qué es una variable?**

Es un espacio reservado en memoria, definido por un tipo de dato y un nombre asignado, en el cual se puede guardar un valor y se puede modificar.

**Declaración y asignación de una variable en C**

![src/programacionEstructurada_8.png](src/programacionEstructurada_8.png)

Para declarar una variable es necesario poner el tipo de dato que deseamos, seguido de su nombre. En este ejemplo, nuestro tipo de dato es un entero (int) de nombre healthpoints.

Para asignarle un valor es necesario el nombre de la variable (healthpoints) seguido del operador de asignación (=) y el valor que le daremos (100)

***NOTA: No debemos confundir el operador de asignación (=) con el de comparación (==).***

**Inicialización de una variable**

![src/programacionEstructurada_9.png](src/programacionEstructurada_9.png)

Para inicializar una variable ponemos primero el tipo de dato (int), el nombre (healthpoints) y el valor que deseamos (100).

**Diferencias entre inicializar y declarar**

Cuando declaramos una variable no le asignamos un valor inicial, en cambio cuando inicializamos una variables nosotros la estamos declarando y dándole un valor inicial.

**Usar codeblocks**

Para crear nuestro primer proyecto en codeblocks hacemos lo siguiente. Vamos en la pestaña de 'File', luego a 'New' y finalmente 'Project':

![src/programacionEstructurada_10.png](src/programacionEstructurada_10.png)

Se nos abrirá una nueva ventana en la que elegiremos 'Console application' y damos click en 'Go':

![src/programacionEstructurada_11.png](src/programacionEstructurada_11.png)

Damos click en 'Next':

![src/programacionEstructurada_12.png](src/programacionEstructurada_12.png)

Elegimos C y después damos click en 'Next':

![src/programacionEstructurada_13.png](src/programacionEstructurada_13.png)

Le ponemos un nombre a nuestro proyecto, en 'Folder to create project in' podemos elegir donde deseamos guardar nuestro proyecto, y finalmente damos click en 'Next':

![src/programacionEstructurada_14.png](src/programacionEstructurada_14.png)

Y finalmente damos click en 'Finish':

![src/programacionEstructurada_15.png](src/programacionEstructurada_15.png)

Ahora ya podemos trabajar en codeblocks, creando lo que deseemos en lenguaje C (o C++ si es lo que elegiste):

![src/programacionEstructurada_16.png](src/programacionEstructurada_16.png)

### Clase 4 *Entrada y salida de datos*
### Clase 5 *Operadores aritméticos*
### Clase 6 *Operadores de asignación, de incremento y decremento*
### Clase 7 *Recapitulación: Conceptos Básicos*
