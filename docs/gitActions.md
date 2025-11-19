# 2 Automatización con GitHub Actions y MkDocs

## 2.1 Configuración de MkDocs

Antes de automatizar con GitHub Actions, necesitamos configurar **mkdocs**, se necesita crear el archivo `requirements.txt` con las dependencias necesarias: `mkdocs`

La estructura de **mkdocs** debe ser esta:

![Captura mkdocs](imagenes/captura2.png)

---
## 2.2 Configuración del WorkFlow

El WorkFlow se ejecuta automáticamente con cada push a la rama main. Sus pasos principales son:
- Descargar el repositorio.
- Instalar Python y las dependencias de requirements.txt.
- Ejecutar MkDocs para compilar la documentación.
- Publicar automáticamente en la rama gh-pages.

![Captura workflow](imagenes/captura3.png)

---
## 2.3 Primer Commit y Ejecución

```
# Añadir archivos de configuración y WorkFlow
git add mkdocs.yml requirements.txt .github/workflows/CreacionDocumentacion.yml

# Confirmar cambios
git commit -m "Configuración inicial de MkDocs y WorkFlow"

# Subir a GitHub
git push origin main
```
---
## 2.4 Obtenemos como resultado la creación de GitHub-Pages

![Captura workflow](imagenes/captura4.png)
