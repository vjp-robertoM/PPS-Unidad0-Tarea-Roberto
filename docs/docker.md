# 4 Creación de un Contenedor NGINX con Docker

## 4.1 Preparación de los archivos

Antes de crear el contenedor, es necesario cambiar a la rama `gh-pages` del repositorio:

```
cd PPS-Unidad0-Tarea-RobertoMN
git checkout gh-pages
```
## 4.2 Creación del contenedor docker

```
docker run -d \
  --name PPSUnidad0-Tarea_RobertoMN \
  -p 8085:80 \
  -v $(pwd):/usr/share/nginx/html \
  nginx
```
Explicación breve:
- `-d` → Ejecuta el contenedor en segundo plano.
- `--name` → Asigna un nombre al contenedor para identificarlo fácilmente.
- `-p 8085:80` → Mapea el puerto 80 del contenedor al 8085 de tu máquina.
- `-v $(pwd):/usr/share/nginx/html` → Monta el directorio actual (gh-pages) dentro del contenedor.
- `nginx` → Imagen oficial de NGINX de Docker Hub.
