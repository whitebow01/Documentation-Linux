# GIT [Revisar documentacion](https://git-scm.com/book/es/v2) 
***
## Comandos Basicos Linux
| Comando | Utilidad | 
| -- | -- | 
| ls | Ver el contenido del directorio en el que se encuentra el prompt. | 
| cd directorio | Acceder al directorio. | 
| cd .. | Un paso atras del promp. | 
| pwd | Revisar donde estamos ubicados. | 
| mkdir nomrbecarpeta | Crear carpeta.|
| touch nombrefichero.py, js, html, css, etc  | Crear archivos vacíos y cambiar marcas de tiempo de archivos o carpetas|
| mv archivo.txt /ruta/de/destino | Mover archivos a directorios o carpetas |
| cat | Imprime por pantalla el fichero seleccionado |
| rm nombrearchivo | Eliminamos el archivo|
>Tambien se puede utilizar `ls` con el nombre de un directorio para ver el contenido.

***
## Indentificadores de colores
**Indentificador de colores, segun tipo de archivo/elemento:**
| Color | Referencia | 
| -- | -- | 
| Color azul | Carpetas | 
| Color verde | Archivos ejecutables | 
| Color azul celeste | Carpetas especiales de Windows | 
| Color blanco | Archivos (pdf, jpg, doc, md, js, etc.) | 
***

## Repositorio
Cuando empezamos en un nuevo equipo, necesitamos iniciar sesion en git para poder sincronizar con github o algun sv remoto

~~~
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"
~~~

### Comandos repositorio local (git) : 
>Normalmente mas usados:

Iniciar un repositorio local:
~~~
git init 
~~~
Agrega el repositorio a ***"STAYING AREA"***. "Por Confirmar" para luego transformarlo en un **COMMIT** (versión):
~~~
git add <archivo> 
~~~
O (si queremos agregar todos los cambios de todos los archivos del **Directorio** actual a ***"STAYING AREA"***):
~~~
git add . 
~~~
Agregar la versión al repositorio. (**-m = mensaje**):
~~~
git commit -m "mensajedeconfirmación" <archivo>
o 
git commit -a -m "amensajedeconfirmación"
~~~
Al agregar `-a` no es necesario hacer un `add .` antes. Se salta el area de preparacion.

### GitHub
Para subir los archivos al servidor Remoto debemos pasar por los estados de  **ADD** y **COMMIT**. (Comprobar con `git status`)

Para subir los cambios a **GITHUB** :
~~~
git push origin main
~~~
Nos pedira Clave o Key en ciertas ocasiones.

Sincronizar tu rama local con la rama remota
~~~
git pull origin ramaquequeremostraer(normal main)
~~~

### Revisar el Estado de tus Archivos
Revision **ESTADO** general del repositorio:
~~~
git status 
o
git status -s  
~~~
`-s` solamente muesta los ficheros en los cuales hubieron cambios y el estado en el que se encuentran.
>El comando te indica en cuál rama estás y te informa que ha variado con respecto a la misma rama en el servidor.
Tambien podemos usar 
~~~
git diff 
~~~
Este comando muestra las líneas exactas que fueron añadidas y eliminadas.

1. Revisaremos si se hicieron los cambios con `git status`.
***
### Historial se Confirmaciones
#### Git log
1. Luego revisaremos la version de commit con su identificador unico o **HASH** con su respectiva informacion:
~~~
git log 
o
git log --oneline
~~~
>El mecanismo que usa Git para generar esta suma de comprobación se conoce como hash SHA-1. Se trata de una cadena de 40 caracteres hexadecimales (0-9 y a-f), y se calcula con base en los contenidos del archivo o estructura del directorio en Git. Por ejemplo:
~~~
24b9da6552252987aa493b52f8696cd6d3b00373
~~~
>Git guarda todo no por nombre de archivo, sino por el valor hash de sus contenidos.

Tambien se puede hacer variantes de `git log` como :

| Comando log | Funcion | 
| -- | -- | 
| -p | Muestra las diferencias introducidas en cada confirmación. | 
| -2 | Se muestren únicamente las dos últimas entradas del historial. | 
| -p -2 | Diferencias y ultimas entradas del hitorial. | 
| --stat: | Estadísticas de cada confirmación. | 


#### Git log en ramas
git puede mostrar las versiones de rammas por separado. Distinto a git log que muestra todo el historial del proyecto.

[Ver mas sobre git en ramas](https://es.stackoverflow.com/questions/496506/como-mostrar-el-log-de-una-rama-espec%C3%ADfica-de-git-sin-mostrar-la-rama-master) 

Mostrar commits que hay en una rama pero en las otras no:
~~~
git log --oneline --graph master..ramaquequeremosverloscommits
~~~