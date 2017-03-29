# Búsquedas
![Redes](header_redes.svg)

Las herramientas de búsqueda basadas en la terminal son extremadamente potentes, ya que poseen una multitud de filtros y opciones que las adaptan a casi cualquier necesidad. 



## find

El comando find es una de las herramientas más utilizadas en este segmento por su gran flexibilidad y potencia. 

####Sintaxis
`find [ruta] (opciones)`

####Opciones de uso frecuente
El comando tiene muchas opciones, aunque sólo se listan algunas que permiten discriminar **búsquedas** por **nombre** (-name), por **tipo** (-type) y **tamaño** (-size) y por **tiempo**

##### name
Explicita los términos de búsqueda, los cuales deben encerrarse entre comillas simples (' ') o dobles (" ")

#####type
Indica el tipo de recurso a buscar

| Opciones | Descripción                              |
| -------- | ---------------------------------------- |
| b        | Bloque (asociado a dispositivos de almacenamiento) |
| c        | Carácter                                 |
| d        | Directorio                               |
| f        | Archivo                                  |
| l        | Enlace simbólico                         |

##### Tamaño
Busca archivos según su tamaño, el cual puede expresarse en kilobytes (k), megabytes (M) ó gigabytes (G)

##### Tiempo
| Opciones | Descripción                              |
| -------- | ---------------------------------------- |
| -atime   | Indica la última lectura a un archivo (horas) |
| -mtime   | Indica la última modificación a un archivo (horas) |
| -amin    | Indica la última lectura a un archivo (minutos) |
| -mmin    | Indica la última modificación a un archivo (minutos) |

####Ejemplos

`# find /etc -name "*.conf"` 
Busca en el directorio `/etc` todos los archivos que finalicen con la extensión `.conf`

`# find / -type d -name "samba"` 
Busca en el directorio raíz todos las carpetas que contengan el nombre "samba"

`$ find . -size +100k`
Busca en el directorio actual, todos los archivos con un tamaño mayor a 100 kilobytes

`$ find -mtime +2`
Busca los archivos modificados hace más de dos días

`$ find -amin +2 -amin -5`
Busca los archivos leídos hace más de dos minutos y menos de cinco minutos




## grep

El comando grep es una herramienta que permite filtrar el contenido de la salida de un programa, a la vez que permite realizar búsquedas en archivos utilizando expresiones regulares

####Sintaxis
`grep ("cadena de caracteres") (archivo)`

`(comando) | grep ("cadena de caracteres")`

####Opciones de uso frecuente
| Opciones | Descripción                              |
| -------- | ---------------------------------------- |
| -i       | No distingue entre mayúsculas y minúsculas |
| -l       | Se detiene en la primer coincidencia encontrada |
| -w       | Muestra sóo coincidencias exactas        |
| -v       | Excluye de la búsqueda un patrón determinado |
| -n       | Muestra el número de línea en la que se encuentran las coincidencias |
| -e       | Permite búsquedas con expresiones regulares complejas |

#### Ejemplos

`$ grep -i "algo" textoImportante.txt` 
Busca la palabra algo, sin discriminar entre mayúsculas y minúsculas dentro del archivo textoImportante.txt

`$ ls -l | grep "server"` 
Toma la salida del comando `ls -l` y buscar archivos que contengan la palabra "server"





## Expresiones regulares

Tambien conocidas como _regex_, es un conjunto de caracteres que forman un patrón de búsqueda. A continuación se listan algunas de ellas junto con ejemplos relacionados con comandos. 

| Expresión regular | Descripción                              |
| ----------------- | ---------------------------------------- |
| .                 | Cualquier caracter                       |
| ?                 | Indica un caracter                       |
| *                 | Cualquier grupo de caracteres            |
| ~                 | Representa el directorio `home` del usuario actual |
| ^                 | Indica el comienzo de una línea          |
| $                 | Expresa el final de una línea            |
| [^  ]             | Corresponde a todos los caracteres exceptuando a los que se encuentran entre corchetes |
| \                 | Omite el significado de una expresión    |
| { }               | Indican agrupación de funciones          |
| [ ]               | Determinan un rango de valores           |
| ( )               | Indican opciones                         |
| !                 | Expresa negación                         |

