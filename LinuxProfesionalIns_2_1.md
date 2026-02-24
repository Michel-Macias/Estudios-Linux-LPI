# 2.2 Uso de la línea de comandos para obtener ayuda

### EJERCICIOS Y PREGUNTAS

### 1. **Use el comando man para averiguar qué hace cada comando**

| Comando | Descripción |
|---------|-------------|
| ls | Mostrar contenido directorio |
| cat | Concatena archivos y los muestra por la salida estándar |
| cut | Elimina fragmentos en cada línea de un archivo |
| cd | Change directory *no tiene manual*|
| cp | Copia archivos y directorios |
| mv | Mueve o renombra files |
| mkdir | Make directory |
| touch | Cambia la fecha de un file, *si no existe se crea* |
| wc | imprime  el  número  de  líneas, de palabras o de byte de un archivo |
| passwd | Change user password |
| rm | remove **Borra files & folders** |
| rmdir | Borra directorios *vacios* |
| more | Muestra la salida por páginas |
| less | Similar a *more* pero más funcional |
| whereis | Localice los archivos binarios, de origen y de página de manual para un dominio |
| head | Muestra las primeras líneas de un file |
| tail | Muestra las últimas líneas de un file |
| sort | Ordena las líneas de un text file |
| tr | Traduce y/o elimina caracteres |
| chmod | Modifica los file permissions |
| grep | Busca patrones en un file |


### 2. Abra la página de información del comando **ls** e identifique el *MENU*

**¿Qué opciones tiene?**

- Which files are listed
- What information is listed
- Sorting the output
- General output formatting
- Formatting file timestamps
- Formatting the file names

**Encuentre la opción que le permite ordenar por tiempo de modificación.**
- ls -t

### 3. Muestre la ruta de los primeros 3 archivos README. Use el comando man para identificar la opción correcta para locate

- Primero debemos actualizar la base de datos para incluir los últimos files con *updatedb*
- Después le pasamos *locate -b '\README' | head -n 3*
- Este comando buscará todos los archivos que contengan la cadena "README" en su nombre en la base de datos de "locate", y luego la salida se enviará a la entrada estándar de la siguiente orden "head" que mostrará solo las primeras 3 líneas del resultado.

### 4.Cree un archivo llamado test en su directorio de inicio. Encuentre su ruta absoluta con el comando locate.

- Crea el file **test.txt** con el comando touch
- Si le pasas *locate test.txt* no te devuelve nada. Que ha pasado? Porqué no sale?
- NO has actualizado con *updatedb*. 
- Después de actualizar la bbdd ya nos devuelve su ruta absoluta

### 5.Busque el archivo de prueba que creó anteriormente, utilizando el comando find. ¿Qué sintaxis uso y cuál es la ruta absoluta?

- sudo find / -iname "test.txt"
- Si le pasamos el comando **time** antes de cada opción, tanto en locate como con find, nos damos cuenta que con locate es mucho mas rápido. 

## Ejercicios exploratorios

### 1.Hay un comando en la tabla anterior que no tiene una página man. ¿Cuál es y por qué cree que el comando no tiene una página de manual?

- El comando `cd` en bash, que se utiliza para cambiar de directorio, es un comando interno (built-in) del propio intérprete de comandos bash. Al ser parte del intérprete, no tiene una página de manual independiente como otros comandos externos.

- Los comandos internos son implementados directamente dentro del intérprete de comandos, en este caso, bash. Esto significa que no se trata de programas independientes que se ejecuten por sí mismos, sino de funcionalidades incorporadas en el intérprete de comandos mismo.

- Como el comando `cd` es una característica básica y esencial de bash, la documentación y las explicaciones sobre cómo utilizarlo se encuentran generalmente en la documentación general de bash o en el manual de referencia de bash. Puedes acceder a la página de manual de bash ejecutando `man bash` en tu terminal, donde encontrarás información detallada sobre el uso del comando `cd` y otros comandos internos de bash.

- Si bien el comando `cd` no tiene su propia página de manual separada, sigue siendo una parte fundamental y ampliamente utilizada de la funcionalidad de bash para la navegación y gestión de directorios.

### 2.Muestre en la pantalla el directorio de trabajo actual, incluidas las subcarpetas.
$ ls -R

### 3.Busque dentro del árbol todos los archivos que terminan con un número., Busque en el árbol todos los archivos que terminen con un número.
$ find ~ -name "*[0-9]"
$ locate "*[0-9]"

### 4.Elimine todo el árbol de directorios con un solo comando
$ rm -R Directorio Test test.txt 

## Resumen

*En esta lección usted aprendió:*

- Cómo obtener ayuda?
- Usar el comando man
- Navegar por la página man
- Diferentes secciones de la página man
- Usar el comando info
- Navegar entre diferentes nodos
- Buscar archivos dentro del sistema

Comandos utilizados en los ejercicios:
- man **Muestra una página de manual.**
- info **Muestra una página de información.**
- locate **Busca en la base de datos locate archivos con un nombre específico.**
- find **Busca en el sistema de archivos nombres que coincidan con un conjunto de criterios seleccionados.**
- updatedb **Actualiza la base de datos locate**

# 2.1 Aspectos básicos de la línea de comandos
## Ejercicios guiados

### 1. Cree una variable local number.
$ number=5

### 2. Cree una variable de entorno ORDER, utilizando uno de los métodos anteriores.
export ORDER=desc

### 3. Muestre los nombres de las variables y sus contenidos.
##### echo number    ----> No lleva comillas
number
##### echo ORDER     ----> Ni el simbolo dolar $, por lo tanto echo devuelve lo que le pasas
ORDER
##### echo $number   ----> Al pasarle el $ le pedimos que nos de el valor almacenado en esa variable
5
##### echo $ORDER
desc

### 4. ¿Cuáles son los ámbitos de las variables creadas anteriormente?
- El ámbito de la variable local number es sólo el shell actual.
- El ámbito de la variable de entorno ORDER es el shell actual y todos los subshells generados
por este.

## Ejercicios exploratorios

### 1. Cree una variable local nr_files y asignele el número de líneas encontradas en el archivo /etc/passwd. Sugerencia: mire el comando wc y la sustitución de comandos, tampoco se olvide de las comillas.

´nr_files="wc -l /etc/passwd"´  ----> Al pasar el comando entre comillas asigna a la variable
 la selida del comando.

### Resumen

En esta lección, usted aprendió:
* Tipos de variables
* Crear variables
* Manipular variables

Comandos utilizados en los ejercicios:
*env*
Muestra las variables de entorno actual.

*echo*
Salida de texto.

*export*
Hace que las variables locales estén disponibles para los subprocesos.

*unset*
Elimina una variable.