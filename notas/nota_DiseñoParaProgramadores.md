# Introducción a la Terminal y Línea de Comandos
## Modulo 1. Introducción
### Clase 1 *Expert Session: Diseño para Programadores*
### Clase 2 *Bienvenida*

Tu profesora será Samanta Martínez, es ingeniera front end y diseñadora web. Ha participado en proyectos con Disney, Google, Renault, ESPN, por mencionar algunos.

## Modulo 2. Entender los Fundamentos del diseño
### Clase 3 *El proceso creativo*

Cuantas veces has escuchado programadores o incluso tú mismo decir esta frase: Me gustaría diseñar pero no tengo creatividad.

Pues la verdad no es así, el proceso creativo, al igual que cualquier otro proceso técnico, costa de algunos pasos y aunque lo hagamos de una manera inconsciente siempre lo aplicamos para resolver distintos problemas

Pasos del proceso creativo
- **Preparación:** investigar, recopilar
- **Incubación:** experimentar, sintetizar
- **Iluminación:** idear, imaginar
- **Evaluación:** criticar, replantear
- **Implementación:** construir, trabajar

En que consiste todos esos pasos, pues:
1. En la ***preparación*** es donde recopilamos e investigamos toda la información relativa a un problema o a una cosa que deseamos solucionar.
2. En la ***incubación*** en esta etapa lo que hacemos es experimentar y buscar diferentes soluciones, mirar como otras personas solucionaron los problemas.
3. En la ***iluminación*** es donde se nos ocurre la idea, entonces, es en esta etapa en donde se nos permite idear e imaginar soluciones
4. En la ***evaluación*** aquí evaluamos si las soluciones son practicas o viales, y las criticamos. Si es necesario la volvemos a replantear.
5. En la ***implementación*** es donde ya con construimos nuestra idea, trabajamos en ella y conseguimos un producto final.

Este proceso no se aplica únicamente en diseño o para crear soluciones, sino que lo aplicamos todos los días para solucionar problemas de la vida cotidiana.

***El proceso creativo es necesario para saber que la creatividad no es un talento o algo con lo que se nace, sino que es algo que todos podemos ir desarrollando.***

### Clase 4 *Conceptos básicos de diseño*

- **Balance:** se refiere a la estructura y estabilidad de una composición en donde la posición de cada elemento es dada por su peso visual. Pueden ser simétricos o asimétricos.
- **Contraste:** lo podemos utilizar para señalar un concepto marcado por la diferencia entre dos elementos distintos.
- **Alineación:** nos permite crear una ruta visual entre diferentes elementos que queremos señalarle al usuario.
- **Proximidad:** nos permite agrupar diferentes elementos. No necesariamente debe ser física, sino que podemos agrupar por colores o elementos
- **Repetición:** es muy utilizada para generar concepto de marca.
- **Espacio:** permite aprovechar el espacio proporcionado de manera eficiente.

### Clase 5 *Diseño responsivo*

Responsive Desing es una metodología de diseño que nos permite crear diferentes diseños que sean adaptables a diferentes tamaños de pantalla.

Como sabemos que nuestro diseño es Responsive Desing:
1. Lo primero es empezar por los dispositivos móviles. Esto nos garantiza que partimos del contenido básico hasta el contenido más complejo.
2. Separar las capas de contenido y funcionalidad. Esto nos sirve para garantizarle al usuario todo el acceso al contenido de nuestra página sin tener que ejecutar screem, de realizar alguna acción ni de ejecutar animaciones complejas.
3. Utilizar sistemas de grillas y columnas. Las columnas son una referencia para dividir el total de la página, de esta manera será más sencillo adaptar los contenidos como imágenes, texto o videos.

