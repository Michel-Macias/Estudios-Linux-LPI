# 3.2 Buscar y extraer datos de los ficheros

#### Áreas de conocimiento clave

- Tuberías en la línea de comandos
- Re-dirección de Entrada/Salida
- Expresiones Regulares básicas usando ., [ ], *, y ?

#### Lista parcial de archivos, términos y utilidades

- grep
- less
- cat, head, tail
- sort
- cut
- wc   

## Ejercicios guiados

1. Liste el contenido del directorio actual, incluyendo la propiedad y los permisos, y redirija la salida a un fichero llamado contents.txt dentro del directorio home del usuario.

`ls -lah > contents.txt`

2. Ordene el contenido del archivo contents.txt de su directorio actual y añádalo al final de un
nuevo archivo llamado contents-sorted.txt.

`sort contents.txt >> contents-sorted.txt`

3. Muestre las últimas 10 líneas del fichero /etc/passwd y rediríjalas a un nuevo fichero en el
directorio Documents de su usuario.

`tail -n 10 /etc/passwd > /Documentos/newfile`


4. Cuente el número de palabras dentro del archivo contents.txt y agregue la salida al final de
un archivo field2.txt en su directorio de inicio. Deberá utilizar la redirección de entrada y
salida.

`wc < contents.txt >> field2.txt`

5. Muestre las primeras 5 líneas del fichero /etc/passwd y ordene la salida en orden alfabético.

`head -n 5 /etc/passwd | sort -r`

6. Usando el archivo contents.txt creado anteriormente, cuente el número de caracteres de las
últimas 9 líneas.

`tail -n 9 contents.txt | wc -c`

7. Cuente la cantidad de ficheros llamados test dentro del directorio /usr/share y sus
subdirectorios. Nota: cada salida de línea del comando find representa un fichero.

`find /usr/share -name test | wc -l`


## Respuestas a los ejercicios exploratorios

1. Seleccione el segundo campo del fichero contents.txt y redirija la salida estándar y la salida
de error a otro fichero llamado field1.txt.

`cut -f 2 -d " " contents.txt &> field1.txt`

2. Usando el operador de redirección de entrada y el comando tr, elimine los guiones (-) del
fichero contents.txt.

`tr -d "-" < contents.txt`

3. ¿Cuál es la mayor ventaja de solo redirigir errores a un fichero?

Redirigir solo los errores a un archivo proporciona una forma más eficiente de gestionar y analizar los mensajes de error generados por comandos o programas, permitiendo una depuración más efectiva y mejorando la legibilidad de la salida estándar.

4. Reemplace todos los espacios recurrentes por un solo espacio dentro del fichero
contenidos.txt ordenado alfabéticamente.

`sort contents.txt | tr -s " "`

5. En una línea de comando, elimine los espacios recurrentes (como se hizo en el ejercicio
anterior), seleccione el noveno campo y ordénelo alfabéticamente y sin distinción entre
mayúsculas y minúsculas. ¿Cuántas "pipes" tuviste que usar?

`cat contents.txt | tr -s " " | cut -f 9 -d " " | sort -fr`

- Hemos usado como se puede ver 3 pipes

## Resumen

En esta lección, usted aprendió:

- Tipos de redirección
- ¿Cómo usar los operadores de redirección?
- ¿Cómo usar tuberías para filtrar la salida de comandos?

Comandos usados en esta lección:

- `cut`
Elimina secciones de cada línea de un fichero.
- `cat`
Muestra o concatena ficheros.
- `find`
Busca ficheros en una jerarquía de directorios.
- `less`
Muestra el contenido de un fichero, lo que permite al usuario desplazarse línea a línea.
- `more`
Muestra el contenido de un fichero, página a página.
- `head`
Muestra las primeras 10 líneas de un fichero.
- `tail`
Muestra las últimas 10 líneas de un fichero.
- `sort`
Ordena ficheros.
- `wc`
Cuenta de forma predeterminada las líneas, palabras o bytes de un fichero.