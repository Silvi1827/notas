# Fundamentos de Base de Datos
## Modulo 1. Bienvenida conceptos básicos y contexto histórico de las Bases de Datos
### Clase 1 *Expert Session: resuelve tus dudas sobre las bases de datos*
### Clase 2 *Bienvenida conceptos básicos y contexto histórico de las Bases de Datos*

Tu profesor será Israel Vázquez, senior web developer en San Francisco, seminarista de bases de datos y entusiasta data engineering.

**Historia de la persistencia de la información**

Históricamente la información se pasaba de boca en boca, pero eso distorsionaba la información de manera rápida. Desde la antigüedad se empezaron a dar cuenta que era necesario guardar la información de forma que no cambiara y persistiera más allá del tiempo de vida del ser humano, es por esto que se inventaron los sistemas de escrituras primitivos.

Una de las primeras escrituras encontradas, arqueológicamente, es la Escritura Cuneiforme que, aunque sea primitiva, es compleja en su estructura y la guardaban básicamente tallándolas en piedras o tablas de arcillas, pero tenían varias desventajas como no eran transportables o que las tabillas de arcillas se rompían fácilmente. Entonces se dio un salto y apareció el papiro o pergamino, eran más portátiles y ligeros, pero con la desventaja de que fueron basados en materia animal o vegetal y, por ello, se descomponían con facilidad o era fácil que fueran anidados por hongos. Fueron los chinos quienes revolucionaron el papel, contaba con la ventaja de ser transportable y no fácilmente destruible.

Pasaron varios siglos antes del siguiente salto, en el siglo XX tenemos el Microfilme, fue una tecnología que almacenaba datos de manera virtualmente infinita, la desventaja estaba en que guardar la información, leerla o modificarla requería maquinas muy especializadas que no eran fáciles de conseguir y no era muy fácil el proceso. La siguiente gran revolución son los medios digitales; discos duros, discos de estado sólido, discos compactos, en estos se guarda la información en formato de 1 y 0. Después de eso existió un periodo de recesión en los que no hubo grandes cambios hasta la aparición de la nube.

La nube tiene un gran pro comparada con los otros métodos de almacenamiento ya que es accesible desde cualquier parte del mundo, es centralizada y puede ser usada por varias personas al mismo tiempo.

**¿Qué son las bases de datos?**

Las bases de datos entran cuando hacemos la transición a medios digitales y, ahora, en la nube. Nos servían para complementar la arquitectura de Von Neumann, que es la arquitectura de computación clásica que incluyen una CPU, memoria y elementos de entrada y salida.

**Tipos de bases de datos**

- **Relacionales:** es un tipo de base de datos que almacena y proporciona acceso a puntos de datos relacionados entre sí. Se basan en el modelo relacional, una forma intuitiva y directa de representar datos en tablas. En una base de datos relacional, cada fila de la tabla es un registro con un ID único llamado clave. Las columnas de la tabla contienen atributos de los datos, y cada registro generalmente tiene un valor para cada atributo, lo que facilita el establecimiento de las relaciones entre los puntos de datos. Algunos ejemplos son; SQL Server, Oracle, MariaDB.

- **No relacionales:** conocidas como NoSQL, están diseñadas específicamente para modelos de datos específicos y tienen esquemas flexibles para crear aplicaciones modernas. Las bases de datos NoSQL son ampliamente reconocidas porque son fáciles de desarrollar, por su funcionalidad y el rendimiento a escala. Algunos ejemplos son; MongoDB, Cassandra, neo4j.

**Servicios**

- **Auto administrado:** es la base de datos que tú instalas en tu computadora o tu servidor y te encargas de las actualizaciones, mantenimiento, etc.
- **Administrado:** son servicios que ofrecen las nubes modernas, tú la utilizas pero no debes instalarla u ocuparte del mantenimiento o actualizaciones.

## Modulo 2. Introducción a las bases de datos relacionales
### Clase 3 *Historia de las RDB*

Las bases de datos surgen de la necesidad de conservar la información más allá de lo que existe en la memoria RAM.

En el esquema de arquitectura de Von Neumann básicamente se contempla la memoria principal, que es lo que conocemos como RAM, y se contempla el procesamiento de datos, pero irónicamente no se contempla el guardado de datos persistentes. Cuando tuvimos la necesidad de guardar y extraer fácilmente se empezaron formas inteligentes de hacer esto.

La primera fue la base de datos basadas en archivos, que no es lo mismo a la base de datos basadas en documentos, básicamente guardar los datos en un archivo de texto plano, fáciles de guardar pero muy difíciles de traer nuevamente en una forma ordenada o de realizar consultas más complejas. Ante la necesidad de algo un poco más estructurado nacen las bases de datos relacionales, el inventor es Edgar Codd que dejó 12 reglas o mandamientos para asegurar de que toda la filosofía de las bases de datos no se pierdan en el boca a boca o con prácticas un poco diferentes. Codd se aseguró de que el estándar fuera más consistente, más sólido.

**12 reglas de Codd**

- **Regla 0:** *Regla de fundación.* Cualquier sistema que se proclame como relacional, debe ser capaz de gestionar sus bases de datos enteramente mediante sus capacidades relacionales.
- **Regla 1:** *Regla de la información.* Toda la información en la base de datos es representada unidireccionalmente por valores en posiciones de las columnas dentro de filas de tablas. Toda la información en una base de datos relacional se representa explícitamente en el nivel Lógico exactamente de una manera: con valores en tablas.
- **Regla 2:** *Regla del acceso garantizado.* Todos los datos deben ser accesibles sin ambigüedad. Esta regla es esencialmente una nueva exposición del requisito fundamental para las llaves primarias. Dice que cada valor escalar individual en la base de datos debe ser lógicamente direccionable especificando el nombre de la tabla, la columna que lo contiene y la llave primaria.
- **Regla 3:** *Regla del tratamiento sistemático de valores nulos.* El sistema de gestión de base de datos debe permitir que haya campos nulos. Debe tener una representación de la "información que falta y de la información inaplicable" que sea sistemática y distinta de todos los valores regulares.
- **Regla 4:** *Catálogo dinámico en línea basado en el modelo relacional.* El sistema debe soportar un catálogo en línea, el catálogo relacional, que da acceso a la estructura de la base de datos y que debe ser accesible a los usuarios autorizados.
- **Regla 5:** *Regla comprensiva del sublenguaje de los datos.* El sistema debe soportar por lo menos un lenguaje relacional que:
1. Tenga una sintaxis lineal.
2. Puede ser utilizado de manera interactiva.
3. Tenga soporte de operaciones de definición de datos, operaciones de manipulación de datos (actualización así como la recuperación), de control de la seguridad e integridad y operaciones de administración de transacciones.
- **Regla 6:** *Regla de actualización de vistas.* Todas las vistas que son teóricamente actualizables deben poder ser actualizadas por el sistema.
- **Regla 7:** *Alto nivel de inserción, actualización y borrado.* El sistema debe permitir la manipulación de alto nivel en los datos, es decir, sobre conjuntos de tuplas. Esto significa que los datos no solo se pueden recuperar de una base de datos relacional a partir de filas múltiples y/o de tablas múltiples, sino que también pueden realizarse inserciones, actualización y borrados sobre varias tuplas y/o tablas al mismo tiempo y no solo sobre registros individuales.
- **Regla 8:** *Independencia física de los datos.* Los programas de aplicación y actividades del terminal permanecen inalterados a nivel lógico aunque realicen cambios en las representaciones de almacenamiento o métodos de acceso.
- **Regla 9:** *Independencia lógicas de los datos.* Los programas de aplicación y actividades del terminal permanecen inalterados a nivel lógico aunque se realicen cambios a las tablas base que preserven la información. La independencia de datos lógica es más difícil de lograr que la independencia física de datos.
- **Regla 10:** *Independencia de la integridad.* Las restricciones de integridad se deben especificar por separado de los programas de aplicación y almacenarse en la base de datos. Debe ser posible cambiar esas restricciones sin afectar innecesariamente a las aplicaciones existentes.
- **Regla 11:** *Independencia de la distribución.* La distribución de porciones de base de datos en distintas localizaciones debe ser invisible a los usuarios de la base de datos. Los usos existentes deben continuar funcionando con éxito:
1. Cuando una versión distribuida del SGBD se carga por primera vez
2. Cuando los datos existentes se redistribuyen en el sistema.
- **Regla 12:** *La regla de la no subversión.* Si el sistema proporciona una interfaz de bajo nivel de registro, aparte de una interfaz relacional, esa interfaz de bajo nivel no debe permitir su utilización para subvertir el sistema. Por ejemplo para sortear las reglas de seguridad relacional o las restricciones de integridad. Esto es debido a que a algunos sistemas no relacionales previamente existentes se les añadió una interfaz relacional pero, al mantener la interfaz nativa, seguía existiendo la posibilidad de trabajar no relacionalmente.

**Álgebra relacional**

Es un conjunto de operaciones que describen paso a paso cómo computar una respuesta sobre las relaciones, tal y como éstas son definidas en el modelo relacional. Denominada de tipo procedimental, a diferencia del Cálculo relacional que es de tipo declarativo.

Describe el aspecto de la manipulación de datos. Estas operaciones se usan como una representación intermedia de una consulta a una base de datos y, debido a sus propiedades algebraicas, sirven para obtener una versión más optimizada y eficiente de dicha consulta.

### Clase 4 *Entidades y atributos*

Principales elementos que vamos a manejar en el día a día a la hora de construir base de datos:

**Entidad**

![src/fundamentoBD_1.png](src/fundamentoBD_1.png)

Una entidad es algo similar a un objeto (programación orientada a objetos) que representa algo en el mundo real, incluso algo abstracto, que se le pueden extraer propiedades o atributos.

**Atributo**

![src/fundamentoBD_2.png](src/fundamentoBD_2.png)

