# Trabajo con Volumenes de Docker
1. Necesitamos descargar una imagen httpd, necesitamos ir a la _pagina web de docker_
2. Para crear un contendor tenemos que ver ne la pagina web, una vez alli usaremos el comando _*docker run -dit --name dam_httpd httpd:2.4*_ . Confirmamos que lo hicimos bien con el comando _*docker image ls -a*_
3. Lo primero seria saber la ip del dispositivo y el puerto en el cual se ha abierto el contenedor. En mi caso se pone la ip y despues el puerto_*10.0.9.10:8080*_
4. Para poder mover el directorio htdocs a otro usamos, _*docker run -p 8080:80 -v /home/dam/Notas-Clase/SXE:/usr/local/apache2/htdocs/*_