Hay distintas maneras de hacer Responsive Desing:
- **Mejora progresiva (Progressive enhancement):** consiste en partir de una base sólida en donde tenemos los elementos esenciales y básicos, y luego le vamos añadiendo capas de complejidad. Es la más recomendada pues con esto podemos garantizar que los usuarios con baja memoria o con un dispositivo muy pequeño puedan acceder al contenido, y los usuarios con mejores dispositivos o pantallas más grandes puedan acceder a la misma experiencia pero de una manera más enriquecedora como con animaciones y otras funcionalidades.
- **Degradación agraciada (Graceful degradation):** es todo lo contrario a la mejora progresiva. Aquí se parte de la versión full y completa en donde tenemos todas las animaciones, contenido e imágenes, y vamos quitando capas de complejidad para que se adapten a dispositivos más pequeños o más lentos. La degradación agraciada es recomendada para escenarios específicos, como cuando deseamos adaptar una página ya existente.

Esta metodología no solo es aplicable a diseños, sino también puede utilizarse en códigos como vemos a continuación:

![src/diseño_1.png](src/diseño_1.png)

1. Primero partimos del dato
2. Después hacemos la maquetación con HTML
3. A continuación le añadimos estilo con CSS
4. Y por último el JS

***ERROR: si iniciamos una aplicación con JS, esta estará basada en script y no en web semántica la cual es el ideal.***

### Clase 6 *Accesibilidad y diseño*

Un componente importante que se debe añadir a una página web es la accesibilidad. Hoy en día es importante que nuestras aplicaciones y páginas sean accesibles, la web es un derecho para todas las personas incluidas las personas que tienen discapacidades físicas, motoras, visuales o auditivas.

Dicho por el director de la W3C, Tim Berners-Lee:

***El poder de la web está en su universalidad. El acceso de todas las personas independientemente de la discapacidad es un aspecto esencial.***

**¿Cómo podemos hacer que nuestras páginas sean más accesibles?**

Existen algunos tips básicos

- Utiliza los encabezados de manera ordenada para organizar la estructura del contenido.
- Utiliza tamaños de fuente accesibles.
- Utiliza colores que tengan un contraste adecuado.
- Garantiza que el código de color no sea la única forma de relacionar contenido
- Diseña teniendo en cuenta los estados 'focus' y 'active' de los componentes.
- Añade etiquetas y textos descriptivos a campos de formulario.
- Escribe contenido descriptivo que pueda reemplazar videos e imágenes.
- Garantiza que las animaciones no bloqueen el acceso del contenido

### Clase 7 *Brief y requerimientos técnicos*

Brief es un documento donde vamos a consignar todos los objetivos y datos relevantes para nuestra aplicación. Es la hoja de ruta para empezar a diseñar.

**Contenido del brief**

Algunos contenidos más comunes son:

- Objetivos
- Identidad de marca
- Público objetivo
- Audiencia al que va dirigido nuestro producto
- La competencia
- Referencias de paginas
- Canal de distribución
- Cronograma

