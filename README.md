# Práctica de tomcat
## Pasos a seguir para ejecutarla
### Carpeta "manual"
Hay que abrir docker y visual studio, en el visual se abre una nueva terminal, donde nos posicionamos en la carpeta "manual" mediante el comando "cd" y ejecutamos el comando: docker build -t nombrequesea . y se creará una imagen. Esa imagen la ejecutamos y se nos creará un contenedor, ya solo falta abrirlo en el navegar en el puerto 8080 y listo.

### Carpeta "automático"
Hay que ejecutarla de la misma que en la carpeta anterior, pero a ser posible pone de nombre de la imagen "automcat" que servirá para la próxima parte

### Carpeta "parte3"
Abrimos docker y visual, abrimos una nueva terminal, comrpobamos que hay una imagen ya creada denominada "automcat" y sino crearla (parte anterior) y ejecutamos el comando docker compose up. Ya solo resta abrir el navegador en el puerto 8080.
