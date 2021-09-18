# Curso de Kotlin desde Cero
## Modulo 1. Introducción a Kotlin
### Clase 1 *Introducción al Curso de Kotlin*

¡Te damos la bienvenida al Curso de Kotlin desde Cero!

Nuestro profesor será **Giuseppe Vetri**, es un desarrollador Android con más de cuatro años de experiencia que gusta de Kotlin que le encanta la sintaxis y le gusta como lo puede utilizar para desarrollar aplicaciones o para escribir código, pero Kotlin no es solo para eso.

En este curso aprenderemos a cómo utilizar Kotlin para luego aplicarlo para desarrollar aplicaciones en backend, desarrollar aplicaciones Android y desarrollar aplicaciones multiplataforma. Este curso será la base para que podamos crear cosas increíbles con Kotlin.

### Clase 2 *Qué es Kotlin*

En esta clase hablaremos sobre que es Kotlin, como funciona y quien lo creo.

**Kotlin es desarrollado por JetBrains**

JetBrains es una compañía que se encarga de crear entornos de desarrollos como AppCode, WebStorm, IntelliJ IDEA, entre otros. Y es el entorno IntelliJ IDEA del cual se basaron para crear Android Studio, el entorno de desarrollo utilizado para crear aplicaciones en Android reemplazando a Eclipse como el IDE oficial.

**Nacimiento de Kotlin**

Kotlin nació en el 2010. Aunque no es tan viejo como Java es bastante robusto, amado por la comunidad y es la base del desarrollo Android hoy en día, pero no solo es utilizado para las aplicaciones Android.

Kotlin es usado en:

- **Backend Development:** Con frameworks como Spring, Micronaut o Ktor, para crear aplicaciones.
- **De forma nativa:** Se compila el código en una versión nativa, se crean ejecutables para Windows, Mac o Linux que después pueden ser corridos e instalados como una aplicación de escritorio.
- **Scripts:** Digamos que tenemos un código que se ejecuta varias veces y no queremos estar repitiendo este proceso manualmente, lo que podemos hacer es crear un script con Kotlin que automatice ese proceso.
- **Multiplataforma:** La versión multiplataforma no se enfoca en tener una UI igual para ambas plataformas, lo que hace es compilar el código en una librería y esa librería queda nativa para Android y iOS, se importa y tienes el mismo código en ambas plataformas.

**Surgimiento de Kotlin**

Kotlin surge de la necesidad de los programadores de JetBrains que buscaban reemplazar Java en los proyectos Android pues no siempre podían tener la última versión, lo cual los de dejaba un poco rezagados. Fue creado con la base de que fuese un lenguaje con las características de Scala, pero sin la penalización del tiempo de compilación de éste.

La interoperabilidad de Kotlin nos permite utilizar un poco de Java y un poco de Android, e ir migrando poco a poco hasta que nuestro proyecto sea completamente de Kotlin. Esto genera una gran adopción de Android porque nadie quería migrar toda su aplicación a un nuevo lenguaje de golpe o empezar de cero, sin embargo, Kotlin nos permite hacerlo poco a poco hasta el punto que quisiéramos y eso lo ha hecho un lenguaje muy popular entre los desarrolladores.

### Clase 3 *Qué es la Java Virtual Machine*

**¿Qué es una Java Virtual Machine?**

Una virtual machine es una virtualización o simulación de un sistema operativo o de los procesos que ocurren dentro de este. En nuestro caso, la Java Virtual Machine pertenece al segundo tipo y se encarga de simular los procesos que ocurren dentro de un sistema operativo. A este tipo de máquinas virtuales se les llama Process Virtual Machines.

**¿Qué ventaja nos da?**

Nos ayuda a manejar los punteros y las referencias de memoria que en otros tipos de lenguaje como C o C++ hay que manejar manualmente. Para esto se utiliza un proceso llamado garbage collection. Este proceso se encarga de revisar qué referencia de memoria no se está utilizando para eliminarla y así reducir la cantidad memoria que puede consumir un programa.

**¿Cómo funciona la JVM?**

La JVM funciona como un punto medio entre el código que nosotros escribimos y lo que entiende el sistema operativo del ordenador. Dependiendo del sistema operativo que uses puede variar. La JVM nos ayuda a que nuestro código se ejecute en Linux, Windows y MacOS. Nuestro código es convertido por la JVM a un lenguaje que puede entender el sistema operativo llamado Java Bytecode.

En palabras más simples, nosotros ingresamos código de Kotlin y se transforma en Bytecode. Este proceso puede ocurrir con otros lenguajes como Java, esto hace que nuestro código de Kotlin pueda ser utilizado desde Java y el código de Java pueda ser utilizado en Kotlin.

## Modulo 2. Configuración del entorno
### Clase 4 *Instalación de IntelliJ*