El ejemplo de un brief para un restaurant de comida rapida es: [Steam Burger](http://https://github.com/mssroboto/diseno-para-programadores/blob/master/1-brief/Brief..pdf "steam burger")

## Modulo 3. Aprender sobre Diseño Experiencia de usuario
### Clase 8 *Definición de diseño UX*
El diseño UX o diseño de experiencia de usuario es un diseño que se centra en los usuarios y en la usabilidad como lo dice esta frase de Alan Cooper, diseñador de software y programador:

***Si queremos que a nuestros usuarios les guste nuestro software, deberíamos diseñarlo para que se comporte como una buena persona: respetuoso, generoso y colaborador.***

Muchas veces entramos a páginas en la que hacer una tarea es muy difícil, ya sea que vamos a subir un recibo o pagar un banco, errores que no son claros, se cierran las sesiones, todo esto problemas son porque no se hizo un buen diseño UX.

**Etapas del diseño UX**

- **Investigación**
En esta etapa se recopilan datos de cómo se comportan los usuarios y en cómo se manejan en otras aplicaciones ya existentes. Esto sirve para que podamos crear un producto que de verdad le vaya a funcionar a los usuarios finales.
- **Análisis**
Esta etapa consiste en clasificar y agrupar la información para definir unos objetivos a nivel de usuario.
- **Diseño**
En este curso nos enforcaremos en esta etapa. Aquí crearemos unos prototipos, unos flujos de usuarios y más que nos permitirá saber cuáles son las mejores prácticas para nuestros usuarios finales.
- **Pruebas de usuarios**
Finalmente se realizan diferentes pruebas, por lo general con prototipos en papel o con prototipos interactivos, pero no con el producto final. Esta etapa nos permitirá hacer ajustes de diseño antes de pasar por una etapa de desarrollo y otras cosas más complejas.

### Clase 9 *Diagramas de flujo*

El primer paso del diseño UX son diagramas de flujos.

**Requerimientos:**
- **Objetivos**
	- Dar a conocer sus productos.
	- Aumentar la presencia en línea.
	- Hacer pedidos online.
	- Dar a conocer su marca.
- **Requerimiento**
	- Menú y promociones.
	- Redes sociales.
	- Pedidos.
	- Contacto y sucursales.

Un diagrama de flujo básico, muy sencillo, es el **Site Map** que nos permite ver un mapa de todas las secciones del sitio que nombramos anteriormente:

![src/diseño_2.png](src/diseño_2.png)

Este tipo de diagrama nos permite ver cuáles son las secciones principales, cuáles son las secundarias y cuáles son las externas, las que solamente serán un link desde nuestra página.

Otro tipo de diagrama, más complejo, son los **User Flow**:

![src/diseño_3.png](src/diseño_3.png)

Este nos permite ver el flujo general que debe completar un usuario para hacer su pedido.

### Clase 10 *Wireframes y componentes*

Wireframes es como el plano de la aplicación. Aquí se hacen bocetos y bosquejos de todos los componentes que va a tener la aplicación y las pantallas que salieron anteriormente en los diagramas de flujos.

**RECOMENDAMIENTO:** hacer los dibujos a mano, no hay necesidad de complicarse con programas de diseño, lo importante es tener un inventario y volar la imaginación en cuanto a las soluciones que le vamos a dar a los distintos componentes.

Los wireframes hechos a mano y en papel se le conoce comowireframes de baja calidad o de baja fidelidad. Pueden servir para tener una idea general o incluso para hacer prueba de usuarios.

También hay wireframes hechos ya en cualquier programa de diseño, incluso en Google Docs, PowerPoint o Paint, estos son llamados wireframes de alta calidad.

Ejemplo de [wireframes](https://github.com/mssroboto/diseno-para-programadores/tree/master/3-wireframes..pdf "wireframes") para desktop y móvil.

**¿Cómo podemos hacer pruebas de usuarios con wireframes?**
Podemos hacerlo de mucha manera, como grabarle a una persona interactuando con los papeles.

Hacer wireframes no solo es muy importante para diseño, sino que también lo es para desarrollo, y es importante incluir al equipo de desarrollo en esta etapa porque comienzan a saber que tamaño tendrá la aplicación.
También es importante negociar esta etapa con el cliente y así se va haciendo a la idea de que secciones tendrá su producto.

## Modulo 4. Aprender sobre Diseño de interfaz de usuario

### Clase 11 *Definición de diseño UI*
### Clase 12 *Moodboard y línea gráfica*
### Clase 13 *Teoría del color*
### Clase 14 *Paletas de color*
### Clase 15 *Tipografía*
### Clase 16 *Layout y sistemas de grillas*
### Clase 17 *Sistemas de componentes UI*
### Clase 18 *Themes y customizaciones*
### Clase 19 *Imágenes para web*
### Clase 20 *Gráficos en movimiento para web*
### Clase 21 *Resultado final*

## Modulo 5. Conclusiones
### Clase 22 *Conclusiones del curso*

## Modulo 6. Mentoría Expert
### Clase 22 *Diseño para programadores*
