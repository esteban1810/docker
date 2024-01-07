# docker

## Comandos
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

### Ubuntu
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