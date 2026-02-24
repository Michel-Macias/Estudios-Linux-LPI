## 3.1 Archivar ficheros desde la línea de comandos

#### Introducción

La compresión reduce el espacio ocupado por datos y se utiliza para almacenar archivos y enviar datos a través de redes.
Reemplaza patrones repetitivos en los datos para reducir su tamaño. La compresión puede ser sin pérdida o con pérdida. Las herramientas de archivo agrupan archivos y directorios en un solo archivo. Las herramientas de compresión comunes en Linux son `bzip2, gzip y xz`. Cada herramienta utiliza algoritmos diferentes y no son intercambiables. La compresión puede llevar más tiempo para patrones complejos. Las herramientas de compresión y archivo en Windows están integradas, mientras que en Linux se deben instalar por separado, como `zip y unzip` para archivos **.zip**.

#### Herramientas de compresión

- La cantidad de espacio en disco que se ahorra al comprimir los archivos depende de varios
factores: la naturaleza de los datos que se comprimen, el algoritmo utilizado para comprimir los
datos y el nivel de compresión.
- No todos los algoritmos admiten diferentes niveles de compresión. Algunas herramientas soportan diferentes niveles de compresión, normalmente un nivel más alto
requiere más memoria y ciclos de CPU, pero se obtiene un archivo comprimido más pequeño; lo
contrario es cierto para un nivel más bajo.
- No es necesario descomprimir un archivo cada vez que se necesite. Las herramientas de
compresión, normalmente incluyen versiones especiales de aplicativos que son usados para leer
archivos de texto, por ejemplo, `gzip` incluye una versión de `cat, grep, diff, less, more`, etc. Para `gzip`, las herramientas utilizan el prefijo z, mientras que el prefijo bz se usa para `bzip2 y xz` para xz.

#### Archivadores

- El programa tar es probablemente el archivador más utilizado en sistemas Linux. Su nombre
proviene de la abreviatura de “tape archive”, ya que los archivos creados con tar se denominan a
menudo como tar balls. Es muy común que el código fuente de las aplicaciones se distribuya en
tar balls.
- Las distribuciones de Linux que incluyen la versión GNU de tar tiene muchas opciones, esta
lección cubrirá el subconjunto más utilizado.
- La opción c indica a tar que cree un nuevo archivo y la opción f el nombre del archivo a crear. El argumento que sigue después de las opciones siempre será el nombre del archivo con el que se va a trabajar. El resto de los argumentos son las rutas a cualquier fichero o directorio que se desee añadir, listar o extraer del archivo. En el ejemplo, se añade el directorio compression y todo su contenido al archivo comprimido. Para ver el contenido de un archivo creado con tar, se utiliza la opción t

<div style="text-align:center">
    <img src="./tarcaptura.png" alt="Captura Tar" width="350">
</div>



#### Resumen

- Los sistemas Linux incluyen varias herramientas de compresión y archivado, esta lección cubre
las más comunes. La herramienta de archivado más común es tar. Si es necesario interactuar con
sistemas Windows, zip y unzip pueden crear y extraer archivos ZIP.
- El comando tar tiene algunas opciones que vale la pena memorizar: x para extraer, c para crear,
t para ver el contenido, y u para agregar o reemplazar archivos. La opción v muestra los archivos
que son procesados por tar mientras se crea o extrae un archivo.
- Generalmente los repositorios de distribuciones de Linux incluyen muchas herramientas de
compresión, las más comunes son gzip, bzip2, y xz. Los algoritmos de compresión generalmente
soportan diferentes niveles que permiten optimizar el proceso según la velocidad o el tamaño del
archivo. Los archivos pueden descomprimirse utilizando gunzip, bunzip2, y unxz.
- Las herramientas de compresión generalmente incluyen programas que se comportan como
herramientas comunes de archivos de texto, con la diferencia de que funcionan con archivos
comprimidos, algunos ejemplos de estas son zcat, bzcat y xzcat. Las herramientas de
compresión suelen incluir programas con la funcionalidad de grep, more, less, diff, y cmp.

Comandos utilizados en los ejercicios:

`bunzip2`
- Descomprime un archivo comprimido con bzip2.

`bzcat`
- Muestra el contenido de un archivo comprimido con bzip.

`bzip2`
- Comprime archivos usando el algoritmo y formato bzip2.

`gunzip`
- Descomprime un archivo comprimido con gzip.

`gzip`
- Comprime archivos usando el algoritmo y formato gzip.

`unxz`
- Descomprime archivos comprimidos con xz.

`unzip`
- Descomprime y extrae el contenido de un archivo ZIP.

`xz`
- Comprime archivos usando el algoritmo y formato xz.

`zcat`
- Muestra el contenido de un archivo comprimido con gzip.

`zip`
- Crea y comprime archivos ZIP.