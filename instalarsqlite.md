![ ](https://www.sqlite.org/images/sqlite370_banner.gif)

# ¿Cómo instalar SQLITE en windows?

## ¿Qué es SQLite?
Lo que nos dice la documentación es:
> SQLite es una librería en lenguaje C que implementa un motor de base de datos SQL pequeño, rápido, autónomo, de alta confiabilidad y con todas las funciones. SQLite es el motor de base de datos más utilizado del mundo. SQLite está integrado en todos los teléfonos móviles y en la mayoría de las computadoras y viene incluido dentro de innumerables otras aplicaciones que la gente usa todos los días. 
Lo que se traduce como: 
***Si quieres una base de datos buena, bonita y barata (recursos), está es tu mejor opción***

## Ok, pero ¿Cómo la instalo?. 
Para instalar SQLite en Windows lo único que tienes que hacer es ir a la página oficial la cual es: [Página oficial](https://www.sqlite.org/download.html) y seleccionar la opción
> sqlite-tools-win64-x86-3460100.zip
la cual va a contener herramientas para la línea de comandos, el archivo sqlite3.exe, sqldiff.exe y sqlite3_analizer.exe
Una vez descargada lo que debes de hacer es descomprimirla, se recomienda crear una carpeta en tu disco local C (o el que tengas disponible) y crear una carpeta con el nombre src.
Te debe de quedar algo mas o menos así:
>C:\src\sqlite-tools-win64-x86-3460100
Dentro de esa carpeta debe estar tus tres archivos .exe, si lo deseas puedes cambiarle el nombre a la carpeta y que solo diga SQLite. 

## PATH de Windows ¿Para que necesito hacer eso?
Para que puedas ejecutar un comando en el cmd de Windows o desde cualquier terminal, debes acceder a la carpeta, pero para poder ahorrarte el escribir la ruta de las carpetas todo el tiempo se crea el PATH

## Agregar la variable de entorno al PATH
Para agregar una variable de entorno es bien facil.
1. Presionar (Windows + e) para abrir nuestro explorador de archivos
2. Clic DERECHO en "Este equipó" y seleccionar propiedades
3. Seleccionar Configuración avanzada del sistema 
4. Dar clic en Variables de entorno (Es la ultima opción de Opciones avanzadas)
5. Buscar la variable Path y dar clic en Editar 
6. Dar clic en Nuevo
7. Agregamos la ruta de nuestra carpeta que debería de ser C:\src\sqlite-tools-win64-x86-3460100 y dar clic en aceptar
Listo!!, ya puedes ejecutar comandos de sqlite desde el cmd.

## A veeeeeer
Ejecuta el comando **sqlite3** desde la línea de comandos.
~~~
SQLite version 3.28.0 [FECHA] [HORA]
Enter ".help" for usage hints.
Connected to a transient in-memory database.
Use ".open FILENAME" to reopen on a persistent database.
~~~

## ¿Y cómo crear una base de datos?
Para crear una base de datos accede a la carpeta donde la desees crear y tienes que escribir el siguiente comando
sqlite3 NOMBRE_DE_TU_BASE_DE_DATOS.EXTENSIÓN por ejemplo:
~~~
sqlite3 MiBaseDeDatos.db
~~~
Después de dar Enter se "creara tu base de datos" pero no se creara realmente hasta que trabajes con ella.
Para comenzar a trabajar con tu base de datos ejecuta el comando:
~~~
sqlite3 .databases
~~~
Después de ejecutar ese comando deberá de crearse el archivo MiBaseDeDatos.db

## Bien hecho!, ya tienes tu base de datos.