Los atributos son las características o propiedades de una entidad. Cada uno de los elementos de la entidad poseen los mismos atributos y a cada atributo se le asigna un valor único por cada elemento.

**Tipos de atributos**

- **Atributos compuestos:** es un atributo que se puede subdividir en otros.
- **Atributos simples:** es aquel atributo que no se puede subdividir.
- **Atributos de un solo valor:** son los que pueden tener un único valor.
- **Atributos multivaluados:** son aquellos que pueden tener muchos valores.
- **Atributo derivado:** es aquel que se puede deducir de otro/s atributos/s mediante un algoritmo. Puesto que se puede calcular, no se guarda en la base de datos.
- **Dominio de un atributo:** es el conjunto de los posibles valores que ese atributo puede poseer.
- **Valor nulo de los atributos:** los atributos de una entidad-instancia pueden no tener ningún valor para algún atributo concreto. En estos casos, también se dice que el atributo tiene valor nulo.

**Atributos llaves**

![src/fundamentoBD_3.png](src/fundamentoBD_3.png)

Es un campo o una combinación de campos que identifica de forma única a cada fila de una tabla. Pueden ser:

- **Naturales:** son inherentes al objeto como el número de serie
- **Artificiales:** no es inherente al objeto y se asigna de manera arbitraria.

**Entidades Fuetes vs Entidades Débiles**

Una entidad fuerte es aquella que no necesita de otra entidad débil para existir. Una entidad débil es aquella que sí que necesita de otra para existir.

Por ejemplo, en una librería lo que realmente vende a los clientes no son libro, sino los ejemplares de ese libro que tiene la librería adquiridas. Las entidades débiles se representan mediante un doble rectángulo; es decir, un rectángulo con doble línea.

![src/fundamentoBD_4.png](src/fundamentoBD_4.png)

Existen dos tipos de dependencias en las entidades débiles:

- **Dependencia por existencia**

  Las ocurrencias de la entidad débil pueden identificarse mediante un atributo identificador clave sin necesidad de identificar la entidad fuerte relacionada.

  ![src/fundamentoBD_5.png](src/fundamentoBD_5.png)

- **Dependencia por identidad**

  La entidad débil no puede ser identificada sin la entidad fuerte relacionada.

  ![src/fundamentoBD_6.png](src/fundamentoBD_6.png)

### Clase 5 *Entidades de Platzi Blog*

Empezamos nuestro proyecto, el cual será un manejador de Blogpost.

**¿Por qué un manejador de Blogpost?**

En primer lugar porque la mayoría de nosotros estamos familiarizados con todos los conceptos y con el funcionamiento de un sistema de blogs. Y en segundo lugar, porque este sistema también nos provee de una serie de retos interesantes que vamos a tener que resolver en el curso y que seguramente te vas a encontrar en tu proyecto también, de esta manera vamos a ir poco a poco librando estos obstáculos y llegando a un resultado final coherente para que tú lo puedas hacer de igual manera con tu proyecto.

**Primer paso**

Debemos identificar las entidades.

- Posts
- Usuarios
- Comentarios
- Categorías

**Segundo paso**

Debemos pensar en los atributos. De hecho es inseparable pensar en los atributos y las entidades debido a que cuando se piensa en un objeto generalmente se nos viene a la cabeza lo que lo hace diferente o lo que lo hace un objeto.

- Posts:
  - Id
  - Título
  - Fecha de publicación
  - Contenido
  - Estatus
  - Etiquetas

- Usuarios
	- Id
	- Login
	- Password
	- Nickname
	- Email

- Comentarios
	- Id
	- Cuerpo del comentario

- Categorías
	- Id
	- Nombre de la categoría

### Clase 6 *Relaciones*

Las relaciones es la manera en que empezamos a ligar las diferentes entidades u objetos. Se representan mediante rombos y, por convención, se definen a través de verbos.

![src/fundamentoBD_7.png](src/fundamentoBD_7.png)

**Cardinalidad**

La cardinalidad es una restricción en una relación que especifica el número de instancias de entidad que una entidad específica puede estar relacionada a través de la relación

**Tipos de cardinalidad**

- **Cardinalidad: 1 a 1**

  En una relación de uno a uno, un registro de una tabla se asocia a uno y solo un registro de otra tabla. Por ejemplo, una persona solo puede tener un dato de contacto y un dato de contacto solo puede pertenecerle a una persona.

  ![src/fundamentoBD_8.png](src/fundamentoBD_8.png)

- **Cardinalidad: 0 a 1**

  Es una relación un opcional a uno, un registro de una tabla puede estar asociado a un solo registro de otra tabla. Por ejemplo, una sesión actual tiene un usuario pero un usuario no necesariamente puede estar en una sesión.

  ![src/fundamentoBD_9.png](src/fundamentoBD_9.png)

- **Cardinalidad: 1 a N**

  En una relación de uno a muchos, un registro de una tabla se puede asociar a uno o varios registros de otra tabla. Por ejemplo, una persona puede tener varios automóviles pero el automóvil solo le pertenece a una sola persona.

  ![src/fundamentoBD_10.png](src/fundamentoBD_10.png)

- **Cardinalidad: 0 a N**

  Es una relación un opcional a muchos, varios registros de una tabla puede estar asociado a uno o varios registros de otra tabla. Por ejemplo, un paciente pertenece a una habitación pero una habitación puede estar vacía o tener varios pacientes.

  ![src/fundamentoBD_11.png](src/fundamentoBD_11.png)

- **Cardinalidad: N a N**

  Esta relación la estaremos viendo en la siguiente clase.

### Clase 7 *Múltiples muchos*

Una relación de muchos a muchos se produce cuando varios registros de una tabla se asocian a varios registros de otra tabla. Por ejemplo, existe una relación de muchos a muchos entre los alumnos y las clases: los alumnos pueden pertenecer a varias clases y las clases pueden pertenecer a varios alumnos.

Por lo general, los sistemas de bases de datos relacionales no permiten implementar una relación directa de muchos a muchos entre dos tablas. Tenga en cuenta el ejemplo de seguimiento de facturas. Si había muchas facturas con el mismo número de factura y uno de sus clientes preguntó acerca de ese número de factura, no sabría a qué número se refería. Este es el motivo por el que se debe asignar un valor exclusivo a cada factura.

Para evitar este problema, puede dividir la relación de muchos a muchos en dos relaciones de uno a muchos mediante el uso de una tercera tabla denominada tabla de unión. Cada registro de una tabla de unión incluye un campo de coincidencia que contiene el valor de las claves principales de las dos tablas que se unen. En la tabla de unión, estos campos de coincidencia son claves externas. Estos campos de clave externa se rellenan con datos, ya que los registros de la tabla de unión se crean desde cualquiera de las tablas que se unen.

Siguiendo con el ejemplo de alumnos y clases, se incluye una tabla Alumnos, que contiene un registro para cada estudiante, y una tabla Clases, que contiene un registro para cada clase. Una tabla de unión, Matrículas, crea una relación de uno a muchos, una entre cada una de las dos tablas.

![src/fundamentoBD_12.png](src/fundamentoBD_12.png)

### Clase 8 *Diagrama ER*

Un diagrama entidad-relación es una herramienta para el modelado de datos que permite representar las entidades relevantes de un sistema de información así como sus interrelaciones y propiedades. Este modelo representa a la realidad a través de un esquema gráfico que ilustra cómo las entidades se relacionan entre sí dentro de un sistema. Son un reflejo de la estructura gramatical y emplean entidades como sustantivos y relaciones como verbos.

![src/fundamentoBD_13.png](src/fundamentoBD_13.png)

### Clase 9 *Diagrama Físico: tipos de datos y constraints*

Antes de llevar todo a la práctica debemos convertir nuestro diagrama a uno físico.

El diagrama físico representa como se construirá el modelo en la base de datos. Un modelo de base de datos física muestra todas las estructuras de tabla, incluidos el nombre de columna, el tipo de datos de columna, las restricciones de columna, la clave principal, la clave externa y las relaciones entre las tablas.

![src/fundamentoBD_14.png](src/fundamentoBD_14.png)

**Tipos de datos**

- **Texto**
  - **CHAR(n):** almacena datos de carácter en un campo de longitud fija. Los datos pueden ser una serie de letras, números y otros caracteres de un solo byte o varios bytes que pueden ser utilizados por el juego de códigos del entorno local de la base de datos.
  - **VARCHAR(n):** almacena series de caracteres de hasta 255 bytes en un campo de longitud variable. Los datos pueden consistir en letras, números y símbolos. CHARACTER VARYING se maneja exactamente igual que el tipo de datos VARCHAR.
  - **TEXT:** almacena cualquier clase de datos de texto. Las columnas TEXT suelen almacenar memorándums, capítulos de manuales, documentos comerciales, archivos de origen de programas y otros tipos de información de texto.
- **Número**
  - **INT o INTERGER:** almacena números enteros grandes. Un entero grande es un entero binario con una precisión de 31 bits. El rango oscila entre -2147483648 y +2147483647.
  - **BIGINT:** enteros muy grandes. Un entero muy grande es un entero binario con una precisión de 63 bits. El rango de los enteros muy grandes oscila entre -9223372036854775808 y +9223372036854775807.
  - **SMALLINT:** enteros pequeños. Un entero pequeño es un entero binario con una precisión de 15 bits. El rango oscila entre -32768 y +32767.
  - **DECIMAL(n, s):** permite almacenar números decimales empaquetados con una coma decimal implícita. La posición de la coma decimal la determinan la precisión y la escala del número. La escala, que es el número de dígitos en la parte de la fracción del número, no puede ser negativa ni mayor que la precisión. La precisión máxima es de 31 dígitos.
  - **NUMERIC(n, s):** sinónimo de decimal.
