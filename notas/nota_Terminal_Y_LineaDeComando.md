# Introducción a la Terminal y Línea de Comandos
## Modulo 1. Comprender las ventajas del uso de la terminal
### Clase 1 *Introducción al curso: ¿Qué es y cómo funciona la terminal?*
Que aprenderás:
- Que es la terminal
- Porque usar la terminal
- Como usar la terminal
- Como aprovechar la terminal al máximo

La termina es un programa que recibe instrucciones de una forma medianamente cómoda, las traduce a un lenguaje que el computador comprende, las ejecuta y muestra los resultados. Utiliza un entorno 100% texto, por tanto, es muy eficiente y rápida, y a través de ella se puede automatizar tareas repetitivas.

Se compone de:
- **Prompt:** es un conjunto de caracteres al principio de cada línea y muestra información propia del sistema en que se esté utilizando.
- **Cursor:** es un 'underscore' que titila en la pantalla del terminal, y en conjunto con el prompt, indica que están a la espera de recibir órdenes.

En la terminal se ingresan instrucciones, también conocidas como 'comandos', los cuales están compuestos por:
- Nombre del programa
- Parámetros
- Modificadores

La terminal también cuenta con otras utilidades como:
- Comodines
- Combinación de teclas
- Sustitución de comandos

***Diferencia entre:
Parámetro: información adicional para la ejecución del programa.
Modificadores: alteración de lo que el programa va hacer.***

Algunos comandos son:
- date: muestra la fecha
- echo: permite imprimir en la terminal
- man <nombre de comando>: muestra información sobre los comandos
- history: historial de los comandos que hemos realizado en algún momento
- ! + número obtenido del history: ejecuta el comando con el número
### Clase 2 *Windows Subsystem for Linux (WSL): Cómo acceder a la terminal en Windows*
Para acceder a la terminal de Linux desde Windows es necesario que tengas instalado el Windows Subsystem for Linux.

Una vez instalado podrás colocar allí cualquier distribución de Linux que desees (si no conoces ninguna te recomiendo comenzar con Ubuntu).

Para continuar necesitarás tener acceso como administrador a tu computadora, asumiré que lo tienes para mostrarte el proceso de instalación.

Comencemos abriendo una terminal Window PowerShell (como administrador):

![src/terminal_1.png](src/terminal_1.png)

Una vez allí escribe el siguiente comando: *Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux.*

![src/terminal_2.png](src/terminal_2.png)

Deberías ver algo como:

![src/terminal_3.png](src/terminal_3.png)

Alternativamente (dependiendo de tu versión de Windows) puedes encontrar un modo más simple:

![src/terminal_4.png](src/terminal_4.png)

![src/terminal_5.png](src/terminal_5.png)

Cuando te sea requerido, reinicia tu computadora.

Al reiniciar estará todo listo para instalar tu distribución favorita.

Ingresa a la tienda de Windows:

![src/terminal_6.png](src/terminal_6.png)

Busca Linux:

![src/terminal_7.png](src/terminal_7.png)

![src/terminal_8.png](src/terminal_8.png)

Selecciona tu distribución favorita:

![src/terminal_9.png](src/terminal_9.png)

Da click en Obtener:

![src/terminal_10.png](src/terminal_10.png)

Selecciona instalar y, cuando haya terminado, “Lanzar”

![src/terminal_11.png](src/terminal_11.png)

Allí comenzará el proceso de instalación/configuración (¡pero ya dentro de Linux!):

![src/terminal_12.png](src/terminal_12.png)

Ingresa tu nombre de usuario (el de Linux, que puede ser completamente diferente al de Windows):

![src/terminal_13.png](src/terminal_13.png)

Y crea tu contraseña:

![src/terminal_14.png](src/terminal_14.png)

¡Y listo! Ya tienes una consola de Linux dentro de tu Windows!

![src/terminal_15.png](src/terminal_15.png)

Para acceder nuevamente o crear una ventana paralela:

![src/terminal_16.png](src/terminal_16.png)

Tienes una nueva entrada en tu menú de inicio.

¡Felicitaciones! Ya puedes operar sobre la terminal de Linux sin problemas.

Un último detallito importante: los archivos que tienes en tu Linux le pertenecen… Para acceder a los archivos que tienes en Windows (o grabar nuevos archivos desde tu Linux) debes ingresar en /mnt/c/Users/TU_USUARIO, donde TU_USUARIO debe ser reemplazado por tu nombre de usuario de Windows.

Ahora sí, cualquier archivo que guardes en esa localización podrá ser accedido con las herramientas propias de Windows.

¡Diviértete!

***OBSERVACIÓN: Esto no esta disponible para Windows 8 y 8.1***
