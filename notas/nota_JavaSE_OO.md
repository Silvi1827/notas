## Modulo 1. Entender la Programación orientada a objetos
### Clase 1 *Programación orientada a objetos en Java*

Uno de los más grandes retos que tienen los programadores es analizar los problemas para posteriormente plasmarlos en código y es precisamente aquí donde la Orientación a Objetos es clave, pues surge a partir de los problemas que se tienen y de la necesidad de expresarlo en código.

Uno podría tener su propia metodología de análisis del problema para plasmarlo en un lenguaje de programación particular, pero en general la Orientación a Objetos ayuda a entender que está sucediendo con ese problema para poder reflejarlo en código de la mejor forma y de una manera más sostenible hacia el futuro. Para eso básicamente necesitaremos observar el problema o los elementos que están involucrados ahí en formas de objetos.

**¡Te damos la bienvenida al Curso de Java SE Orientado a Objetos!**

Porque Java es el campeón de la orientación a objetos ya que precisamente este lenguaje de programación surgió de este paradigma y es uno de los ganadores que ha marcado el rumbo de la orientación a objetos.

Nuestra profesora será Anahí Salgado y este es el segundo curso de la ruta para Java SE, por lo que es muy recomendable que antes de seguir hayas tomado el [Curso de Introducción a Java SE](https://platzi.com/clases/java-basico/ "Curso de Introducción a Java SE") y [Curso de Programación Orientada a Objetos: POO](https://platzi.com/cursos/oop/ "Curso de Programación Orientada a Objetos: POO"). Al terminar este curso puedes continuar con el Curso de Java SE: Programación Funcional.

**¿Qué es un paradigma?**

Es una teoría que nos suministra una base y modelo estandarizado para resolver problemas con nuestro código.

Recordemos que la orientación a objetos nos ayuda a analizar y entender todos estos problemas para resolverlos. Y es por eso que decimos es un paradigma, porque tiene un modelo para la resolución de problemas.

Este paradigma se compone de 4 elementos:

- Clases
- Propiedades
- Métodos
- Objetos

Además, se basa en los siguiente 4 pilares:

- Encapsulamiento
- Abstracción
- Herencia
- Polimorfismo

La orientación a objetos también está muy ligado a la UML (Unified Modeling Language o, en español, Lenguaje de Modelado Unificado). Parte de la orientación a objetos es analizar un problema, pero adicionalmente también observamos, graficamos y finalmente programamos. Y es en la parte de graficar donde el UML es un tema clave.

### Clase 2 *¿Qué es un Objeto?*

Los **objetos** son todas las cosas que tienen propiedades y comportamientos, estos pueden ser físicos o conceptuales, y siempre serán nombradas en sustantivos. Cuando decimos físico nos referimos a todo aquello que sea tangible, mientras que el objeto conceptual sería todo aquello que sea intangible, es decir, que no podemos tocar.

Por ejemplo, un objeto físico puede ser User (usuario) o Car (auto). Y un objeto conceptual sería Session (sesión).

**Propiedades**

También llamadas atributos, son la clave para cuando estemos identificando a los objetos y siempre serán escritas sustantivos.

Las Propiedades son las características de nuestros objetos y pueden tener diferentes valores que harán referencia a nombres, tamaños, formas, estados, etc.

Cuando estés analizando un objeto es un error común poner el resultado en lugar del atributo. Por ejemplo, puedes decir que tenemos un auto de color verde y cuando pensamos en la propiedad decimos que es verde, pero en realidad verde es el posible valor que tiene ese objeto auto. El verdadero atributo seria «color».

**Comportamiento**

Son todas las operaciones que puede hacer nuestro objeto y siempre serán en verbos o sustantivo y verbo. Por ejemplo, login(), logout(), makeReport().

### Clase 3 *Abstracción: ¿Qué es una Clase?*

La clase es el modelo sobre el cual se construirá nuestro objeto. Con las clases podremos generar más objetos, y eso es justamente lo que deseamos. Generamos un molde que nos permita obtener muchos más objetos. Para hacerlo analizamos nuestros objetos, traemos sus atributos y entonces generamos modelos llamada Clase.

Tomemos como un ejemplo una estrella:

![src/POO_26.png](src/POO_26.png)

Nosotros obtenemos el molde de esa estrella y así podemos obtener más estrellas de distintos colores. A esto se le llama abstracción.

**Abstracción**

Se trata básicamente de analizar objetos de forma independiente para abstraer su composición y generar un modelo, lo que traducimos a código como clases.

El primer paso en todo esto es analizar, una vez hecho todo eso continuamos el segundo paso de graficar y es aquí en donde hablamos del UML. Cuando tenemos una clase, un modelo lo suficientemente genérico, lo siguiente es plasmarlo en un diagrama UML:

![src/POO_33.png](src/POO_33.png)

En UML, una clase será representada como un rectángulo con tres zonas:

- **Superior:** Es donde colocaremos el nombre de la clase
- **Intermedio:** Aquí definiremos los atributos
- **Inferior:** Es donde estarán los comportamientos, es decir, los que serán las funcionalidades.

Con esto le daremos a nuestras clases en UML una identidad (nombre de la clase), estados (atributos o propiedades) y operaciones (comportamientos).

Para nuestro ejemplo, imaginemos que tenemos una clase **Person** cuyo atributo es **name** y su comportamiento sea **walk()**:

![src/POO_34.png](src/POO_34.png)

Las clases también nos ayudaran que es separar el código lo más posible para modularizarlo.

***RECUERDA: Las características o comportamientos que tendrán las clases son diferentes dependiendo del contexto en el que se encuentra.***

### Clase 4 *Modularidad*

La modularidad en Java se abarca en dos niveles:

- El nivel básico que estaremos viendo en el curso.
- El nivel avanzado que es para sistemas más grandes y lo veremos en Java SE: Programación Funcional.

**Modularidad**

Consiste en dividir nuestro programa en diferentes módulos de forma que puedan unirse o separarse sin romperse entre ellos o perder alguna funcionalidad.

La modularidad viene, aunque parezca extraño, del área del diseño que se dedican a las construcciones y la edificación.

Tomemos como ejemplo este sofá:

![src/POO_27.png](src/POO_27.png)

Este sofá fue divido y diseñado completamente módulos, cada asiento o lugar es un módulo que se pensó para robustecerla a medida que se van añadiendo más asientos.

![src/POO_28.png](src/POO_28.png)

Cada módulo (asiento) vive por sí mismo, y puede ser movido y unificado para crear un sistema entero.

La Modularidad en Programación Orientada a Objetos nos ayuda a:

- Reutilizar código
- Evitar colapsos
- Que nuestro código sea mantenible
- Mejorar la legibilidad
- Resolución rápida de problemas

En el curso anterior de Java SE empezamos a aplicar un poco de programación modular al separar código y delegarlo en diferentes módulos que fueron las funciones. Ahora podemos escalar a un nivel mayor y será a partir de las clases.

Las clases van a ser un elemento para manejar modularidad porque en vez de reorganizar el programa o archivo en muchas clases que al final sigue siguiendo la responsabilidad a un mismo archivo. Lo que haremos ahora es delegar la responsabilidad en diferentes archivos y cada archivo diremos que es un módulo, y cada módulo será una clase.

![src/POO_30.png](src/POO_30.png)

Imaginemos que la imagen representa nuestro programa. En una programación modular cada cuadro representa un archivo individual, nosotros podríamos fácilmente agregar o extraer un módulo y eso no afectara nuestro programa. Incluso, si por alguna razón tenemos un colapso, el error solamente ocurrirá dentro de ese módulo, así el detectar bugs o errores será más sencillo.

Idealmente cada clase va a tener su propio archivo, pero existe otros tipos de clases que son clases anidadas y estas también pueden vivir dentro del mismo archivo, pero en general son excepciones y no son tan común. Pero si partimos de la naturaleza de modularidad y queremos que nuestro proyecto sea mucho más fácil de mantener, lo más conveniente es trabajar con clases separadas por archivos.