- **Fecha/hora**
	- **DATE:** almacena fechas, un valor de tres partes que representa un año, mes y día.
	- **TIME:** almacena horas, un valor de tres partes que representa las horas, minutos y segundos.
	- **DATETIME:** almacena una fecha del calendario combinada con las horas del día.
	- **TIMESTAMP:** una indicación de fecha y hora es un valor de siete partes que representa una fecha y hora mediante año, mes, día, hora, minuto, segundo y microsegundo.
- **Lógicos**
	- **BOOLEAN:** un campo puede almacenar true, false y null. El tipo de dato booleano no es SQL estándar.

**Constraints (Restricciones)**

- **NOT NULL:** Se asegura que la columna no tenga valores nulos.
- **UNIQUE:** Se asegura que cada valor en la columna no se repita.
- **PRIMARY KEY:** Es una combinación de NOT NULL y UNIQUE.
- **FOREIGN KEY:** Identifica de manera única una tupla en otra tabla.
- **CHECK:** Se asegura que el valor en la columna cumpla una condición dada.
- **DEFAULT:** Coloca un valor por defecto cuando no hay un valor especificado.
- **INDEX:** Se crea por columna para permitir búsquedas más rápidas.

### Clase 10 *Diagrama Físico: normalización*

El proceso de normalización de una base de datos relacional consiste en aplicar una serie de reglas para evitar a futuro realizar queries, o consultas innecesariamente complejas. En otras palabras están enfocadas en eliminar redundancias e inconsistencias de dependencia en el diseño de las tablas.

Las bases de datos se normalizan para:

- Evitar la redundancia de datos
- Proteger la integridad de los datos
- Evitar problemas de actualización de los datos en las tablas

Para poder decir que nuestra base de datos está normalizada deben respetarse 4 niveles de normalización.

Suponiendo que tenemos esta tabla que deseamos normalizar:

![src/fundamentoBD_15.png](src/fundamentoBD_15.png)

**Primera Forma Norma (1FN)**

Atributos atómicos, es decir, sin campos repetidos.

![src/fundamentoBD_16.png](src/fundamentoBD_16.png)

**Segunda forma normal (2FN)**

Cumple 1FN y cada campo de la tabla debe depender de una clave única.

![src/fundamentoBD_17.png](src/fundamentoBD_17.png)

**Tercera forma normal (3FN)**

Cumple con 1FN y 2FN, y los campos que NO son claves NO deben tener dependencias.

![src/fundamentoBD_18.png](src/fundamentoBD_18.png)

**Cuarta forma normal (4FN)**

Cumple 1FN, 2FN, 3FN, y los campos multivaluados se identifican por una clave única.

![src/fundamentoBD_19.png](src/fundamentoBD_19.png)

### Clase 11 *Diagrama Físico: normalizando Platziblog*

Ya que aprendimos a normalizar es hora de que lo apliquemos en nuestro proyecto de Platziblog.

**Diagrama Lógico**

![src/fundamentoBD_20.png](src/fundamentoBD_20.png)

**Diagrama Físico**

1. Generamos los campos de las diferentes entidades e identificamos las claves primarias y secundarias

  ![src/fundamentoBD_21.png](src/fundamentoBD_21.png)

2. Relacionamos las entidades

  ![src/fundamentoBD_22.png](src/fundamentoBD_22.png)

3. Si tenemos una relación muchos a muchos, como posts con etiquetas, debemos romper la relación y poner una tabla intermedia con las claves de unión entre ambas entidades.

  ![src/fundamentoBD_23.png](src/fundamentoBD_23.png)

### Clase 12 *Formas normales en DB relacionales*

La normalización en las bases de datos relacionales es uno de esos temas que, por un lado es sumamente importante y por el otro suena algo esotérico. Vamos a tratar de entender las formas normales (FN) de una manera simple para que puedas aplicarlas en tus proyectos profesionales.

**Primera Forma Normal (1FN)**

Esta FN nos ayuda a eliminar los valores repetidos y no atómicos dentro de una base de datos.

Formalmente, una tabla está en primera forma normal si:

- Todos los atributos son atómicos. Un atributo es atómico si los elementos del dominio son simples e indivisibles.
- No debe existir variación en el número de columnas.
- Los campos no clave deben identificarse por la clave (dependencia funcional).
- Debe existir una independencia del orden tanto de las filas como de las columnas; es decir, si los datos cambian de orden no deben cambiar sus significados.

Se traduce básicamente a que si tenemos campos compuestos como por ejemplo “nombre_completo” que en realidad contiene varios datos distintos, en este caso podría ser “nombre”, “apellido_paterno”, “apellido_materno”, etc.

También debemos asegurarnos que las columnas son las mismas para todos los registros, que no haya registros con columnas de más o de menos.

Todos los campos que no se consideran clave deben depender de manera única por el o los campos que si son clave.

Los campos deben ser tales que si reordenamos los registros o reordenamos las columnas, cada dato no pierda el significado.

**Segunda Forma Normal (2FN)**

Esta FN nos ayuda a diferenciar los datos en diversas entidades.

Formalmente, una tabla está en segunda forma normal si:

- Está en 1FN
- Sí los atributos que no forman parte de ninguna clave dependen de forma completa de la clave principal. Es decir, que no existen dependencias parciales.
- Todos los atributos que no son clave principal deben depender únicamente de la clave principal.

Lo anterior quiere decir que sí tenemos datos que pertenecen a diversas entidades, cada entidad debe tener un campo clave separado. Por ejemplo:

![src/fundamentoBD_24.png](src/fundamentoBD_24.png)

En la tabla anterior tenemos por lo menos dos entidades que debemos separar para que cada uno dependa de manera única de su campo llave o ID. En este caso las entidades son alumnos por un lado y materias por el otro. En el ejemplo anterior, quedaría de la siguiente manera:

![src/fundamentoBD_25.png](src/fundamentoBD_25.png)

**Tercera Forma Normal (3FN)**

Esta FN nos ayuda a separar conceptualmente las entidades que no son dependientes.

Formalmente, una tabla está en tercera forma normal si:

- Se encuentra en 2FN
- No existe ninguna dependencia funcional transitiva en los atributos que no son clave

Esta FN se traduce en que aquellos datos que no pertenecen a la entidad deben tener una independencia de las demás y debe tener un campo clave propio. Continuando con el ejemplo anterior, al aplicar la 3FN separamos la tabla alumnos ya que contiene datos de los cursos en ella quedando de la siguiente manera.

![src/fundamentoBD_26.png](src/fundamentoBD_26.png)

![src/fundamentoBD_27.png](src/fundamentoBD_27.png)

**Cuarta Forma Normal (4FN)**

Esta FN nos trata de atomizar los datos multivaluados de manera que no tengamos datos repetidos entre rows.

Formalmente, una tabla está en cuarta forma normal si:

- Se encuentra en 3FN
- Los campos multivaluados se identifican por una clave única

Esta FN trata de eliminar registros duplicados en una entidad, es decir que cada registro tenga un contenido único y de necesitar repetir la data en los resultados se realiza a través de claves foráneas.

Aplicado al ejemplo anterior la tabla materia se independiza y se relaciona con el alumno a través de una tabla transitiva o pivote, de tal manera que si cambiamos el nombre de la materia solamente hay que cambiarla una vez y se propagara a cualquier referencia que haya de ella.

![src/fundamentoBD_28.png](src/fundamentoBD_28.png)

![src/fundamentoBD_29.png](src/fundamentoBD_29.png)

De esta manera, aunque parezca que la información se multiplicó, en realidad la descompusimos o normalizamos de manera que a un sistema le sea fácil de reconocer y mantener la consistencia de los datos.

Algunos autores precisan una 5FN que hace referencia a que después de realizar esta normalización a través de uniones (JOIN) permita regresar a la data original de la cual partió.

## Modulo 3. RDBMS (MySQL) o cómo hacer lo anterior de manera práctica
### Clase 13 *RDB ¿Qué?*

RDBMS (Relational Database Management System o Sistema Gestor de Bases de Datos Relacionales) se trata de software capaz de producir, manipular y gestionar bases de datos de tipo relacional. Es un software que se antepone a los datos de una base de datos, de modo que cualquier acceso a los datos pasa por una petición al RDBMS que éste gestiona a fin de realizar la operación más conveniente sobre esa petición. Los sistemas de base de datos relacionales son aquellos que almacenan y administran de manera lógica los datos en forma de tablas.

Hay diferentes tipos de manejadores de base de datos relaciones como Oracle, MySQL o PostgreSQL. Todos son muy parecidas, porque internamente manejan el mismo lenguaje, pero cada una tiene un estilo diferente.

### Clase 14 *Instalación local de un RDBMS (Windows)*

Hay dos maneras de acceder a manejadores de bases de datos:
- Instalar en máquina local un administrador de bases relacional (recomendada si comienzas a experimentar y hacer ejercicios).
- Tener ambientes de desarrollo especiales o servicios cloud (usada en empresas).

En este curso usaremos MySQL porque tiene un impacto histórico siendo muy utilizado y además es software libre y gratuito. La versión 5.6.43 es compatible con la mayoría de aplicaciones y frameworks.
- Root es el usuario principal que tendrá todos los permisos y por lo tanto en ambientes de producción hay que tener mucho cuidado al configurarlo.

**Instalación**

Primero vamos a la página de descargas: https://dev.mysql.com/downloads/windows/installer/5.6.html

![src/fundamentoBD_30.png](src/fundamentoBD_30.png)

Es un instalador que tiene varias herramientas que nos ayudaran a hacer más visual las operaciones con la base de datos, como los conectores.

Tenemos un panel en la que podemos seleccionar la versión de la base de datos (nosotros elegimos la 5.6), otro panel en donde elegimos el sistema operativo (Microsoft Windows) y tenemos dos opciones de instaladores: uno es el instalador de versión web y otro el instalador completo. El instalador web nos baja un instalador muy pequeño y cada que queramos instalar algo va nuevamente a la web para instalarlo, y el instalador completo trae todo para ahorrarnos la parte tediosa de descargar e instalar.

