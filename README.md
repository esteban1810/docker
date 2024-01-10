# DOCKER

## Introducción
Ejecuta y si no existe instala, y luego ejecuta  
`docker run <nombre_imagen>`

Enlista las imagenes descargadas  
`docker image ls`

Contenedores en ejecución  
`docker ps`

Contenedores detenidos   
`docker ps -a`

Abrir terminal del sistema operativo  
`docker run -it ubuntu`

## Terminal Linux
Muestra los archivos del directorio actual  
`ls`

Muestra la ruta actual  
`pwd`

Muestra el usuario al actual  
`whoami`

Imprimir datos  
`echo <dato>`

Muestra la shell actual   
`echo $0`

Puedes buscar algún comando que hayas ejecutado. Si lo vuelves a presionar busca otra incidencia   
`command + R`

Listado de los últimos comandos que hayas ejecutado.   
`history`

El comando `history` devuelve un listado de los comandos ejecutados recientemente con número secuencial. Si queremos ejecutar uno de esos comando sin necesidad de escribirlo basta con escribir `!` seguido del número del comando  
`!5`

Muestra todos los archivos en lista  
`ls -1`

Muestra todos los archivos con más detalle  
`ls -l`

Crea un directorio  
`mkdir <nombre_directorio>` 

Mueve un archivo   
`mv <archivo_mover> <ruta_destino>`  

Crea archivo. Se pueden crear multiples archivos con este comando.  
`touch <nombre_archivo> <nombre_archivo2`

Eliminar archivos.  
`rm`  

El `*` nos permite eliminar incidencias.  
`rm a*.txt`

Sirve para eliminar directorios con su contenido. `-r` pertenece a recursivo.  
`rm -r <nombre_directorio`

Muestra el contenido del archivo  
`cat <nombre_archivo>` 

Muestra un fragmento del archivo y se mueve por porcentaje usando las flechas.  
`more <nombre_archivo>` 

Muestra un fragmento del archivo y se mueve por línea usando las flechas.  
`less <nombre_archivo>`  

Muestra las `n` primeras líneas del archivo.  
`head -n <numero> <nombre_archivo>` 

Muestra las `n` últimas líneas del archivo.  
`tail -n <numero> <nombre_archivo>` 

Muestra en tiempo real las líneas que se agreguen al archivo.  
`tail -f <nombre_archivo>`

### Redirecciones
`>` con este simbolo se puede enviar un dato hacia un archivo especifico

Se puede concatenar el contenido de dos archivos en uno sólo.  
`cat <nombre_archivo1> <nombre_archivoN> > <nombre_archivo_result>`

**Más Ejemplos**  
Estamos mostrando todos los archivos incluidos los ocultos con `-a`, además con el `l` a un lado estamos mostrando el detalle de cada archivo contenido y lo estamos enviando a `<nombre_archivo>`  
`ls -al <nombre_carpeta> > <nombre_archivo>`

Redirecciona y concatena el dato a un archivo existente `>>`  
```
root@c482c309ec1e:/# echo Vamos bien >> ejemplo3
root@c482c309ec1e:/# cat ejemplo3
Vamos bien
root@c482c309ec1e:/# echo Vamos bien >> ejemplo3
root@c482c309ec1e:/# cat ejemplo3 
Vamos bien
Vamos bien
root@c482c309ec1e:/# echo Vamos bien >> ejemplo3
root@c482c309ec1e:/# cat ejemplo3 
Vamos bien
Vamos bien
Vamos bien
```

Redireccionar datos que contengan errores. Si no se usa para los errores, no se redireccionará al archivo `2>`
```
root@c482c309ec1e:/# cat 124 > ejemplo4
cat: 124: No such file or directory
root@c482c309ec1e:/# cat ejemplo4
root@c482c309ec1e:/# cat 124 2> ejemplo4
root@c482c309ec1e:/# cat ejemplo4
cat: 124: No such file or directory
```

Redireccionar datos que contengan errores cómo de exito en un mismo archivo `2>&1`
```
root@c482c309ec1e:/# cat ejemplo2 > ejemplo5 2>&1
root@c482c309ec1e:/# cat ejemplo5
-rw-r--r-- 1 root root 4030 Jan 10 06:14 ejemplo
root@c482c309ec1e:/# cat ejemplo21324 >> ejemplo5 2>&1
root@c482c309ec1e:/# cat ejemplo5
-rw-r--r-- 1 root root 4030 Jan 10 06:14 ejemplo
cat: ejemplo21324: No such file or directory
```


#### Apt
Instalación de dependencias  
`apt install`

Desintalación de dependencias  
`apt remove`

Lista todas las dependencias instaladas  
`apt list`

Desinstala paquetes que no se usen  
`apt autoremove`

Actualiza la lista de paquetes (Nuevos o actualizaciones)  
`apt update`