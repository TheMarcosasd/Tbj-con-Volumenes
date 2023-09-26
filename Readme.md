# Trabajo con Volumenes de Docker
1. Necesitamos descargar una imagen httpd, usamos _docker pull httpd_
2. Para crear un contendor usamos (para mas info busca httpd en docker hub),usaremos el comando _*docker run -dit --name dam_httpd httpd:2.4*_ . Confirmamos que lo hicimos bien con el comando _*docker image ls -a*_
3. Lo primero seria saber la ip del dispositivo y el puerto en el cual se ha abierto el contenedor. En mi caso se pone la ip y despues el puerto_*10.0.9.10:8080*_
4. Para poder mover el directorio htdocs a otro usamos, _*docker run -it -p 8080:80 -v /home/dam/Escritorio/Notas-Clase/SXE/vol/apch:/usr/local/apache2/htdocs --name dam_httpd httpd*_
5. Ahora necesitamos ir a la carpeta, abrirla y crear un documento html. Una vez creado con el "comando" < p> escribimos el hola mundo cerramos < /p> y listo. Lo vemos poniendo nuestra ip junto al puerto que le pusimos (no te olvides de guardar el documento con los cambios).
6. Tenemos que crear otro contenedor -*docker run -dit --name dam_web2 -p 9080:80 httpd2.4*-