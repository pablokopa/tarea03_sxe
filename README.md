# TAREA_03 - DOCKER

### 1. Descarga la imagen 'httpd' y comprueba que está en tu equipo.
Para descargar la imagen de **httpd** desde el repositorio de **Docker**:
```bash
docker pull httpd
```
Para comprobar si la imagen está instalada se utiliza:
```bash
docker images
```
### 2. Crea un contenedor con el nombre 'dam_web1'.
Para crear un contenedor de httpd con nombre **dam_web1** se utiliza:
```bash
docker run -d --name dam_web1 -p 8000:80 -v /home/accesodatos/Escritorio/sxe/ejercicio02_docker:/usr/local/apache2/htdocs httpd
```
Crea y ejecuta el contenedor asignando el puerto 8000 del equipo al puerto 80 del contenedor.
### 3. Si quieres poder acceder desde el navegador de tu equipo, ¿que debes hacer?
Simplemente utilziar la siguiente URL en el navegador:
```text
http://localhost:8000
```
### 4. Realiza un 'hola mundo' en html y comprueba que accedes desde el navegador.
```html
<!DOCTYPE html>
<html>
  <head>
    <title>WEB EJEMPLO</title>
  </head>
  <body>
  	<h1> Hola Mundo </h1>
  	<p> Me llamo Pablo </p>
  </body>
</html>
```
Utilizando la URL del apartado anterior se puede acceder sin problema al navegador y comprobar el resultado.
### 5. Crea otro contenedor 'dam_web2' con el mismo bind mount y a otro puerto, por ejemplo 9080.
Para crear otro contenedor de httpd con nombre **dam_web2** y diferente puerto se utiliza:
```bash
docker run -d --name dam_web2 -p 9080:80 -v /home/accesodatos/Escritorio/sxe/ejercicio02_docker:/usr/local/apache2/htdocs httpd
```
### 6. Comprueba que los dos servidores 'sirven' la misma página, es decir, cuando consultamos en el navegador: 
Para comprobar el correcto fucnionamiento de **dam_web1** y de **dam_web2** se utiliza:
```text
http://localhost:9080 
http://localhost:8000
```
En mi caso ambos funcionan correctamente y sin problemas.
### 7. Realiza modificaciones de la página y comprueba que los dos servidores 'sirven' la misma página
Tras haber realizado pequeñas modificaciones, puedo confirmar que el funcionamiento es perfecto y que ambos servidores sirven a la misma página.