Damos click a Download y nos envía a otra página. Pequeño tic: MySQL busca que te registres, no te cobra nada pero sirve para pertenecer a la comunidad por lo que primero que te resaltan son los botones de Login y Sign Up, pero hasta abajo esta un pequeño link de 'no gracias, solo quiero la descarga', damos click y nos descarga.

![src/fundamentoBD_31.png](src/fundamentoBD_31.png)

Vamos a la carpeta donde está el instalador descargado, damos doble click o click derecho y ejecutar como administrador para que comience la instalación. El programa nos va a pedir algunos permisos, probablemente porque va hacer cambios al sistema operativo y va a usar recursos de sistema entonces nos pide acceso a permisos especiales:

![src/fundamentoBD_32.png](src/fundamentoBD_32.png)

Decimos si y se instala los componentes:

![src/fundamentoBD_33.png](src/fundamentoBD_33.png)

Para continuar nos pide nuevamente permisos, aceptamos, y luego nos abre la ventana del instalador. La primera ventana, como es costumbre, es la licencia bajo el cual se distribuye el programa. Damos click en Aceptar y después Next para continuar:

![src/fundamentoBD_34.png](src/fundamentoBD_34.png)

Ahora se nos presenta diferentes tipos de instalación. El primero es una instalación para desarrolladores, el segundo solamente para servidor, el tercero solamente para clientes, el cuarto es completa y el quinto es para hacer nosotros mismos la configuración. Es el último el cual aceptamos porque dentro del paquete existe muchos componentes que no vamos a utilizar, seleccionamos y damos click en Next:

![src/fundamentoBD_35.png](src/fundamentoBD_35.png)

Posteriormente nos apareces las opciones de lo que podemos instalar, tenemos el servidor de MySQL, aplicaciones, conectores que nos ayudara cuando desarrollemos una aplicación para que el lenguaje se comunique con la base de datos, ejemplos y documentación. Lo que instalaremos serán MySQL Server y MySQL Workbrench, seleccionamos y damos click a Next:

![src/fundamentoBD_36.png](src/fundamentoBD_36.png)

Nos muestra una ventana que nos dice que los dos componentes están listos para la instalación, algunas veces pueden pedir dependencias adicionales sobre todo del framework de Windows para Visual Studio no pasa siempre, pero llega a pedir. En este momento nos indica que está listo para instalar, así que damos click en Ejecutar:

![src/fundamentoBD_37.png](src/fundamentoBD_37.png)

Ya terminado de instalar ambos programas, damos click al botón Next y nos sale una ventaja que notifica que el servidor ya está listo para configurar. Nuevamente damos click en Next:

![src/fundamentoBD_38.png](src/fundamentoBD_38.png)

Y nos sale una ventana que nos da la configuración inicial del servidor, esto es una configuración bastante sencilla y lo único que nos pide es saber el tipo de configuración que deseamos (desarrollo, servidor o solamente dedicada a la base de datos). Elegimos una computadora para desarrollo que nos permite hacer experimentos sin ninguna consecuencia, nos indica el puerto en donde será instalado, damos click a Next con las opciones default tenemos suficiente:

![src/fundamentoBD_39.png](src/fundamentoBD_39.png)

La siguiente ventana nos pide la cuenta o roles. Damos click a la contraseña de Root (root es nuestro usuario principal y tiene todos los permisos, es por el que tenemos que tener más cuidado. En un ambiente de prueba no es nada, pero si en un ambiente de producción porque si alguien hackea este usuario va a tener accesos a todos los datos), ponemos una contraseña -no te olvides porque lo usaran en todo momento-, damos click en Next:

![src/fundamentoBD_40.png](src/fundamentoBD_40.png)

En la siguiente ventana nos pregunta si queremos configurarlo como servicio para que corra en segundo plano dentro de Windows y si deseamos que inicie cada vez que iniciemos la computadora. Elige como lo deseas:

![src/fundamentoBD_41.png](src/fundamentoBD_41.png)

En la proxima ventana tenemos un check list, una lista que nos corre una vez que demos ejecutar para ver los pasos del instalador:

![src/fundamentoBD_42.png](src/fundamentoBD_42.png)

Una vez finalizada, si existio algun error podemos ir a Log y ver lo que debemos corregir. En este caso todo salio bien y damos en Finish:

![src/fundamentoBD_43.png](src/fundamentoBD_43.png)

Con la configuración completa volvemos a esta ventana. Damos click en Next:

![src/fundamentoBD_44.png](src/fundamentoBD_44.png)

Y nos sale una ventana que nos dice que toda la instalación (tanto servidor como cliente visual) ya está completa. Con esto la instalación finaliza:

![src/fundamentoBD_45.png](src/fundamentoBD_45.png)

### Clase 15 *Instalación local de un RDBMS (Mac)*

**Instalación de un RDBMS en Mac OS**

Vamos a la página para descargar el servidor de comunidad de MySQL: https://dev.mysql.com/downloads/mysql/5.7.html

![src/fundamentoBD_46.png](src/fundamentoBD_46.png)

Al igual que la instalación de Windows, nos pide que seamos parte de la comunidad. Damos click en 'no gracias, solo quiero la descarga':

![src/fundamentoBD_47.png](src/fundamentoBD_47.png)

Una vez que termino de descargarse, nos dirigimos a nuestra carpeta de descarga y damos doble click al archivo DMG para iniciar la instalación. Click al archivo pkg y nos abre la pantalla de bienvenida en donde nos da las gracias por escogerlo y nos explica un poco lo que vamos a instalar, damos click al botón continuar:

![src/fundamentoBD_48.png](src/fundamentoBD_48.png)

Se nos presenta la licencia. Es una licencia GNU o GPL que es precisamente para código abierto, damos click en continuar:

![src/fundamentoBD_49.png](src/fundamentoBD_49.png)

Nos salta una ventana en donde nos pregunta si estamos aceptando la licencia, damos click en acepto:

![src/fundamentoBD_50.png](src/fundamentoBD_50.png)

Esta ventana nos indica el espacio que va ocupar y si deseamos cambiar la ubicación de la instalación, en este caso no hacemos nada, y damos continuar:

![src/fundamentoBD_51.png](src/fundamentoBD_51.png)

Nos sale una ventana que nos pide la clave de acceso al administrador, si seguiste los pasos del tutorial correctamente no deberías tener ninguna aprensión, este es normalmente el proceso y es un software legítimo. Una vez ingresada la clave del administrador, damos click en instalar software:

![src/fundamentoBD_52.png](src/fundamentoBD_52.png)

Se empieza a hacer la instalación como tal:

![src/fundamentoBD_53.png](src/fundamentoBD_53.png)

Nuevamente nos pide permiso del sistema, algo de esperarse pues utilizara el disco duro y algunos otros recursos, así que damos click en ok:

![src/fundamentoBD_54.png](src/fundamentoBD_54.png)

La instalación finaliza con una ventana que nos muestra la contraseña y usuario root, también nos indica que podemos cambiar la contraseña después. Puedes copiar la contraseña para que después puedas acceder a la base de datos, y damos click en ok:

![src/fundamentoBD_55.png](src/fundamentoBD_55.png)

Con esto terminamos de instalar el servidor de MySQL y termina el instalador. Damos click en cerrar:

![src/fundamentoBD_56.png](src/fundamentoBD_56.png)

Una última ventana nos pregunta si deseamos conservar el archivo de instalación o directamente lo envias al basurero, das click al que desees realizar:

![src/fundamentoBD_57.png](src/fundamentoBD_57.png)

**MySQL Workbench**

Como parte de la instalación, ya tenemos el servidor pero necesitamos algo que se conecte a él y nos permita administrar la base de datos de una forma más visual. Para esto, la misma gente de MySQL que son Oracle nos presenta la herramienta Workbench (en Windows viene todo junto, pero en Mac es diferente) así que bajamos esta herramienta por separado.

Vemos una página muy similar a la anterior, elegimos el sistema operativo y damos click en descargar: https://dev.mysql.com/downloads/workbench/

![src/fundamentoBD_58.png](src/fundamentoBD_58.png)

Nos presenta la misma página para registrarnos o iniciar sesión, damos click en 'no gracias, solo quiero la descarga'. Nuevamente nos vamos a la carpeta y damos doble click al instalador, y nos muestra esta ventana de avance que instala todos los componentes del Workbench:

![src/fundamentoBD_59.png](src/fundamentoBD_59.png)

Una vez finalizada nos sale una pantalla en donde lo unico que debemos hacer es dar click al icono del MySQL Workbench y arrastar hasta la carpeta:

![src/fundamentoBD_60.png](src/fundamentoBD_60.png)

Una vez arrastrado nos sale una pantalla que nos muestra el progreso de copiar la aplicación:

![src/fundamentoBD_61.png](src/fundamentoBD_61.png)

Una vez finalizada, cerramos todo y ya está. Tenemos instalado MySQL en Mac.

**Nota: Es importante guardar la información que te da al instalar el servidor (usuario y contraseña) porque lo ocupamos más adelante cuando deseamos configurar Workbench para conectarse a nuestro servidor de base de datos.**

### Clase 16 *Instalación local de un RDBMS (Ubuntu)*

Visita la dirección de descarga de la versión de comunidad de MySql: https://dev.mysql.com/downloads/mysql/5.7.html#downloads

Dirígete a la sección de selección de descargas y selecciona tu distribución de Linux. En nuestro caso Ubuntu y selecciona posteriormente la versión que estás utilizando actualmente, en nuestro caso 18.04 de 64 bits.

![src/fundamentoBD_62.png](src/fundamentoBD_62.png)

Más abajo encontrarás las diferentes opciones de descarga existen diversos paquetes dependiendo tus necesidades. En el caso del ejemplo usaremos la versión deb bundle. Da click en el botón Download seleccionado.

![src/fundamentoBD_63.png](src/fundamentoBD_63.png)

