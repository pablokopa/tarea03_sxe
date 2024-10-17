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
docker run -it --name=dam_web1 httpd /bin/sh
```
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
