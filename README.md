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