En la siguiente pantalla nos piden que nos registremos o iniciemos sesión, pero ya que solo queremos la descarga daremos click en el link que se encuentre en la parte de abajo.

![src/fundamentoBD_64.png](src/fundamentoBD_64.png)

Espera a que la descarga concluya.

Al terminar abre el archivo .tar con el desempaquetador de tu preferencia.

![src/fundamentoBD_65.png](src/fundamentoBD_65.png)

Extrae el contenido en la carpeta de tu preferencia.

![src/fundamentoBD_66.png](src/fundamentoBD_66.png)

Selecciona el archivo de servidor de comunidad y ábrelo con tu manejador de paquetes instalado.

![src/fundamentoBD_67.png](src/fundamentoBD_67.png)

![src/fundamentoBD_68.png](src/fundamentoBD_68.png)

Da click en instalar.

Finalmente puedes ir a la consola o terminal de Ubuntu y escribir el siguiente comando: ***sudo mysql***

![src/fundamentoBD_69.png](src/fundamentoBD_69.png)

A continuación deberá aparecer una ventana con el prompt de mysql donde ya puedes comenzar a ejecutar los comandos de las lecciones.

![src/fundamentoBD_70.png](src/fundamentoBD_70.png)

***Nota***

***- Recuerda estar seguro que las dependencias para el paquete se cumplen para instalar.***

***- Muchas veces las distribuciones ya cuentan con paquetes en su repositorio, en ese caso también puedes ejecutar el comando: sudo apt-get install mysql-server***

### Clase 17 *Clientes gráficos*

Como parte de las herramientas que nos da MySQL como desarrolladores tenemos algunas herramientas bastante interesantes, como MySQL Workbench.

**¿Qué es MySQL Workbench?**

Básicamente es un tipo de herramienta llamada «cliente gráfico», el cual es una forma muy gráfica de representar y de ver cómo funciona nuestra base de datos internamente. Y es que la forma de abstraer los datos de base de datos y que nosotros lo podamos entender de una manera más simple.

Este tipo de herramienta nos permite visualizar y modificar los datos, y jugar un poco con la configuración de la base de datos de una forma bastante más amigable.

Existen varias opciones para clientes gráficos y hay algunas, dependiendo del manejador de base de datos que utilices, hay diversas más famosas.

**MySQL Workbench**

Abrimos el programa y nos sale esta pantalla de bienvenida, entre las conexiones tenemos una por default (Local instance MySQL80):

![src/fundamentoBD_71.png](src/fundamentoBD_71.png)

Si queremos agregar una nueva conexión a la base de datos con la configuración que tienes, simplemente das click en el botón de más y nos sale una ventana que nos pide los datos para la conexión:

![src/fundamentoBD_72.png](src/fundamentoBD_72.png)

Damos doble click sobre la instancia local para usar el editor visual, antes de poder usarlo nos sale una pantalla que pide la contraseña configurada anteriormente durante la instalación:

![src/fundamentoBD_73.png](src/fundamentoBD_73.png)

Editor visual

![src/fundamentoBD_74.png](src/fundamentoBD_74.png)

### Clase 18 *Servicios administrados*

Hoy en día muchas empresas ya no tienen instalados en sus servidores los RDBMS sino que los contratan a otras personas. Estos servicios administrados cloud te permiten concentrarte en la base de datos y no en su administración y actualización.

Los servicios vienen en una variedad de sabores, algunos muy famosos como AWS de Amazon, Google Cloud Platform de Google o Azure de Microsoft.

## Modulo 4. SQL hasta en la sopa
### Clase 19 *Historia de SQL*

SQL (Structured Query Language o Lenguaje de Consultas Estructurada) es un lenguaje de programación diseñado para almacenar, manipular y recuperar datos almacenados en bases de datos relacionales.

La primera encarnación de SQL apareció en 1974, cuando un grupo de IBM desarrolló el primer prototipo de una base de datos relacional. Se trataba de hacer consultar a los datos, pero no existía una forma realmente estandarizada de hacerlo, entonces, SQL aparece con el objetivo hacer un solo lenguaje de consulta sin importar que manejador de base datos es utilizada, trata de unificarlo todo y se vuelve un gran estándar.

Fue Relational Software (luego se convirtió en Oracle) quien lanzó la primera base de datos relacional comercial.

Existen estándares para SQL. Sin embargo, el SQL que puede utilizarse en cada uno de las principales RDBMS actuales viene en distintas formas. Esto se debe a dos razones:

1. El estándar SQL es bastante complejo, y no es práctico implementar el estándar completo
2. Cada proveedor de base de datos necesita una forma de diferenciar su producto de otros.

La función para unificar todo se debe a que antes se trataba de consultar archivos de texto y cada compañía tenía su RDBMS, pero no sabía comunicarse entre ellos y el tratar de programarlo llegaba a ser tedioso y desgastante, entonces, se crea el SQL como una manera de manejar mejor esa situación.

Su nombre Structured Query Language se debe a que está estructurado y eso es una de las características más importantes de SQL es su estructura clara y fija.

**NoSQL**

Ahora existen algo llamado NoSQL y mucha gente cree que se refiere a no utilizar SQL, pero no es así.

NoSQL (No only SQL o No solo SQL) está diseñada específicamente para modelos de datos específicos y tienen esquemas flexibles para crear aplicaciones modernas. Las bases de datos NoSQL son ampliamente reconocidas porque son fáciles de desarrollar, por su funcionalidad y el rendimiento a escala.

Algunas de las base de datos NoSQL más reconocidas son:

- MongoDB
- Cassandra
- Neo4j
- BigQuery

### Clase 20 *DDL create*

SQL tiene dos grandes sub lenguajes, el que veremos ahora será:

DDL (Data Definition Language o Lenguaje de Definición de Datos) es un lenguaje proporcionado por el sistema de gestión de base de datos que permite a los programadores de la misma llevar a cabo las tareas de definición de las estructuras que almacenarán los datos así como de los procedimientos o funciones que permitan consultarlos.

Un DDL es un lenguaje de programación para definir una estructura de datos. El término DDL fue introducido por primera vez en relación con el modelo de base de datos CODASYL, donde el esquema de la base de datos ha sido escrito en un lenguaje de descripción de datos que describe los registros, los campos, y "conjuntos" que conforman el usuario modelo de datos. Más tarde fue usado para referirse a un subconjunto de SQL, pero ahora se utiliza en un sentido genérico para referirse a cualquier lenguaje formal para describir datos o estructuras de información, como los esquemas XML.

A diferencia de muchos lenguajes de descripción de datos, SQL utiliza una acción de versos imperativo cuyo efecto es modificar el esquema de la base de datos, añadiendo, cambiando o eliminando las declaraciones se pueden mezclar libremente con otras sentencias SQL, por lo que el DDL no es realmente una lengua independiente. La declaración más común es CREATE TABLE. El lenguaje de consulta SQL, el más difundido entre los gestores de bases de datos, admite las siguientes sentencias de definición: CREATE, DROP y ALTER, cada una de las cuales se puede aplicar a las tablas, vistas, procedimientos almacenados y triggers de la base de datos.

**CREATE**

Sirve para crear una nueva base de datos, tabla, vista, índice, etc.

![src/fundamentoBD_75.png](src/fundamentoBD_75.png)

Un comando CREATE común es la de CREATE TABLE (Crear Tabla)

![src/fundamentoBD_76.png](src/fundamentoBD_76.png)

### Clase 21 *CREATE VIEW y DDL ALTER*

**CREATE VIEW**

Un vista es una consulta que se presenta como una tabla (virtual) a partir de un conjunto de tablas en una base de datos relacional.

Las vistas tienen la misma estructura que una tabla: filas y columnas. La única diferencia es que sólo se almacena de ellas la definición, no los datos. Los datos que se recuperan mediante una consulta a una vista se presentarán igual que los de una tabla. De hecho, si no se sabe que se está trabajando con una vista, nada hace suponer que es así. Al igual que sucede con una tabla, se pueden insertar, actualizar, borrar y seleccionar datos en una vista. Aunque siempre es posible seleccionar datos de una vista, en algunas condiciones existen restricciones para realizar el resto de las operaciones sobre vistas.

![src/fundamentoBD_77.png](src/fundamentoBD_77.png)

**ALTER**

La sentencia ALTER TABLE es usada para agregar, borrar o modificar columnas en una tabla existente.

![src/fundamentoBD_78.png](src/fundamentoBD_78.png)

### Clase 22 *DDL drop*

**DROP**

Sirve para borrar en forma sencilla distintos objetos dentro de la base de datos como por ejemplo base de datos, tablas, índices.

Para eliminar una tabla de una base de datos tenemos la sentencia DROP TABLE. Con ella quitamos una o varias definiciones de tabla y todos los datos, índices, desencadenadores, restricciones y especificaciones de permisos que tengan esas tablas. Las vistas o procedimientos almacenados que hagan referencia a la tabla quitada se deben quitar explícitamente con DROP VIEW o DROP PROCEDURE.

![src/fundamentoBD_79.png](src/fundamentoBD_79.png)

### Clase 23 *DML*

DML (Data Manipulation Language o Lenguaje de Manipulación de Datos) es un lenguaje proporcionado por los sistemas gestores de bases de datos que permite a los usuarios de la misma llevar a cabo las tareas de consulta o modificación de los datos contenidos en las bases de datos.

El lenguaje de manipulación de datos más popular hoy en día es SQL, usado para recuperar y manipular datos en una base de datos relacional. Otros ejemplos de DML son los usados por bases de datos IMS/DL1, CODASYL u otras.

**Sentencias**

- INSERT

	La estructura básica para la sentencia insert utilizando el estándar de SQL es la siguiente:

  ![src/fundamentoBD_80.png](src/fundamentoBD_80.png)

	Tomando como ejemplo si se tuviera una tabla llamada 'people' con los campos de tipo cadena de caracteres (last_name, first_name, address, city), donde se inserta los valores que se encuentran en después de la palabra values, los valores se insertan en el orden correspondiente a como se hizo la llamada de los campos, los valores van separados por comas, las comillas dobles indican que se está insertando datos de tipo cadena de caracteres.