Es momento de crear un entorno de desarrollo en Windows. Para eso vamos al sitio oficial de [IntelliJ IDEA](https://www.jetbrains.com/idea/download/#section=windows "IntelliJ IDEA").

![src/javaSE_7.png](src/javaSE_7.png)

Como podemos ver tenemos las dos versiones. Ultimate es la versión de paga, mientras que la versión gratis y la cual descargaremos es la Community. Damos click en Download para que comience la descarga.

**Instalación de IntelliJ IDEA**

Vamos a la carpeta donde esta descargada el instalador, damos click derecho y "Ejecutar como administrador", o simplemente doble click sobre el archivo de instalación, después nos aparece una ventana que nos pide permiso para que la aplicación realice cambios en la computadora:

![src/javaSE_9.png](src/javaSE_9.png)

Aceptamos y nos aparece la ventana de instalación, damos click en Next:

![src/javaSE_10.png](src/javaSE_10.png)

Nos aparece el directorio donde se instalara el programa, damos click en Next nuevamente:

![src/javaSE_11.png](src/javaSE_11.png)

Usaremos la opción por defecto, así que Next:

![src/javaSE_12.png](src/javaSE_12.png)

Damos click en Install:

![src/javaSE_13.png](src/javaSE_13.png)

Y ya comienza la instalación:

![src/javaSE_14.png](src/javaSE_14.png)

Al terminar la instalación damos simplemente click en Finish:

![src/javaSE_15.png](src/javaSE_15.png)

**Utilizando IntelliJ IDEA**

Cuando ejecutamos el programa nos parece la licencia de JetBrains, aceptamos y damos click en Continue:

![src/javaSE_22.png](src/javaSE_22.png)

Después nos pregunta si queremos compartir datos, esto ya depende de cada persona en mi caso le doy a Don't Send para no compartir:

![src/javaSE_23.png](src/javaSE_23.png)

Una vez hecho todo eso, IntelliJ IDEA nos dará la bienvenida:

![src/javaSE_24.png](src/javaSE_24.png)

¿Qué significan los botones del costado?

- **Projects:** Podemos empezar un nuevo proyecto, abrir uno u obtener desde VCS que es un sistema de control de versiones.
- **Costume:** Aquí podemos realizar cambios en la apariencia, elegir un tema Light o Darcula dependiendo de los gusto, cambiar el tamaño de fuente y demás.
- **Plugins:** Los complementos que podemos instalar para ampliar nuestra funciones.
- **Learn IntelliJ IDEA:** Para aprender más sobre el programa.

**Creando proyecto con IntelliJ IDEA**

Ya podríamos crear nuestro primer proyecto con IntelliJ IDEA. Para eso damos click en New Project:

![src/javaSE_25.png](src/javaSE_25.png)

Seleccionaremos nuestra SDK, para eso en la parte superior donde dice Project SDK, abrimos y elegimos la versión del JDK:

![src/javaSE_26.png](src/javaSE_26.png)

Podemos ir en Add JDK para agregar una nueva versión:

![src/javaSE_27.png](src/javaSE_27.png)

Y al finalizar, ya tenemos completamente instalado nuestro entorno de desarrollo para comenzar a trabajar.

### Clase 5 *Instalación de IntelliJ en Linux*

La instalación de IntelliJ Idea Community en Linux es muy similar a la que hicimos en Windows, podemos descargar el programa directamente desde su [sitio web](https://www.jetbrains.com/es-es/idea/download/#section=linux "sitio web"), seleccionando la opción Descargar debajo del título de Community.

![src/kotlinCero_1.png](src/kotlinCero_1.png)

Después tenemos que extraer los archivos que se encuentran comprimidos dentro del archivo **.tar.gz**. Una vez descomprimidos, debemos buscar la carpeta bin, dentro habrá un archivo llamado **idea.sh**, el cual tendremos que ejecutar desde una terminal usando el comando **./idea**. Por último tendrás que crear los accesos directos manualmente dependiendo de la distribución de Linux que utilices.

Otra alternativa, y la que se recomienda, es descargar la **Toolbox App** de Jetbrains ya que esta gestionará las versiones que tengas instaladas, y también te ayudará a que tus iconos siempre estén funcionando de la manera adecuada. Al final es importante tener una linda estética en tu sistema operativo Linux, ¿no lo crees?

Esta la puedes descargar desde el [sitio web de Jetbrains](https://www.jetbrains.com/es-es/toolbox-app "sitio web de Jetbrains"), una vez que la descargues y ejecutes solo tendrás que seleccionar qué entorno de desarrollo quieres instalar. A menos que tengas una licencia de IntelliJ IDEA la opción que debes seleccionar es la de Community, ya que es la versión gratuita.

### Clase 6 *Kotlin con Visual Studio Code*

Aunque en este curso vayamos a trabajar con IntelliJ, ya que es el standard en la industria para trabajar con Kotlin, puede que si estás empezando a programar no tengas todavía un ordenador lo suficientemente potente para ejecutar IntelliJ o simplemente prefieras usar Visual Studio Code.

En esta guía podrás configurar tu Visual Studio Code para utilizar Kotlin.

**Descargar Visual Studio Code**

Para utilizar Visual Studio Code debes ir al siguiente enlace y descargar la versión dependiendo de tu sistema operativo: [Download Visual Studio Code](https://code.visualstudio.com/Download "Download Visual Studio Code") - Mac, Linux, Windows.

**Instalar el plugin de Kotlin y Code Runner**

Ahora que ya has descargado Visual Studio Code, tendrás que instalar el plugin de Kotlin y Code Runner para esto tienes que ir al marketplace y descargarlos.

- [Enlace del Marketplace](https://marketplace.visualstudio.com/items?itemName=mathiasfrohlich.Kotlin "Enlace del Marketplace") de visual studio code.
- [Enlace del Marketplace](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner "Enlace del Marketplace") de visual studio code para instalar el code runner

Ahora puedes hacer clic derecho y ejecutar el código o presionar el botón de play en la esquina superior derecha.

Aquí te dejo un ejemplo de cómo se vería:
![src/kotlinCero_2.png](src/kotlinCero_2.png)

## Modulo 3. Hola mundo Kotlin
### Clase 7 *Hola mundo con Kotlin*

Ya tenemos instalado nuestro entorno de desarrollo y creamos nuestro primer proyecto, ahora veremos a profundidad que funcionalidad tiene cada archivo.

En el lado izquierdo tenemos todas las carpetas y archivos del proyecto:

![src/kotlinCero_3.png](src/kotlinCero_3.png)

- **.idea:** Contiene los archivos de configuración específicos del proyecto. Estos incluyen detalles del proyecto, mapeo VCS y configuraciones de ejecución y depuración, así como detalles del usuario, archivos abiertos actualmente, historial de navegación y configuración seleccionada actualmente. Algunos archivos pueden estar comprometidos con el control de código fuente, otros pueden excluirse.
- **out:** Contiene el resultado del proyecto después de ser compilado.
- **src:** Es la carpeta más importante. Contiene todo el código de nuestro proyecto.
	
    - **main.kt:** Es el archivo que contiene el código fuente escrito en Kotlin. El nombre ***main*** nos señala que es el punto por donde comienza a ser ejecutado el proyecto, y la extensión ***.kt*** que es un archivo de Kotlin.

- **MiPrimerProyecto.iml:** Es el módulo del proyecto. Un módulo se crea automáticamente junto con el proyecto, y nos permite combinar tecnologías y marcos en una aplicación.
- **External Libraries:** Son la colección de código externo que podemos agregar a nuestro proyecto. El proyecto le hace referencia, tal que no "pueda vivir sin él", pero no es "solo parte de este" proyecto.
- **Scratches and Consoles:** Son herramientas básicas que brinda una interacción más cómoda con el código fuente para el usuario. Los scratches son archivos que no están adjuntos a una fuente de datos especificas (como archivos temporales o un borrador del código fuera del contexto del proyecto). Consoles son archivos SQL ejecutables que se adjuntan a una fuente de datos especifica (como archivos que puedan ejecutar y compilar sentencias SQL).

**Método main**

![src/kotlinCero_4.png](src/kotlinCero_4.png)

- **fun:** Es la palabra reservada para declarar una función en Kotlin.
- **main:** Nombre de la función. La función Main sirve como punto de partida para la ejecución del programa.
- **(args: Array<String>):** Son los parámetros que reciben la función.
- **println:** Una variante de print que nos ayuda a imprimir un mensaje en pantalla. A diferencia de print, println ejecuta un salto de línea al final del mensaje.
- **"Hola mundo":** Es el mensaje que imprimiremos. Para declarar una cadena se utiliza comillas dobles, no se pueden declarar con las comillas simples.

### Clase 8 *Variables en Kotlin*

Todos los tipos de lenguajes de programación tienen las variables y Kotlin no es la opción. Una **variable** no es más que un espacio de memoria en el que podemos guardar información. Dependiendo del tipo de información disponemos de diferentes variables, lo que nos permitirá evitar problemas como por ejemplo intentar sumar un número con una letra, ya que al ser tipos de variables diferentes no nos lo permitirá.

**Variables mutables e inmutables**

Kotlin utiliza dos palabras clave diferentes para declarar variables: **val** y **var**.

- La palabra reservada ***«val»*** es para una variable cuyo valor no cambia nunca. No puedes volver a asignar un valor a una variable que se declaró mediante val.
- Utilizamos ***«var»*** para una variable cuyo valor puede cambiar.

La decisión de usar **var** o **val** depende del uso que queramos darle, pero resumiendo podríamos decir que si es para almacenar un valor único y garantizamos que no se modificaran debemos usar **val**. En cambio, si es una variable cuyo valor cambiara tantas veces como queramos utilizamos **var**.

**Declarar una variable**

Cuando declaramos una variable en Kotlin lo hacemos del siguiente modo:

![src/kotlinCero_5.png](src/kotlinCero_5.png)

En donde la palabra reservada **«var»** nos dice que es una variable mutable y **«dinero»** es el nombre de la variable. Para indicar el tipo de variable lo hacemos con dos puntos seguido del tipoVariable (en este caso, nuestra variables es del tipo **Int** indica que es del tipo numérico entero). Le asignamos el valor con el operador asignar (=) seguido del valor que tendrá nuestra variable (en este caso, la variable dinero tiene asignado el valor 10).

También podemos acortar nuestro código si lo escribimos de la siguiente forma:

![src/kotlinCero_6.png](src/kotlinCero_6.png)

Sigue siendo válido, incluso sin especificar el tipo de variable, esto se debe a que Kotlin es inteligente y puede inferir automáticamente el tipo. Esto nos permite tener un código más pequeño y legible a la hora de desarrollar software, aunque al final depende de nosotros y la convención que tengamos a la hora de escribir.

Del mismo modo, también podemos declarar una variable inmutable:

![src/kotlinCero_7.png](src/kotlinCero_7.png)

**Cambio de valor a la variable**

![src/kotlinCero_8.png](src/kotlinCero_8.png)

El valor asignado a nuestra variable **dinero** es de 10, pero si queremos cambiarlo lo que hacemos es escribir nuevamente el nombre de la variable seguido del operador asignar y el nuevo valor. En este caso, nuestra variable dinero pasa de tener 10 a 5.

Para verificar que asignamos correctamente los valores, podemos imprimirlos en pantalla con **println()**.

Esto obviamente no puede ser hecho con una variable de tipo val ya que es una variable inmutable, es decir, que no cambia de valor. En el caso de que intentemos modificar su valor, Kotlin nos indicara el error:

![src/kotlinCero_9.png](src/kotlinCero_9.png)

Y nos indicara que podemos cambiar el tipo de variable de **val** a **var**.

Del mismo modo, también podemos imprimir en pantalla el valor de las variables de tipo **val** mediante **println()**:

![src/kotlinCero_10.png](src/kotlinCero_10.png)

**Constante**

Una variante de las variables de solo lectura son las constantes. Una **constante** no puede cambiar durante la ejecución del programa (lo mismo hacen los valores), pero aparte de ello, su asignación debe ser constante. Además, solo puede ser declarada dentro de un objeto o en la parte superior de una función.

Para declarar una constante utilizamos ***const val***:

![src/kotlinCero_11.png](src/kotlinCero_11.png)

***NOTA: Las val y const son datos que se utilizaremos para definir valores unchangeables, pero esto es interesante y es porque son usadas en diferentes casos. En el caso de const, el valor se determina en tiempo de compilación, y en el caso de val, el valor se determina en tiempo de ejecución. En este caso vemos los elementos y en qué momento se le asigna un dato (en el caso de const es asignada cuando el programa se está compilado y en el caso de val es asignada cuando el programa ya fue ejecutado).***

### Clase 9 *Kotlin y sus tipos de variables*

En la clase anterior aprendimos a declarar variables y modificar su valor, ahora veremos qué tipos de variable. En Kotlin, el tipo de la variable se especifica después del nombre de la variable y es precedido de «**:**», los tipos básicos que tenemos son:

- **Numéricos:** Estas variables se usan para asignar números, calcular tamaños y realizar operaciones matemáticas entre otras. Dentro de ellas se dividen en dos grupos, las variables *enteras* y *reales*.
  
	- **Byte:** Es la más pequeña entre las variables numéricos, soporta solo un rango de -128 a 127.
	- **Short:** Soporta un rango mayor a Byte, pero menor a Int. Su rango va de -32,768 a 32,767.
	- **Int:** Es la más básica que usaremos, en la cual podremos insertar números naturales, pero hay una limitación. Con una variable de tipo Int no podemos pasar de -2,147,483,647 a 2,147,483,647. Este será el número máximo y mínimo que soportará.
    - **Long:** Básicamente es igual que Int, a diferencia de que soporta un rango mayor de números, de -9,223,372,036,854,775,807 a 9,223,372,036,854,775,807.
    - **Double:** Muy similar a float pero soporta hasta 14 decimales, pero también ocupa más memoria así que para un código óptimo deberemos pensar que tipo será el que más se adapte a nuestro proyecto.  Tampoco habrá que añadir ningún tipo de letra al final del valor.
    - **Float:** Llegamos a las variables reales. A diferencia de las anteriores, estas pueden almacenar decimales. Float soporta hasta 6 decimales, pero también puede trabajar con números enteros. Esta variable cambia un poco respecto a las demás, pues habrá que meter una «f» al final del valor.
	
	![src/kotlinCero_12.png](src/kotlinCero_12.png)

- **Alfanuméricos:** Aunque los números sean muy útiles, hay veces que necesitaremos guardar cadenas de texto, o una mezcla de caracteres. Para ello tenemos las variables alfanuméricas.

	- **Char:** La variable Char nos permitirá guardar un carácter de cualquier tipo, lo único que debemos tener en cuenta es que va entre comillas simples.
	- **String:** La variable String será la que más usemos como norma general, nos permite almacenar cualquier tipo de caracteres pero a diferencia del Char, podemos añadir la cantidad que queramos. Para ser exactos, una String no es más que una cadena de Char. Las cadenas deberán ir entre comillas dobles.
	
    ![src/kotlinCero_13.png](src/kotlinCero_13.png)
	
- **Booleanas:** Son variables que solo pueden ser verdaderas o falsas (true o false). Su uso es muy amplio, cuando trabajemos con las condiciones veremos más a fondo este tema. Para asignar un valor basta con añadir true o false sin comillas.

    ![src/kotlinCero_14.png](src/kotlinCero_14.png)

**Concatenar cadenas de Textos**
Nosotros podemos combinar cadenas (string) de varios valores en uno solo. La forma más sencilla es usando el operador de adición (+) como herramienta de concatenación. Sin embargo, esto puede generar problemas cuando es necesario el espacio, pues debemos estar concatenando un string vacío (" ") para que las cadenas no estén pegadas.

Otra forma de concatenar es usando la interpolación de cadenas, también conocidas como la sintaxis de plantillas de Strings (String Templates). La interpolación te permite concatenar literales junto a fragmentos de expresiones antecedidas por el símbolo '$'. Hay dos formas de hacerlo:

- $id, donde id es un identificador simple
- ${e}, donde e es una expresión valida en Kotlin

    ![src/kotlinCero_15.png](src/kotlinCero_15.png)

**En Kotlin todo es un objeto**

Un ***objeto*** es un espacio en memoria más complejo que una simple variable. En el caso del objeto se compone de variables e incluso otros objetos, pero principalmente se compondrá de acciones, métodos y funcionalidades.

En Kotlin todo será un objeto, o al menos trataremos todos nuestros datos como uno, evitando los tipos de datos simples o sencillos (tipos primitivos). Nosotros tendremos dos tipos de datos (primitivos y objetos) y, aunque nosotros SI podremos declarar una variable, debemos evitar hacerlo. Son este tipo de cosas que podemos, pero no debemos de haber. Debemos procurar en tratar a los datos como si fueran objetos, y una característica que tiene Kotlin es que utiliza **wrappers** para los números y esto es llamado **boxing**.

Kotlin tiene características bastantes interesantes, como el hecho de no ser necesario poner punto y coma (;), incluso si lo ponemos el IDE nos señala que es algo redundante. Otra cosa interesante es que no necesitamos estar guardando los cambios, esto es porque ya automáticamente se están guardando.

Una característica para manejar los datos es que, si nosotros ponemos nuestra variable seguida del operador punto, Kotlin nos enseña una serie de métodos:

![src/kotlinCero_16.png](src/kotlinCero_16.png)

Esto es la clave donde, en ese momento, la variable está siendo tratada como objeto. Recordemos los objetos tendrán métodos y atributos, y las variables no.

Si nosotros quisiéramos poner un número seguido del operador punto:

![src/kotlinCero_17.png](src/kotlinCero_17.png)

Nos saldrán expresiones que pueden ser ejecutadas como convertir el número en un array o un list, pero no son métodos.

Entonces, para manejar nuestras operaciones, lo haremos del siguiente modo:

![src/kotlinCero_18.png](src/kotlinCero_18.png)

Tenemos **plus** para sumar, **minus** para restar, **times** para multiplicar y **div** para dividir. Y si queremos imprimir estas operaciones, solo es necesario encerrarlos dentro de un println. De esta forma es como nosotros ejecutamos las mismas operaciones del inicio, pero esta vez tratando los datos como objetos.

Y si observamos nuestro código, creamos directamente las variables, no las instanciamodefinimos para convertirlas en objetos, sino que Kotlin automáticamente ya lo asume como uno.

Entonces, tratas las variables es más conveniente y esto porque las sumas o métodos que están definidas en los objetos (esas variables que nosotros declaramos y Kotlin trata como objetos) están mucho más optimizadas, mejor organizadas en nuestro código, para manejar hilos, rutinas u operaciones en paralelo. Este tipo de operaciones que están definidas en los objetos es más adecuado utilizarlas porque nos permite preparar nuestro código para programación más robusta, concurrente, que sea a base de errores, etc.

### Clase 10 *Modificadores y tipos de datos en Kotlin*

Un **tipo de datos** es la propiedad de una variable que determina su dominio (qué valores puede tomar), qué operaciones se le pueden aplicar y cómo es representado internamente por el computador. Pueden ser ***números enteros***, ***cadenas de texto*** o ***booleanos***, y estos tres tipos de datos comparten algo en común; son datos ***primitivos***.

Los **tipos de datos primitivos** son asignaciones de memoria predefinidas para almacenar un dato, tales asignaciones de memoria son similares en los diversos lenguajes de programación, tanto para Java como Kotlin, y casi siempre lo único que los diferencia entre un lenguaje de programación y otro es su sintaxis, aunque en forma interna se manejan la misma cantidad de bits de memoria, así como su gestión de ésta. Con los tipos de datos primitivos nosotros somos capaces de crear ***objetos***.

**Todo es un objeto en Kotlin**

Como sabemos, un **objeto** es un espacio en memoria más complejo compuesto de variables e incluso otros objetos.

En Kotlin trataremos todos nuestros datos como un objeto, evitando los tipos de datos primitivos. Esto nos permitirá tener ventajas como un código más corto, conciso y directo, sin necesidad de estar repitiendo código constantemente. También podemos sobrescribir operadores como la suma para sumar dos objetos del mismo tipo.

**Retrocompatibilidad con Java**

Kotlin es compatible con todos los frameworks Java, teniendo soporte concreto en alguno de ellos como Spring tanto por parte del framework como con plugins específicos en IntelliJ. Es lo suficientemente para convertir el código de Kotlin a bytecode, esto es lo que permite que la migración de una aplicación Java existente a Kotlin se puede realizar de manera gradual, desarrollando el código nuevo, o cambiando gradualmente partes del código en Kotlin mientras se mantiene el código antiguo Java.

### Clase 11 *Operaciones con los tipos de datos en Kotlin*
Operaciones con los tipos de datos en Kotlin
En Kotlin las operaciones son traducidas a funciones interiormente por el compilador. La operación **val tercerValor = primerValor + segundoValor** es lo mismo que decir **tercerValor = primerValor.plus(segundoValor)**.

En la siguiente tabla te voy a dejar las operaciones que vas a poder realizar con los distintos tipos de datos y si te encuentras con alguno que no permita realizar esa operación puedes crearla por tu cuenta. Recuerda que Kotlin te permite extender el lenguaje para aprovechar estas funcionalidades.

**Operaciones más utilizadas**

![src/kotlinCero_19.png](src/kotlinCero_19.png)

Dependiendo del tipo de dato que tengas podrás utilizar todos o solamente algunas de estas operaciones, por ejemplo si tienes una variable del tipo de dato String no vas a poder dividirla, a menos que tú crees esa función. Sin embargo, sí vas a poder sumar dos variables del tipo de dato String para obtener el valor de dicha suma.

Con esto espero que hayas obtenido una idea sobre cómo funcionan las operaciones, queda de parte de ti si prefieres utilizar la versión larga del operator fun o el operador directamente.

Ten en cuenta que si las operator fun se inventaron para que puedas reducir tu código a operaciones con símbolos ¿por algo será, no?

### Clase 12 *Kotlin y la programación funcional*

Los lenguajes de programación comunes suelen permitir diferentes paradigmas de programación. Dentro de estos, se hace una distinción aproximada entre los paradigmas de **programación declarativa** y de **programación imperativa**. Simplificando mucho, estos paradigmas constituyen los métodos fundamentales de programación.

**Paradigma Imperativo**

Es el paradigma de programación más antiguo. Los programas consisten en una sucesión de instrucciones o conjunto de sentencias, como si el programador diera órdenes concretas. El desarrollador describe en el código paso por paso todo lo que hará su programa.

Ejemplos de programación imperativa más conocidos son: FORTRAN, PASCAL, COBOL, C, C#, C++, Ruby, etc.

**Paradigma Declarativo**

Este paradigma no necesita definir algoritmos puesto que describe el problema en lugar de encontrar una solución al mismo. Este paradigma utiliza el principio del razonamiento lógico para responder a las preguntas o cuestiones consultadas.

Este paradigma a su vez se divide en dos:

- **Programación Lógica:** Prolog
- **Programación funcional:** Lisp, Scala, Java, Kotlin

**Programación Funcional**

La programación funcional es un paradigma declarativo. Nos enfocaremos en "qué" estamos haciendo y no en "cómo" se está haciendo que sería el enfoque imperativo. Esto quiere decir que nosotros expresaremos nuestra lógica sin describir controles de flujo; no usaremos ciclos o condicionales.

Aunque Kotlin no es un lenguaje de programación funcional al 100% como Haskell o Scala, sigue teniendo muchos conceptos que, al entenderlas, nos ayudaran a sacar un mayor provecho del lenguaje, tales como:

- **Inmutable:** Un objeto inmutable es aquel que no puede ser modificado una vez haya sido creado. En la programación funcional la inmutabilidad es lo que hace que los demás conceptos funcionen. Si nuestra data fuera mutable la composición de funciones colapsaría y podríamos fallar en no tener estado compartido, que es otro de los pilares de la programación funcional.
- **Efectos secundarios:** En la programación funcional un efecto secundario es cualquier cambio en el estado/comportamiento de la aplicación observable fuera de la función en la que se ejecuta. En algunas ocasiones los efectos secundarios son evidentes y en otros un poco más sutiles.
- **Funciones puras:** Son funciones con la característica que generando una misma entrada retornaran a la misma salida, este no contiene efectos secundarios.
- **Composición de funciones:** Se refiere al proceso en que se fusionan dos o más funciones, esto para que sean ejecutadas en secuencia y generar un resultado concreto.
- **Recursividad:** Es una técnica muy usada en programación funcional porque nos evita el uso de iteraciones. Las funciones recursivas se invocan a sí mismas, permitiendo que una operación se realice una y otra vez hasta alcanzar el caso base.
- **Sistemas de Tipos:** Un sistema de inferencia de tipos permite inferir los tipos de las expresiones sin obligar al programador a su declaración explícita. En caso de que el programador los haya declarado, se comprueba que los tipos declarados encajan con los tipos inferidos por el sistema
- **Funciones de orden superior:** Son funciones que pueden tomar otras funciones como argumentos o devolverlos como resultados.

### Clase 13 *Estructuras de control: if*

Las **estructuras condicionales** comparan una variable contra otro(s) valor(es), para que en base al resultado de esta comparación, se siga un curso de acción dentro del programa. Cabe mencionar que la comparación se puede hacer contra otra variable o contra una constante, según se necesite. Existen tres tipos básicos, las simples, las dobles y las múltiples.

**Simples**
Las estructuras condicionales simples se les conoce como «Tomas de decisión». Estas tomas de decisión tienen la siguiente forma:

![src/kotlinCero_20.png](src/kotlinCero_20.png)

Donde:

- **Si:** Indica el comando de comparación
- **Condición:** Indica la condición a evaluar
- **Entonces:** Precede a las acciones a realizar cuando se cumple la condición
- **Instrucción(es):** Son las acciones a realizar cuando se cumple o no la condición

**Dobles**

Las estructuras condicionales dobles permiten elegir entre dos opciones o alternativas posibles en función del cumplimiento o no de una determinada condición. Se representa de la siguiente forma:

![src/kotlinCero_21.png](src/kotlinCero_21.png)

Donde:
- **Si:** Indica el comando de comparación
- **Condición:** Indica la condición a evaluar
- **Entonces:** Precede a las acciones a realizar cuando se cumple la condición
- **Instrucción(es):** Son las acciones a realizar cuando se cumple o no la condición
- **Si no:** Precede a las acciones a realizar cuando no se cumple la condición
	Dependiendo de si la comparación es cierta o falsa, se pueden realizar una o más acciones.

**Múltiples**

Las estructuras de comparación múltiples, son tomas de decisión especializadas que permiten comparar una variable contra distintos posibles resultados, ejecutando para cada caso una serie de instrucciones específicas. La forma común es la siguiente:

![src/kotlinCero_22.png](src/kotlinCero_22.png)

**Múltiples (En caso de)**

Las estructuras de comparación múltiples, es una toma de decisión especializada que permiten evaluar una variable con distintos posibles resultados, ejecutando para cada caso una serie de instrucciones específicas. La forma es la siguiente:

![src/kotlinCero_23.png](src/kotlinCero_23.png)

Hasta ahora solo hemos nuestros ejemplos solo han sido ejecutadas en el orden en que son formuladas. El orden de ejecución de las instrucciones es lo que se conoce como **Flujo del Programa**, y estas instrucciones pueden variar a voluntad utilizando las **sentencias de control de flujo**, con las que es muy fácil alterarlo para adecuarlo a nuestras necesidades. Esto es lo que hace potentes a los lenguajes de programación. Básicamente, existen tres tipos de sentencias; secuencial, condicional e iterativa, y con ellas se puede escribir cualquier programa.

**Sentencias Condicionales**

Existen dos formas de alterar el flujo dependiendo de una condición. La idea básica es la de encontrarnos ante una bifurcación de un camino, en la que seguiremos por uno u otro camino dependiendo de la respuesta a una pregunta que se halla escrita en la bifurcación. Una variante de esto es que en lugar de dos posibilidades, se nos presenten más caminos por los que poder seguir.

**Sentencia if**

La forma más elemental de control de flujo condicional y se emplea para tomar decisiones en función de una condición. Su sintaxis es la siguiente:

![src/javaSE_131.png](src/javaSE_131.png)

Si la condición se cumple (es decir, si su valor es **true**) se ejecutan todas las instrucciones que se encuentran dentro de {...}. Si la condición no se cumple (es decir, si su valor es **false**) no se ejecuta ninguna instrucción contenida en {...} y el programa continúa ejecutando el resto de instrucciones del script.

Ejemplo:

![src/kotlinCero_24.png](src/kotlinCero_24.png)

Tenemos una variable **«nombre»**. Usando **isNotEmpaty()** podemos comprobar si «nombre» es una cadena vacía o no. SI se cumple la condición, es decir, «nombre» efectivamente tiene guardado un cadena, entonces imprimimos la cantidad de caracteres con las que se compone.

En Kotlin, si la instrucción dentro de la condicional es de una simple línea, podemos ahorrarnos las llaves y acortar nuestro código de la siguiente forma:

![src/kotlinCero_25.png](src/kotlinCero_25.png)

**Estructura if-else**

En ocasiones, las decisiones que se deben realizar no son del tipo "si se cumple la condición, hazlo; si no se cumple, no hagas nada". Normalmente las condiciones suelen ser del tipo "si se cumple esta condición, hazlo; si no se cumple, haz esto otro".

Para este segundo tipo de decisiones, existe una variante de la estructura if llamada if-else. Su sintaxis es la siguiente:

![src/javaSE_134.png](src/javaSE_134.png)

Si la condición se cumple (es decir, si su valor es **true**) se ejecutan todas las instrucciones que se encuentran dentro del if(). Si la condición no se cumple (es decir, si su valor es **false**) se ejecutan todas las instrucciones contenidas en else{ }. Ejemplo:

![src/kotlinCero_26.png](src/kotlinCero_26.png)

Siguiendo nuestro ejemplo anterior. Tenemos una variable **«nombre»** el cual evaluaremos; SI se cumple la condición, es decir, la variable efectivamente tiene guardado un valor, entonces nos imprimirá la cantidad de caracteres con las que se compone. SI NO se cumple, es decir, tenemos un valor nulo (null), entonces nos imprimirá un mensaje para avisarnos.

Aunque no es la práctica más correcta y no deberíamos abusar, en determinadas ocasiones necesitamos más condiciones, y aunque podríamos recurrir a otras instrucciones, es posible construir una serie de comprobaciones uniendo un if a la cláusula else de un if anterior:

![src/javaSE_142.png](src/javaSE_142.png)

Si la primera condición se cumple (es decir, si su valor es **true** para la condicional_1) se ejecutan todas las instrucciones que se encuentran dentro del if(). Si la segunda condición  (es decir, su valor es **true** para la condicional_2) se ejecutan las instrucciones que contiene el else if(). Pero, si no se cumple ninguna (es decir, si su valor es **false** tanto para el primero como para el segundo) se ejecutan todas las instrucciones contenidas en else{ }. Ejemplo:

![src/kotlinCero_27.png](src/kotlinCero_27.png)

Tenemos dos variables, **«nombre»** y **«mensaje»**. Nosotros evaluaremos la variable «nombre»; SI nuestro nombre es mayor a 4, nos imprimirá el mensaje de que tenemos un nombre largo, pero SI nuestro nombre es nulo (es decir, está vacío) nos alertara imprimiendo un mensaje diferente, y si ninguna de las dos condiciones es cumple (es decir, no es nulo, pero tampoco mayor a 4) entonces nos imprimirá un mensaje para decirnos que tenemos un nombre corto.

Con nuestro IntelliJ podemos acortar aún más nuestro código, ya que el entorno nos aconsejara que creemos una condicional que asigne directamente el valor a una variable y también podemos optar por suprimir las llaves:

![src/kotlinCero_28.png](src/kotlinCero_28.png)

### Clase 14 *Estructuras de Control: when*

En lugar de la ampliamente utilizada declaración **switch**, Kotlin proporciona la expresión **when** que es mucho más flexible, concisa y poderoso.

**Expresión when**

Es una estructura de control para agilizar el flujo del programa en opciones múltiples. Se tiene una condición que se puede cumplir dependiendo de diferentes casos, cada caso nos lleva a un bloque de cumplimiento de la condición y ese bloque nos lleva a continuar el programa. Su sintaxis es la siguiente:

![src/kotlinCero_29.png](src/kotlinCero_29.png)

En comparación al switch, when es más conciso:

- No necesita agrupaciones complejas con case / break, solo la condición seguida de ->.
- Puede ser usada como expresión o declaración.
- Puede agrupar dos o más opciones equivalentes, separándolas con una coma.

Ejemplo:

![src/kotlinCero_30.png](src/kotlinCero_30.png)

Tenemos una variable **«nombreColor»**. Usando la expresión **when** evaluaremos esa variable y, dependiendo de cual valor cumple, el programa nos dará diferentes resultados.

Si la instrucción es de una sola línea, podemos ahorrarnos las llaves y acortar nuestro código. También, en lugar del default que tiene switch, la expresión when hace uso del else y, si tenemos varias opciones que devuelvan una misma respuesta, podemos agruparlas separándolos por una coma:

![src/kotlinCero_31.png](src/kotlinCero_31.png)

Pero la expresión when no solo funciona con cadenas de texto, también podemos evaluar números:

![src/kotlinCero_32.png](src/kotlinCero_32.png)

O podemos verificar el rango comprendido entre dos números. Para esto, creamos el rango utilizando el operador .. (punto doble) y el operador in sirve para verificar si un valor pertenece a un rango:

![src/kotlinCero_33.png](src/kotlinCero_33.png)

## Modulo 4. Conceptos básicos de Kotlin
### Clase 15 *Bucles: While y Do While*

Un **loop** es una estructura iterativa que permite repetir un bloque de instrucciones. Esta repetición es controlada por una condición booleana.

**While**
Es un bucle o sentencia repetitiva con una condición al principio. Se ejecuta una sentencia especificada mientras cierta condición se evalúe como verdadera. Dicha condición es evaluada antes de ejecutar la sentencia.

La sintaxis es:

![src/javaSE_158.png](src/javaSE_158.png)

Ejemplo:

![src/kotlinCero_34.png](src/kotlinCero_34.png)

Tenemos una variable **«contador»**. Con el bucle while evaluaremos el contador, mientras sea mayor a 0 imprimiremos el valor actual e iremos decrementando el valor de la variable en uno.

**NOTA:**

La evaluación se realiza antes de ejecutar el bloque. Si la expresión es **true** pasa a ejecutar de forma repetida el bloque de sentencias. Cada vez que termina de ejecutar el bloque de sentencias vuelve a evaluar la expresión. Si la expresión sigue siendo verdadera (true) vuelve a ejecutar el bloque. En el caso de que la expresión sea **falso** se saldrá del bucle.

Es por ello que dentro del bloque de sentencias deberán de existir sentencias que modifiquen la evaluación de la expresión, ya que de no hacerse se podría entrar en un bucle infinito.

***Los casos de uso de una sentencia repetitiva while son variados, pero principalmente se utiliza para recorrer estructuras de datos o tener contadores.***

**Do-While**

Es un bucle o sentencia repetitiva con una condición al final. Ejecuta una sentencia especificada, hasta que la condición de comprobación se evalúa como falsa. La condición se evalúa después de ejecutar la sentencia, dando como resultado que la sentencia especificada se ejecute al menos una vez.

La sintaxis es:

![src/javaSE_159.png](src/javaSE_159.png)

Ejemplo:

![src/kotlinCero_35.png](src/kotlinCero_35.png)

Creamos un bucle do-while, en su interior generaremos un número aleatorio. Primeramente indicaremos que generaremos un número aleatorio y para eso creamos la variable **«numeroAleatorio»**, especificamos que tiene que estar en un rango de 0 a 100 y hacemos uso de la función **random()** para obtener un número aleatorio dentro de ese mismo rango. Después imprimimos el resultado en pantalla. Si el número aleatorio es mayor a 50, volveremos al bucle, pero si el número es menor, entonces el bucle se detendrá.

**NOTA:**

El bucle do-while es prácticamente igual al while, pero con la diferencia de que el código del bucle se ejecutara al menos una vez ya que la comprobación se hace después de cada iteración y no antes como en el caso del while.
	
***Este tipo de bucle es el idóneo cuando necesitamos que un fragmento de código se ejecute al menos una vez y dependiendo de las circunstancias puede ser que se vuelva a repetir un número indeterminado de veces o ninguna. Un ejemplo claro del bucle do-while serían los menús de aplicaciones, los cuales mostraremos en forma de eco por pantalla, hasta que se introduzca la opción de salida.***

### Clase 16 *Ciclos*

El **bucle for** se utiliza para repetir una o más instrucciones un determinado número de veces, pero en Kotlin es un poco distinto a como es en otros lenguajes, aquí tenemos una variable que itera sobre rangos o datos estructurados y como tal en cada iteración toma el siguiente valor.

La sentencia se compone de una **declaración de variables**, una **expresión contenedora**, compuesta por el operador **in** y los datos estructurados (arreglos, listas, etc.), y el **cuerpo del bucle**:
	
![src/kotlinCero_36.png](src/kotlinCero_36.png)

Ejemplo:

![src/kotlinCero_37.png](src/kotlinCero_37.png)

Creamos una variable que contendrá nuestra lista de fruta compuesta por cuatro cadenas de textos (strings), para crear la lista hacemos uso de la función **listOf()**, y para poder imprimir su contenido usamos el **ciclo for**, donde **fruta** será la variable y **listaDeFrutas** nuestra estructura de datos.

Aunque usamos el cuerpo como un bloque de código, al ser una sola sentencia, puedes omitir las llaves:

![src/kotlinCero_38.png](src/kotlinCero_38.png)

**Lista**

Una lista es una colección genérica de elementos que se caracteriza por almacenarlos de forma ordenada, donde pueden existir duplicados (incluso un ítem null) y se indexan los elementos con base 0.

Su diseño es representado por la interfaz genérica **List< E >**, la cual hereda las operaciones base para colecciones de **Collection< E >**:

![src/kotlinCero_39.png](src/kotlinCero_39.png)

Si deseas crear una lista debes primero definir si será de solo lectura o mutable.

**Listas de solo lectura**

Similar a las variables de solo lectura, una lista de solo lectura (*read-only list*) puede ser consultada luego de ser inicializada, pero no te permite el uso de comandos para cambiar su estado.

Para crear una lista de solo lectura usa la función **listOf()**, la cual recibe como argumentos un grupo de ítems de un mismo tipo. Por ejemplo, crear nuestra lista de frutas:

![src/kotlinCero_40.png](src/kotlinCero_40.png)

Al inicializar una lista cuyo contenido sea claro, es posible omitir el tipo parametrizado. Por lo que en el caso anterior puedes remover a List< Int >.

**forEach**

El bucle forEach es una estructura especializada en recorrer los elementos que contiene una variable, es por eso que está especialmente indicado para ver o recorrer todos los elementos de una estructura de datos.

La sintaxis es similar a la de Java. Sin embargo, en Kotlin, el lambda acepta un solo parámetro:

![src/kotlinCero_41.png](src/kotlinCero_41.png)

Siguiendo con nuestro ejemplo anterior, en esta ocasión utilizamos **forEach** para recorrer nuestra lista de frutas y en su interior tenemos una función anónima cuyo parámetro es **fruta** y estará recibiendo los valores de nuestra estructura de datos.

Como vimos en nuestro ejemplo de lista mutable podemos utilizar **it** como el nombre del parámetro por defecto y no necesitamos nombrarlo explícitamente.

**for vs forEach**

- Usar forEach en lugar del bucle for hace que nuestro código sea más conciso e inteligente.
- ForEach se utilizan para realizar acciones en todos y cada uno de los elementos de la lista.
- Es como un enfoque de función hacia la forma tradicional de bucle for.
- Tanto los bucles for como los forEach son iguales cuando se generan resultados a partir de una matriz o lista
- ForEach puede ser más útil si usamos operadores más funcionales.

**Lambda**

Una función lambda es un literal de función que puede ser usado como expresión. Esto quiere decir, una función que no está ligada a un identificador y que puedes usar como valor.

Por ejemplo, si tenemos la función **f(s) = s + 2**, en Kotlin podemos expresarla como una declaración de función separada, así:

![src/kotlinCero_42.png](src/kotlinCero_42.png)

Al ser reescrita como lambda, tendrías lo siguiente:

![src/kotlinCero_43.png](src/kotlinCero_43.png)

Definir la función de esta forma te permitirá usarla como un valor en diferentes situaciones, como pasarla como argumento de una función o almacenarla en una variable.

La sintaxis de un literal lambda va al interior de dos llaves {}. Sus componentes son:

- **Lista de parámetros** — Cada parámetro es una declaración de variable, aunque esta lista es opcional
- **Operador de flecha ->** — Se omite si no usas lista de parámetros
- **Cuerpo del lambda** — Son las sentencias que van luego del operador de flecha

![src/kotlinCero_44.png](src/kotlinCero_44.png)

La anterior sintaxis de la imagen se puede leer como «para cada par de s y t corresponde el valor 2*(s+t).

**Función map**

La función de orden superior map { } nos permite aplicar una función sobre todos los elementos de una colección con el fin de una nueva colección con el cálculo final.

Por ejemplo, tenemos nuestra lista de frutas y quisiéramos obtener otra lista que tome cada elemento como argumento y nos entregue la cantidad de caracteres que compone ese elemento, es decir, cuantas letras tiene el nombre de cada fruta:

![src/kotlinCero_45.png](src/kotlinCero_45.png)

La solución consistió en pasar una función lambda que nos permita accede a la propiedad miembro **length** del string para poder obtener el tamaño de la secuencia de caracteres.

**Función filter()**

La función de extensión filter nos permite filtrar los ítems de una colección de elementos a partir de un predicado como argumento.

![src/kotlinCero_46.png](src/kotlinCero_46.png)

El predicado afirma o niega expresiones sobre el sujeto (cada elemento de la colección). Si un elemento satisface al predicado, entonces es incluido en el resultado final.

Este parámetro es representado por un tipo función cuyo único argumento es el sujeto y el cuerpo es Boolean. En la ilustración anterior veías que si se aplica el predicado x > 0 sobre la lista L = {-2 ,-1 ,0, 1} el resultado solo será el elemento 1.

Considerando nuestra lista de frutas, nosotros deseamos obtener aquellas cuyo tamaño de secuencia de caracteres sea mayor a 5. Usa la función filter y pasa una lambda que exprese este predicado:

![src/kotlinCero_47.png](src/kotlinCero_47.png)

Usa la condición **largoDeFruta > 5** para determinar si el tamaño de la secuencia de caracteres es mayor a 5. Efectivamente la salida será una lista List< Int > con 7, 8 y 7 que son los que satisfacen esta descripción.

### Clase 17 *Null-Safety en Kotlin*

La nada es un concepto ligado al lenguaje; en Kotlin, el pariente más cercano es el **null**. Para escribir código sólido, es importante comprender el concepto de nulo.

**¿Qué representa null?**

Null es un flag. Representa diferentes situaciones según el contexto en que se utiliza e invoca.

Esto produce el error más grave en desarrollo de software: Acoplar una decisión oculta en el contrato entre un objeto y quién lo utiliza.

Por si esto fuera poco rompe la biyección que era nuestra única regla de diseño, al representar múltiples elementos del dominio y obligando a tener interpretaciones contextuales.

Un buen principio de software nos reta a tener alta cohesión. Esto quiere decir que los objetos sean lo más específicos posible y tengan una única responsabilidad (La S de Solid). El objeto con menor cohesión de cualquier sistema es nuestro comodín: null.

**El error de los mil millones de dólares**

La creación de null ocurrió por un hecho fortuito en el año 1965.

Tony Hoare, el creador del algoritmo QuickSort y también ganador del premio Turing (el equivalente al Premio Nobel en Computación), lo agregó al lenguaje Algol porque le parecía práctico y fácil de hacer. Varias décadas después mostró su arrepentimiento:

*Esta excelente nota cuenta la historia en detalle
Lo llamo mi error de mil millones de dólares … En ese momento, estaba diseñando el primer sistema de tipos para referencias en un lenguaje orientado a objetos. Mi objetivo era asegurar que todo uso de referencias debería ser absolutamente seguro, con una verificación realizada automáticamente por el compilador. Pero no pude resistir la tentación de poner una referencia nula, simplemente porque era muy fácil de implementar. Esto ha llevado a innumerables errores, vulnerabilidades y fallas en el sistema, lo que probablemente ha causado miles de millones de dólares de dolor y daños en los últimos cuarenta años.* — Tony Hoare, inventor de ALGOL W.

**Null en Kotlin**

Uno de los errores más comunes en muchos lenguajes de programación es acceder a un miembro de referencia nula que dará como resultado una excepción de referencia nula. Esto sería el equivalente a un NullPointerException (NPE).

Kotlin tiene como objetivo eliminar el riesgo de los **NullPointerException**. Distingue entre referencias anulables y no anulables como parte de su sistema de tipos. En Kotlin, el sistema de tipos distingue entre referencia que pueden contener null (variables que aceptan el valor NULL) y aquellas que no pueden (variables del tipo no anulables). Es por eso que Kotlin es **Null Safety**, es decir, que gestiona los nulos de forma segura, de modo que puedes garantizar que tu código no va a producir NullPointerException.

Las únicas causas posibles de un NPE en Kotlin son:

- Una llamada explícita a throw NullPointerException().
- Uso del operador !!
- Inconsistencia de datos con respecto a la inicialización.
- Interoperación con Java, como por ejemplo problemas causados por el código Java externo o problemas de nulabilidad con tipos genéricos que se utilizan para la interoperación de Java.

**La excusa**

Los desarrolladores utilizan null porque es cómodo (de escribir) y porque creen que mejora la eficiencia del software. Al cometer este error ignoran que el código se lee hasta 10 veces más de las que se escribe.

Leer código con nulls es más arduo y dificultoso. Por lo tanto, solo están posponiendo el problema para más adelante. Con respecto a la eficiencia (que es la excusa más utilizada para generar acoplamiento), salvo en casos muy puntuales y críticos, esta pérdida en la performance es despreciable. Y solo se justifica en aquellos sistemas que privilegien la eficiencia sobre la legibilidad, adaptabilidad y mantenibilidad.

Este sesgo cognitivo se mantuvo en el tiempo a pesar de que, según el estado del arte actual las máquinas virtuales modernas optimizan el código por nosotros. Para utilizar evidencias en vez de opiniones, solo necesitamos empezar a hacer benchmarks en vez de continuar afirmando erróneamente que la eficiencia es más importante que la legibilidad.

***Benchmarks: Una prueba de rendimiento o comparativa es una técnica utilizada para medir el rendimiento de un sistema o uno de sus componentes.***

**Falla Rápido**

Null se (ab)usa para enmascarar situaciones inesperadas y propagar el error en el código muy lejos generando el tan temido efecto de onda.

Uno de los principios de un buen diseño consiste en fallar rápidamente.

Supongamos un formulario de ingreso de datos de un paciente donde se pide ingresar la fecha de nacimiento. En caso de existir un error en el componente visual y en la creación del objeto, este podría construirse con una fecha de nacimiento null. Al correr algún proceso nocturno a la noche que recolecte todas las fechas de los pacientes para calcular un promedio de edad el paciente ingresado va a generar un error.

El stack con información útil para el desarrollador va a estar muy lejos del lugar donde se está presente el defecto. Eventualmente podrían ser distintos sistemas con distintos lenguajes de programación o con transmisión de datos a través de una API, archivos etc.

La pesadilla del desarrollador es tener que depurar ese error a la madrugada y tratar de encontrar la causa raíz del problema.

**Trabajar con tipos que aceptan valores nulos**

- **Verificación igualdad a NULL**

	Podemos usar la expresión if-else para verificar explícitamente las variables que aceptan valores NULL . Sin embargo, esta opción solo funciona cuando la variable es inmutable. Dependiendo de la complejidad de las condiciones, esto también puede conducir a expresiones anidadas.

- **Operador de Acceso Seguro (?)**

	Kotlin tiene un operador  de acceso seguro, o Safe Call, para manejar referencias nulas. Este operador ejecuta cualquier acción solo cuando la referencia tiene un valor no nulo. De lo contrario, devuelve un valor nulo. El operador Safe Call combina una verificación nula junto con una llamada a un método en una sola expresión.

- **Método let()**

	Podemos hacer uso del método let() junto con el operador Safe Call para actuar sobre una variable que no acepta valores NULL.

- **Método also()**

	El método also() se utilizan para ejecutar operaciones adicionales como el registro y la impresión de las variables que no aceptan valores NULL. Además, este método puede ser utilizado en una cadena con let() o con el método run().

- **Método run()**

	El método run() es usado para ejecutar algunas operaciones en una referencia que no acepta valores NULL. Este método opera usando esta referencia y devuelve el valor del resultado lambda.

- **Operador Elvis ( ?: )**

	El operador Elvis nos devuelve un valor predeterminado solo si la variable original tiene un valor nulo. Si la expresión del lado izquierdo del operador de Elvis tiene un valor que no acepta valores NULL, se devuelve. De lo contrario, se devuelve la expresión del lado derecho.

- **Operador !!**

	Podemos usar el operador de aserción not null (!!) o not-null assertion operator para lanzar explícitamente una NullPointerException. Este operador convierte cualquier valor a un tipo no anulable. Si no se puede, se lanza una excepción del tipo NullPointerException.

### Clase 18 *Valores nulos, Double bang y cómo solucionarlos*

Los null no son malos, son incomprendidos. Como toda herramienta de programación, el null puede ser buena o mala dependiendo del uso que nosotros le estamos dando.

**Nullables**

Las variables de tipo nulo en Kotlin no existen mientras no se diga lo contrario. Es decir, a ningún objeto, por defecto, se le puede asignar null. Recuerda que en Kotlin todos los tipos son objetos.

Las variables nullables son aquellas que pueden aceptar valores null. Si necesitamos un tipo que acepte nulos, debemos definirlo como anulable, ubicando un signo de interrogación de cierre (?) al final del tipo.

Por ejemplo:

![src/kotlinCero_48.png](src/kotlinCero_48.png)

La variable **noAceptaNull** es de tipo no anulable, por lo que si intentas asignarle null tendremos el error:
***Null can not be a value of a non-null type String***

Por el otro lado **aceptaNull** que ha sido declarado anulable con String?, si permite la asignación del literal constante null (ausencia de valor).

**El compilador es tu amigo, no tu enemigo**

El compilador es capaz de interpretar estos tipos de variables nullables y advertirnos de lo que puede ocurrir al ejecutar nuestro programa. Por lo tanto, el compilador es nuestro amigo y si vemos que nos muestra un error no debemos buscar una forma rápida de saltarnos o ignorar ese error, sino que debemos buscar la manera de utilizar el lenguaje para sacarle provecho.

***RECUERDA: No programes pensando en complacer al compilador, programa para tener un código eficiente.***

**La regla del Boy Scout**

Imaginemos que ingresamos a una nueva empresa y comenzamos a crear código, pusimos código nullable en todos lados y no le hicimos caso al compilador e ignoramos los warning. Más adelante, en tal vez seis meses, cuando sigamos en esa misma empresa y nos toque ver nuevamente ese código no entenderemos lo que hicimos en el pasado y sufriremos cuando debamos mejorarlo.

Se bueno cuando compiles. No compiles para complacer al compilador, utiliza al compilador como amigo para crear mejor código.

Esto se llama la ***regla de los Boy Scout***. Deja siempre el código mejor que lo encontraste.

**Safe Calls**

El operador  de acceso seguro, o Safe Call, para manejar referencias nulas. Este operador ejecuta cualquier acción solo cuando la referencia tiene un valor no nulo. De lo contrario, devuelve un valor nulo. El operador Safe Call combina una verificación nula junto con una llamada a un método en una sola expresión.

Por ejemplo:
	
![src/kotlinCero_49.png](src/kotlinCero_49.png)

Si el miembro existe, entonces se retorna el contenido, de lo contrario se obtendrá null del recibidor.

**Double Bang**

El operador de aserción not null (!!) o not-null assertion operator evitará la necesidad de chequear null si estás completamente seguro de que una variable nunca será nula.

Hay muy pocos casos en los que este operador tiene sentido. Casi siempre hay una solución mejor.

***RECOMENDACIÓN: Utilizar este tipo de operador lo menos posible, porque no son considerado buenas prácticas.***

Por ejemplo, el siguiente código produce una NPE debido a que el contador nunca se reasigna con un valor entero:

![src/kotlinCero_50.png](src/kotlinCero_50.png)

Al intentar usar **dec()** para disminuir el valor, la excepción se disparará.

**Un gran poder conlleva una gran responsabilidad**

Digamos que somos una persona que ha probado mucho nuestro código, estamos 1000% seguros de que podemos usar el símbolo del Double Bang para saltarnos la prohibición de nullabilidad. Obviamente podemos hacerlo sin ningún problema, pero quedara bajo nuestra responsabilidad cuando el programa comience a fallar.

**Interoperabilidad con Java**

Cuando estamos trabajando con librerías Java, podemos encontrarnos ante diferentes situaciones con respecto al chequeo de nulos.

- **La librería está correctamente anotada**

	Si se están utilizando adecuadamente las anotaciones *@Nullable* y *@NotNull*, tanto las de Java como las propias de Android, Kotlin será capaz de trabajar sin problemas con ellas para deducir cuándo una variables es nula y cuándo no.
	Muchas partes del framework de Android ya están anotadas correctamente, así que esto es una ventaja enorme para trabajar con Kotlin.

- **La librería no tiene anotaciones**

	Sin embargo, si la librería no está anotada, los tipos serán marcados con un operador especial (una única !), lo que significa que queda en nuestra mano decidir si un parámetro o valor de retorno acepta nulo o no.
	
Con este tipo de casos tenemos dos recomendaciones:

- **Si tenemos acceso al código fuente, lo mejor es comprobar qué valores acepta el código en cuestión que estemos utilizando**

	Un ejemplo en Android que no está anotado es la librería de soporte de RecyclerView. Cuando creas un adapter y autogeneras los métodos, por defecto les añadirá una interrogación a los tipos.
	Pero si miras el código fuente, te darás cuenta de que nada puede ser null en los métodos que necesitas sobrescribir. Así que puedes deshacerte de todas las interrogaciones, y evitar chequeos de nulos innecesarios.

- **Si no tenemos acceso al código fuente, lo mejor será siempre tratarlos como del tipo nullable y mantener un ojo puesto en ellos**

	Por ejemplo, digamos que entramos a trabajar en una empresa que cuyo código de Java ha migrando a Kotlin, nosotros podemos encontrarnos con un tipo de dato raro que lleva un símbolo de exclamación al final (ejemplo, **Integer!**). Esto no significa que esa variable sea exactamente del tipo nullable, es solo la manera que tiene Kotlin de avisarte que NO puede asegurarse de que ese código no devuelve null.
	Solo nos queda asegurarnos de vigilar bien esas variables, porque en muchos casos pueden devolvernos valores nulos cuando menos lo esperamos y esto puede causar que nuestras aplicaciones se cierren inesperadamente.

### Clase 19 *Try Catch*

Las excepciones son problemas que ocurren en nuestro código durante la ejecución del programa e interrumpen el flujo convencional. Esto puede ocurrir debido a varias razones, como una operación aritmética no válida o una referencia nula.

**Manejo de Excepciones**

Es la capacidad de abordar (o manejar) la excepción que podría ocurrir. Si no manejamos cualquier excepción que ocurra, nuestro programa detendrá abruptamente la ejecución, cerrando nuestra aplicación inmediatamente.

El manejo de excepciones permite a nuestro programa continuar la ejecución incluso si hubo una excepción (aunque es altamente recomendable reportar tus excepciones usando una herramienta de reporteo de errores como Crashlytics).

**Excepciones de Kotlin**

En Kotlin, solo hay **excepciones no revisadas** que son arrojadas debido a fallas lógicos y se verifican en el tiempo de ejecución.

Los ejemplos de excepciones no revisadas incluyen:

- **ArithmeticException:** lanzada cuando divides entre cero.
- **ArrayIndexOutOfBoundExceptions:** arrojada cuando un arreglo ha sido accedido con un índice ilegal.
- **SecurityException:** Arrojada por el administrador de seguridad para indicar una violación de seguridad.
- **NullPointerException:** arrojada cuando se invoca un método o propiedad de un objeto nulo.

Aunque Kotlin hereda el concepto de excepción de Java, no admite ***excepciones revisadas***.

Las **excepciones revisadas** se consideran una característica controvertida en Java. Disminuye la productividad del desarrollador sin ningún aumento adicional en la calidad del código. Entre otros problemas, las excepciones revisadas también conducen a código repetitivo y dificulta el usar expresiones lambda.

Entonces, como muchos otros lenguajes de programación modernas, los desarrolladores de Kotlin también decidieron no incluir excepciones revisadas como una característica del lenguaje.

**Try-Catch**

Al igual que en Java, Kotlin nos permite capturar excepciones con la expresión ***try..catch..finally***.

En el bloque **try** ponemos el código que es propenso a lanzar excepciones y luego añade bloques **catch** que verifiquen la aplicabilidad de un subtipo de excepción.

Tomemos el siguiente código como ejemplo:

![src/kotlinCero_51.png](src/kotlinCero_51.png)

Tenemos dos variables, **«result1»** y **«result»**, en donde imprimiremos el resultado de dos divisiones. Dentro del bloque **try** están encerradas las divisiones porque pueden lanzarnos excepción, en la primera variable haremos la división y nos imprimirá el resultado **[ 10 / 2 = 5 ]**. En la segunda variable se detectara una excepción que será capturado por el bloque catch y se ejecutará el println() con la excepción.

El bloque **finally** se ejecuta luego de que se aplique o no algún bloque catch. Normalmente aquí liberamos los recursos que has tomado del sistema y limpiamos las referencias para evitar fugas de memoria.

![src/kotlinCero_52.png](src/kotlinCero_52.png)

**Lanzar excepciones en Kotlin**

Para lanzar objetos de excepción en Kotlin, usa la expresión **throw** seguido de la instanciación del tipo. Al igual que en Java, la declaración del tipo debe tener como supertipo a la interfaz **Throwable**.

![src/kotlinCero_53.png](src/kotlinCero_53.png)

### Clase 20 *Elvis operator*

**Elvis Operator ( ?: )** se usa para devolver un valor no nulo, incluso cuando la expresión condicional es nula. También se utiliza para comprobar la seguridad nula de los valores. En algunos casos, podemos declarar una variable que puede contener una referencia nula.

Tomemos el siguiente código como ejemplo:

![src/kotlinCero_54.png](src/kotlinCero_54.png)

Tenemos una variable **«nombre»** y deseamos imprimir el tamaño de caracteres, pero esa variable «nombre» también puede contener referencias nulas. Antes de conseguir el tamaño de caracteres, tenemos que verificar su nullabilidad. Para eso creamos una nueva variable, **«caracterNombre»**, que contendrá la longitud de caracteres y usamos el Operador Elvis.

SI nuestra variable «nombre» es nula, entonces se devolverá el valor por defecto que en este caso es 0. Pero si «nombre» NO es nula, entonces obtendremos el tamaño de caracteres.