- UPDATE

	Para modificar uno o varios datos de uno o varios registros utilizamos "update" (actualizar).

	Por ejemplo, en nuestra tabla people, queremos cambiar los valores del campo last_name por el valor 'Chávez' y del campo city por 'Mérida', utilizamos la condición "where" para que afecte solamente a ese registro:

  ![src/fundamentoBD_81.png](src/fundamentoBD_81.png)

	Utilizamos "update" junto al nombre de la tabla y "set" junto con el campo a modificar y su nuevo valor.

	Otro ejemplo sería:

  ![src/fundamentoBD_82.png](src/fundamentoBD_82.png)

	Esto nos dice que de nuestra tabla people todos los valores del campo first_name serán cambiados a 'Juan', con la condición "where" señalamos a que afecte únicamente a aquellos de la ciudad de Mérida.

	Para que el cambio afecte a todos son registros sin discriminar usamos:

  ![src/fundamentoBD_83.png](src/fundamentoBD_83.png)

- DELETE

	Para eliminar los registros de una tabla usamos el comando "delete":

  ![src/fundamentoBD_84.png](src/fundamentoBD_84.png)

	La ejecución del comando indicado en la línea anterior borra TODOS los registros de la tabla.

	Si queremos eliminar uno o varios registros debemos indicar cuál o cuáles, para ello utilizamos el comando "delete" junto con la cláusula "where" con la cual establecemos la condición que deben cumplir los registros a borrar. Por ejemplo, queremos eliminar aquel registro cuyo id sea 1:

  ![src/fundamentoBD_85.png](src/fundamentoBD_85.png)

	Si solicitamos el borrado de un registro que no existe, es decir, ningún registro cumple con la condición especificada, no se borrarán registros, pues no encontró registros con ese dato.

- SELECT

	La sintaxis básica de select es la siguiente utilizando el estándar de SQL:

  ![src/fundamentoBD_86.png](src/fundamentoBD_86.png)

	Donde en SELECT ponemos primero las columnas que deseamos consultar y en FROM ponemos el nombre de la tabla que contiene el campo mencionado.

	Si deseamos traer TODOS los registros de una tabla usamos: ***SELECT * FROM people;***


### Clase 24 *¿Qué tan standard es SQL?*

La utilidad más grande de SQL fue unificar la forma en la que pensamos y hacemos preguntas a un repositorio de datos. Ahora que nacen nuevas bases de datos igualmente siguen tomando elementos de SQL.

### Clase 25 *Creando Platziblog: tablas independientes*

![src/fundamentoBD_87.png](src/fundamentoBD_87.png)

1. Creamos la base de datos platziblog
2. Creamos las tablas sin llave foránea:
  - Categoría
  - Etiquetas
  - Usuarios

**Recomendaciones:**

- Una buena práctica es comenzar creando las entidades que no tienen una llave foránea.
- Generalmente en los nombres de bases de datos se evita usar eñes o acentos para evitar problemas en los manejadores de las bases de datos.


### Clase 26 *Creando Platziblog: tablas dependientes*

![src/fundamentoBD_87.png](src/fundamentoBD_87.png)

Ya que creamos nuevas tablas independientes es hora de crear el resto de base de datos, pero debemos tener cuidado en el orden en que son creadas.

1. Creamos la tabla posts
2. La unimos a las tablas categorías y usuarios.

**Nota:**
- El comando "cascade" sirve para que cada que se haga un update en la tabla principal, se refleje también en la tabla en la que estamos creando la relación.


### Clase 27 *Creando Platziblog: tablas transitivas*

![src/fundamentoBD_87.png](src/fundamentoBD_87.png)

1. Creamos la tabla comentarios.
2. Unimos la tabla comentarios con usuario.
3. Creamos la tabla transitiva posts_etiquetas.
4. Unimos la tabla posts_etiquetas con las tablas posts y etiquetas.
5. Hacemos el Reverse Engineer.

**Nota:**

- Las tablas transitivas sirven como puente para unir dos tablas. No tienen contenido semántico.
- Reverse Engineer nos reproduce el esquema del cual nos basamos para crear nuestras tablas. Es útil cuando llegas a un nuevo trabajo y quieres entender cuál fue la mentalidad que tuvieron al momento de crear las bases de datos.

## Modulo 5. Consultas a una base de datos
### Clase 28 *¿Por qué las consultas son tan importantes?*

Las consultas o queries a una base de datos son una parte fundamental ya que esto podría salvar un negocio o empresa.

Alrededor de las consultas a las bases de datos se han creado varias especialidades como ETL o transformación de datos, business intelligence e incluso machine learning.

### Clase 29 *Estructura básica de un Query*

Los queries son la forma en la que estructuramos las preguntas que le vamos hacer a la base de datos. Nos ayuda a transformar una pregunta o duda en sintaxis para sea entendida por la base de datos.

La estructura de un querie puede ser tan simple como quieran y tan compleja como se pueda, hay muchas formas de hacer queries pero vamos a empezar por la estructura más básica y poco a poco subiremos la escala, viendo todas las opciones que tenemos para hacer preguntas cada vez más complejas.

**Estructura Básica**

El query tiene básicamente 2 partes, la sentencia SELECT y la sentencia FROM, en la mayoría de las veces también puedes encontrar una tercera sentencia, WHERE.

![src/fundamentoBD_88.png](src/fundamentoBD_88.png)

- SELECT: Campos que deseamos obtener.
- FROM: Tabla de donde se extraerá los datos.
- WHERE: Condición que debe cumplir los registros de la tabla seleccionada.
- GROUP BY: Agrupa los campos que tienen el mismo valor.
- ORDER BY: Especifica la orden en que se desea recuperar los datos.
- HAVIGN: Condición que debe cumplir un grupo de registros.

**Ejemplos**

Selecciona todos los campos de la tabla posts:

> SELECT *
>
> FROM posts;

Selecciona todos los campos de la tabla posts, pero únicamente si fueron publicados después del 2024:

> SELECT *
>
> FROM posts
>
> WHERE fecha_publicacion > '2024';

Selecciona todos los campos de la tabla posts, pero únicamente si fueron publicados antes del 2024:

> SELECT *
>
> FROM posts
>
> WHERE fecha_publicacion < '2024';


**NOTA:** El asterisco (*) funciona para seleccionar todos los campos de una tabla.

### Clase 30 *SELECT*

La primera parte de la estructura que necesitamos tener para generar preguntas a una base de datos es la sentencia SELECT.

SELECT se utiliza para recuperar información de la base de datos, y puede proyectar las columnas seleccionadas, es decir, realizar un filtro sobre la tabla o tablas originales y recuperar solamente datos de las columnas filtradas. También puede seleccionar, es decir, filtrar los registros según varios criterios, o realizar uniones, que recopilan datos de diferentes tablas a través de una relación entre ellas.

**Ejemplo**

Trae todos los campos de la tabla posts:

> SELECT *
>
> FROM posts;

Trae los campos seleccionados (título, fecha de publicación y estatus) de la tabla posts:

> SELECT titulo, fecha_publicacion, estatus
>
> FROM posts;

Para renombrar la cabecera de una columna usamos AS:

> SELECT titulo AS encabezado, fecha_publicacion AS publicado_en, estatus AS estado
>
> FROM posts;

Si deseamos saber el número de filas, es decir, la cantidad de registros que tiene una tabla usamos COUNT:

> SELECT COUNT (*)
>
> FROM posts;

También puede ser renombrado por la función AS:

> SELECT COUNT (*) AS numero_posts
>
> FROM posts;

### Clase 31 *FROM*

La segunda parte de la estructura que necesitamos tener para generar preguntas a una base de datos es la sentencia FROM.

**¿Por qué es importante?**

Es una de las sentencias más interesantes y poderosas a la hora de hacer un query, y esto tiene que ver con que FROM indica de donde debemos que traer los datos.

Hasta ahora hemos seleccionado todos los campos de una tabla X, pero la parte interesante viene cuando deseamos unir tablas. En normalización vimos como la información de nuestra base de datos fueron distribuidos en diferentes tablas, pero a la hora de presentar un informe o traer datos que sea valiosa nosotros requerimos volver a juntar nuevamente esa información, como compañero de FROM tenemos a la sentencia JOIN que quiere decir justamente unir o juntar tablas.

**Diagramas de Venn**

Son círculos que se tocan en algún punto para ver dónde está la intersección de conjuntos. Ayudan mucho para poder formular la sentencia JOIN de la manera adecuada dependiendo del query que se quiere hacer.

**Ejemplo:** Supongamos que deseamos extraer ciertos datos de la tabla A y la tabla B, para eso usamos JOIN

![src/fundamentoBD_89.png](src/fundamentoBD_89.png)

- LEFT JOIN: Si deseamos saber los datos de la tabla A, sin importar que estén o no en la tabla B.
- LEFT JOIN (con condición): Deseamos saber los datos que están únicamente en la tabla A (excluimos a la tabla B).
- RIGHT JOIN: Si deseamos saber los datos de la tabla B, sin importar que estén o no en la tabla A.
- RIGHT JOIN (con condición): Deseamos saber los datos que están únicamente en la tabla B (excluimos a la tabla A).

![src/fundamentoBD_90.png](src/fundamentoBD_90.png)

- INNER JOIN: Si deseamos saber únicamente los datos que estén en ambas tablas.
- OUTER JOIN: Si deseamos traer los datos de ambas tablas, sin excepciones.
- OUTER JOIN (con condición): Si deseamos traer los datos que estén en la tabla A o en la tabla B, pero que no compartan relación la una con la otra.

### Clase 32 *Utilizando la sentencia FROM*
1. **LEFT JOIN**

	Trae todos los usuarios sin importar que tengan o no posts asociados, y después vemos los posts asociados a ese usuario.

	> SELECT *
  >
  > FROM usuarios
  >
  >  LEFT JOIN posts ON usuarios.id = posts.usuario_id;

2. **LEFT JOIN (con condición)**

	Trae todos los usuarios que NO tengan posts asociados.

  > SELECT *
  >
  > FROM usuarios
  >
  > LEFT JOIN posts ON usuarios.id = posts.usuario_id
  >
  > WHERE posts.usuario_id IS NULL;

3. **RIGHT JOIN**

	Trae todos los posts sin importar que tengan o no usuarios asociados, y después vemos los usuarios asociados a ese posts.

  > SELECT *
  >
  > FROM usuarios
  >
  > RIGHT JOIN posts ON usuarios.id = posts.usuario_id;

4. **RIGHT JOIN (con condición)**

  Trae los posts que no están relacionados a un usuario.

  > SELECT *
  >
  > FROM usuarios
  >
  > RIGHT JOIN posts ON usuarios.id = posts.usuario_id
  >
  > WHERE posts.usuario_id IS NULL;

5. **INNER JOIN**

  Trae los que tienen dependencia de ambos lados, o sea que deja de lados los usuarios que no tengan posts asociados o los posts que quedaron huérfanos.

  > SELECT *
  >
	> FROM usuarios
  >
  > INNER JOIN posts ON usuarios.id = posts.usuario_id;

6. **OTHER JOIN**

  Usada para traer el total de la unión de ambas tablas, tanto con los usuarios sin posts y con los posts sin usuarios. Pero existe un dato interesante y es que tiene dos formas, la primera no está incorporada por todos los manejadores de base de datos y es:

  > SELECT *
  >
  > FROM usuarios
  >
  > FULL OTER JOIN posts ON usuarios.id = posts.usuario_id;

	La segunda es la otra forma estándar que si funciona en todos los manejadores de base de datos.

	> SELECT *
  >
  > FROM usuarios
  >
  > LEFT JOIN posts ON usuarios.id = posts.usuario_id
  >
  > UNION
  >
  > SELECT *
  >
  > FROM usuarios
  >
  > RIGHT JOIN posts ON usuarios.id = posts.usuario_id;

7. **OTHER JOIN (con condición)**

  Trae todos los usuarios sin posts asociados y los posts huérfanos que no tienen usuarios relacionados.

  > SELECT *
  >
  > FROM usuarios
  >
  > LEFT JOIN posts ON usuarios.id = posts.usuario_id
  >
  > WHERE posts.usuario_id IS NULL
  >
  > UNION
  >
  > SELECT *
  >
  > FROM usuarios
  >
  > RIGHT JOIN posts ON usuarios.id = posts.usuario_id
  >
  > WHERE posts.usuario_id IS NULL;

### Clase 33 *WHERE*

WHERE es la sentencia que nos ayuda a filtrar tuplas o registros, permite filtrar los datos que queremos mostrar dependiendo de las características que elegimos. Empezaremos a filtrar los datos que nos interesa, no en sentido de que campo mostramos pero si de acuerdo a criterios como una fecha o cantidad.

**Ejemplo**

Trae todos los posts cuyo id sea menor a 50 (sin incluirlo)

> SELECT *
>
> FROM posts
>
> WHERE id < 50;

Trae todos los posts cuyo id sea menor o igual a 50

> SELECT *
>
> FROM posts
>
> WHERE id <= 50;

Trae todos los posts cuyo id sea mayor o igual a 50

> SELECT *
>
> FROM posts
>
> WHERE id >= 50;

Trae todos los posts cuyo id sea mayor a 50 (sin incluirlo)

> SELECT *
>
> FROM posts
>
> WHERE id > 50;

Trae todos los posts cuyo estatus sea igual a activo. OBS.: Esto solo funciona con campos que tengan datos precisos, como estatus que solo tiene activo o inactivo

> SELECT *
>
> FROM posts
>
> WHERE estatus = 'activo';

Trae todos los posts cuyo estatus sea inactivo

> SELECT *
>
> FROM posts
>
> WHERE estatus = 'activo';

Trae todos los posts cuyo estatus NO sea igual a activo

> SELECT *
>
> FROM posts
>
> WHERE estatus != 'activo';

Trae todos los posts cuyo id NO sea igual a 50

> SELECT *
>
> FROM posts
>
> WHERE id != 50;

Trae todos los posts que contenga la palabra escándalo

> SELECT *
>
> FROM posts
>
> WHERE titulo LIKE '%escandalo%';

Trae todos los posts que empiezan con la palabra escándalo

> SELECT *
>
> FROM posts
>
> WHERE titulo LIKE 'escandalo%';

Trae todos los posts que terminan con la palabra escándalo

> SELECT *
>
> FROM posts
>
> WHERE titulo LIKE '%escandalo';

Trae todos los posts que terminan con la palabra roja

> SELECT *
>
> FROM posts
>
> WHERE titulo LIKE '%roja';

Trae todos los posts cuya fecha de publicación sea después a 2025-01-01

> SELECT *
>
> FROM posts
>
> WHERE fecha_publicacion > '2025-01-01';

Trae todos los posts cuya fecha de publicación sea antes a 2025-01-01

> SELECT *
>
> FROM posts
>
> WHERE fecha_publicacion < '2025-01-01';

Trae todos los posts cuya fecha de publicación estén entre el rango de 2023-01-01 y 2025-12-31

> SELECT *
>
> FROM posts
>
> WHERE fecha_publicacion BETWEEN '2023-01-01' AND '2025-12-31';

Trae todos los posts cuyo id esté entre el rango de 50 y 60

> SELECT *
>
> FROM posts
>
> WHERE id BETWEEN '50' AND '60';

Trae todos los posts cuyo año de fecha de publicación se encuentra entre el 2023 y 2024

> SELECT *
>
> FROM posts
>
> WHERE YEAR(fecha_publicacion) BETWEEN '2023' AND '2024';

Trae todos los posts cuyo mes de fecha de publicación sea igual a Abril (04)

> SELECT *
>
> FROM posts
>
> WHERE MONTH(fecha_publicacion) = '04';

**NOTA**

- La propiedad LIKE nos ayuda a traer registros de los cuales conocemos sólo una parte de la información.
- La propiedad BETWEEN nos sirve para arrojar registros que estén en el medio de dos.


### Clase 34 *Utilizando la sentencia WHERE nulo y no nulo*

Ya sabemos que WHERE es utilizados para filtrar los row o tuplas, pero nos ha faltado ver dos tipos de datos muy particulares y es que no son exactamente un tipo de dato, aunque pueden ser considerado de ese modo, y esos son: nulo y no nulo.

El valor nulo en una tabla generalmente es el valor por defecto. Es el valor que se guarda en un campo cuando no tiene una especificación y por defecto la base de datos lo guarda como nulo. Muchos de los campos dentro de nuestra definición de base de datos le pusimos un constraint que se llama not null que quiere decir no nulo, no se desea que se quede vacío y por tanto es obligatorio.

**¿Cómo consultar a través de WHERE cuando tenemos un valor nulo?**

Hasta ahora hemos visto operados de consulta (igual, menor que, mayor que), LIKE o BETWEEN, pero para consultar los valor de tipo nulo no usamos esto porque no es mayor o menor a nada, es un vacío, una forma diferente de tratar la información. Entonces el valor nulo o no nulo va a funcionar de una manera un poco diferente y por eso lo debemos consultar de una manera muy particular.

**Ejemplo**

Vemos los posts que no tengan ningún usuario asociado

> SELECT *
>
> FROM posts
>
> WHERE usuario_id IS NULL;

Vemos los posts que no pertenezcan a ninguna categoría

> SELECT *
>
> FROM posts
>
> WHERE categoria_id IS NULL;

Trae los posts que SI tengan usuarios asociados
> SELECT *
>
> FROM posts
>
> WHERE usuario_id IS NOT NULL;

Traemos los posts que tengan usuarios asociados y con estatus activos

> SELECT *
>
> FROM posts
>
> WHERE usuario_id IS NOT NULL
>
> AND estatus = 'activo';

Traemos los posts que tengan usuarios asociados, estatus activos y cuyo id sea menor a 50

> SELECT *
>
> FROM posts
>
> WHERE usuario_id IS NOT NULL
>
> AND estatus = 'activo'
>
> AND id < 50;

Traemos los posts que tengan usuarios asociados, estatus activos, cuyo id sea menor a 50 y pertenezcan a la categoría 2

> SELECT *
>
> FROM posts
>
> WHERE usuario_id IS NOT NULL
>
> AND estatus = 'activo'
>
> AND id < 50
>
> AND categoria_id = 2;

Traemos los posts que tengan usuarios asociados, estatus activos, cuyo id sea menor a 50, pertenezcan a la categoría 2 y haya sido publicado en el año 2025

> SELECT *
>
> FROM posts
>
> WHERE usuario_id IS NOT NULL
>
> AND estatus = 'activo'
>
> AND id < 50
>
> AND categoria_id = 2
>
> AND YEAR(fecha_publicacion) = '2025';

### Clase 35 *GROUP BY*

GROUP BY tiene que ver con agrupación y es la que indica a la base de datos que criterios debe tener en cuenta para agrupar.

**Ejemplo**

Vemos los estatus que tenemos y la cantidad de posts que pertenecen a ese estatus

> SELECT estatus, COUNT(*) AS post_quantity
>
> FROM posts
>
> GROUP BY estatus;

Agrupamos los post por el año de publicación y contamos la cantidad de post hecho en ese tiempo

> SELECT YEAR(fecha_publicacion) AS post_year, COUNT(*) AS post_quantity
>
> FROM posts
>
> GROUP BY post_year;

Agrupamos los post por el mes de publicación, sin importar el año, y contamos la cantidad de post hecho en ese tiempo

> SELECT MONTHNAME(fecha_publicacion) AS post_month, COUNT(*) AS post_quantity
>
> FROM posts
>
> GROUP BY post_month;

Agrupamos los post por el estatus y después por el mes de publicación, sin importar el año, además contamos la cantidad de post hecho en ese tiempo y con ese estatus

> SELECT estatus, MONTHNAME(fecha_publicacion) AS post_month, COUNT(*) AS post_quantity
>
> FROM posts
>
> GROUP BY estatus, post_month;

### Clase 36 *ORDER BY y HAVING*

ORDER BY tiene que ver con el ordenamiento de los datos, justamente ORDER BY quiere decir 'ordena por', y se encarga de decirle a la base de datos que ordene los datos por los criterios que quieres usar.

**Ejemplo**

Ordena los datos por manera ascendente según la fecha de publicación

> SELECT *
>
> FROM posts
>
> ORDER BY fecha_publicacion;

Si quieres ser explícito de que ordenas de forma ascendente puedes hacer de la siguiente manera

> SELECT *
>
> FROM posts
>
> ORDER BY fecha_publicacion ASC;

El orden inverso, es decir, de manera descendente

> SELECT *
>
> FROM posts
>
> ORDER BY fecha_publicacion DESC;

Orden los datos ascendentemente por el titulo (alfabéticamente)

> SELECT *
>
> FROM posts
>
> ORDER BY titulo ASC;

Orden los datos descendentemente por el titulo (alfabéticamente)

> SELECT *
>
> FROM posts
>
> ORDER BY titulo DESC;

Orden los datos por el id de usuario ascendentemente

> SELECT *
>
> FROM posts
>
> ORDER BY usuario_id ASC;

Orden los datos por el id de usuario descendentemente

> SELECT *
>
> FROM posts
>
> ORDER BY usuario_id DESC;

Orden los datos por la fecha de publicación ascendentemente y filtra los primeros cinco

> SELECT *
>
> FROM posts
>
> ORDER BY fecha_publicacion ASC
>
> LIMIT 5;

**HAVING**

Una sentencia no muy utilizada, pero que es sumamente útil para casos muy particulares. HAVING tiene una similitud muy grande con WHERE, sin embargo, el uso de ellos depende del orden. Cuando se quiere seleccionar tuplas agrupadas únicamente se puede hacer con HAVING.

**Ejemplo**

Seleccionamos la fecha de publicación según el mes y el estatus, y contamos todo, agrupamos por mes y estatus, ordenamos por el mes y filtramos para ver los que tengan más de un post publicado

> SELECT MONTHNAME(fecha_publicacion) AS post_month, estatus, COUNT(*) AS post_quantity
>
> FROM posts
>
> GROUP BY estatus, post_month
>
> HAVING post_quantity > 1
>
> ORDER BY post_month;

### Clase 37 *El interminable agujero de conejo (Nested queries)*

Los nested queries significan que dentro de un query podemos hacer otro query. Esto sirve para hacer join de tablas, estando una en memoria. También teniendo un query como condicional del otro.

Este proceso puede ser tan profundo como quieras, teniendo infinitos queries anidados. Se le conoce como un producto cartesiano ya que se multiplican todos los registros de una tabla con todos los del nuevo query. Esto provoca que el query sea difícil de procesar por lo pesado que puede resultar.

**¿Cuándo ocupar los nested queries?**

Generalmente se utiliza cuando se tiene un problema que no se puede solucionar simplemente consultando tu tabla, por si necesitas hacer agregación u otro tipo de operación que viene de otra tabla o de tu misma tabla.

**¿Cuándo NO ocupar los nested queries?**

Es bueno saber cuándo utilizarlo, pero es mejor saber cuándo NO utilizarlo. Debido a que es pesado y resulta difícil de usar, se debe evitar que el uso de lo nested queries en base de datos que van a estar creciendo constantemente.

**Ejemplo 1**

> SELECT new_table_projection.date, COUNT(*) AS posts_count
>
FROM (
>
	SELECT DATE(MIN(fecha_publicacion)) AS date, YEAR(fecha_publicacion) AS post_year
>
	FR> OM posts
>
	GROUP BY post_year
>
) AS new_table_projection
>
GROUP BY new_table_projection.date
>
ORDER BY new_table_projection.date;

**Ejemplo 2**

> SELECT *
>
FROM posts
>
WHERE fecha_publicacion = (
>
	SELECT MAX(fecha_publicacion)
>
	FROM posts
>
);

### Clase 38 *¿Cómo convertir una pregunta en un query SQL?*

Ahora tienes todo lo necesario para trabajar y operar con las bases de datos relacional en el día a día; ya entiendes los conceptos, entiendes el valor de hacer un buen query, ya tienes todas las herramientas para armar ese query y en esta clase aprenderás a transformar una pregunta en un query, esto no siempre es una transformación directa y muchas de las sutilezas que involucra, porque es casi un arte, la vas adquirieron conforme te preguntes nuevas cosas o tu empresa requiera nuevas cosas.

El equivalente de pregunta a query:

- SELECT: Lo que quieres mostrar en cuando a que datos. Que información nos conviene presentar al usuario.
- FROM: De dónde voy a tomar los datos. ¿La saco de una tabla? ¿Necesito dos tablas? ¿Tres tablas? ¿A través de que campos voy hacer los join?
- WHERE: Los filtros de los datos que quieres mostrar. Ya tengo mi información, pero no la quiero toda así que vamos sacar, discriminar que no me sirve y solo vamos a dejar los datos relevantes.
- GROUP BY: Los rubros por los que me interesa agrupar la información. ¿Por qué grupos me interesa seleccionar la información?
- ORDER BY: El orden en que quiero presentar mi información. ¿Lo ordeno por fecha? ¿Deseo saber cuál se escribió primero? ¿Quiero el top 10? ¿Sácame los 5 mejores?
- HAVING: Los filtros que quiero que mis datos agrupados tengas. Usado cuando ya has filtrado todos los datos y deseamos sacar un documento que tenga más sentido.

### Clase 39 *Preguntándole a la base de datos*

Veremos cómo transformamos algunas dudas o preguntas que pueden surgir del proyecto PlatziBlog en queries.

**¿Cuántas etiquetas tiene un blogpost?**

Para resolverlo debemos plantearnos primero que deseamos sacar con el SELECT (el título del posts y la cantidad de etiquetas), con FROM vemos que tablas necesitamos para sacar la información (unión entre la tabla posts y la tabla etiqueta mediante la tabla transitiva posts_etiquetas) y finalmente vemos la forma en que deseamos agrupar (agrupamos por el id, porque deseamos saber la cantidad de etiquetas tiene un posts).

> SELECT posts.titulo, COUNT(*) num_etiqueta
>
FROM posts
>
	INNER JOIN posts_etiquetas ON posts.id = posts_etiquetas.post_id
>
	INNER JOIN etiquetas ON etiquetas.id = posts_etiquetas.etiqueta_id
>
GROUP BY posts.id;

Si deseamos ir un paso más allá, también podemos filtrar y ver cuáles son los posts que tiene más etiquetas.

> SELECT posts.titulo, COUNT(*) num_etiqueta
>
FROM posts
>
	INNER JOIN posts_etiquetas ON posts.id = posts_etiquetas.post_id
>
	INNER JOIN etiquetas ON etiquetas.id = posts_etiquetas.etiqueta_id
>
GROUP BY posts.id
>
ORDER BY num_etiquetas DESC;

**¿Cuáles son las etiquetas que pertenecen al posts?**

Para responder a esta pregunta es necesario usar GROUP_CONCAT que toma el resultado del query y lo pone como campo separado por comas.

> SELECT posts.titulo, GROUP_CONCAT(nombre_etiqueta)
>
FROM posts
>
	INNER JOIN posts_etiquetas ON posts.id = posts_etiquetas.post_id
>
	INNER JOIN etiquetas ON etiquetas.id = posts_etiquetas.etiqueta_id
>
GROUP BY posts.id;

**¿Cuáles son las etiquetas que no tengan posts relacionados?**

> SELECT *
>
FROM etiquetas
>
	LEFT JOIN posts_etiquetas ON etiquetas.id = posts_etiquetas.etiqueta_id
>
WHERE posts_etiquetas.etiqueta_id IS NULL;

### Clase 40 *Consultando PlatziBlog*

Consulta: Traer las categorías ordenados por las que tienen más posts hasta la menor

> SELECT c.nombre_categoria, COUNT(*) AS cant_posts
>
FROM categorias AS c
>
	INNER JOIN posts AS p ON c.id = p.categoria_id
>
GROUP BY c.id
>
ORDER BY cant_posts DESC;

¿Cuál es la categoría con más posts?

> SELECT c.nombre_categoria, COUNT(*) AS cant_posts
>
FROM categorias AS c
>
	INNER JOIN posts AS p ON c.id = p.categoria_id
>
GROUP BY c.id
>
ORDER BY cant_posts DESC
>
LIMIT 1;

¿Cuáles son las cantidad de posts creado por usuario?

> SELECT u.nickname, COUNT(*) AS cant_posts
>
FROM usuarios AS u
>
	INNER JOIN posts AS p ON u.id = p.usuario_id
>
GROUP BY u.id
>
ORDER BY cant_posts DESC;

Saber cuáles son las categorías que los usuarios escriben

> SELECT u.nickname, COUNT(*) AS cant_posts, GROUP_CONCAT(nombre_categoria)
>
FROM usuarios AS u
>
	INNER JOIN posts AS p ON u.id = p.usuario_id
>
	INNER JOIN categorias AS c ON c.id = p.categoria_id
>
GROUP BY u.id
>
ORDER BY cant_posts DESC;

Sacamos los usuarios que no escriben ningún posts

> SELECT *
>
FROM usuarios
>
	LEFT JOIN posts ON usuarios.id = posts.usuario_id
>
WHERE posts.usuario_id IS NULL;
