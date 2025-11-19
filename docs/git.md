# 1 Creación y Configuración del Repositorio

## 1.1 Preparación Inicial 
```
git config --global user.name "rmartinn05"
git config --global user.email "rmartinn05@informatica.iesvalledeljerteplasencia.es"
git config --global init.defaultBranch main
```
###Creación de Clave SSH

Se genera una clave SSH para conectarse de forma segura con GitHub y se agrega al agente:

```
ssh-keygen -t ed25519 -C "rmartinn05@informatica.iesvalledeljerteplasencia.es"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

## 1.2 Creación y Clonación del Repositorio Remoto

Se crea un repositorio público en GitHub llamado: **`PPS-Unidad0-Tarea-RobertoMN`**

Luego se clona localmente:

```
git clone **git@github.com:vjp-robertoM/PPS-Unidad0-Tarea-Roberto.git**
cd **PPS-Unidad0-Tarea-Roberto**
```

## 1.3 Creación de la Estructura de Archivos

Se genera la estructura de carpetas y archivos necesaria:

``` 
# Crear archivos de documentación
touch docs/index.md docs/git.md docs/gitActions.md docs/gitPages.md docs/docker.md docs/conclusiones.md

# Archivos de configuración
touch mkdocs.yml requirements.txt

# WorkFlow de GitHub Actions
touch .github/workflows/CreacionDocumentacion.yml
```

## 1.4 Subida de archivos al repositorio

Se agregan los archivos al control de versiones, se confirma y se sube a la rama main:

```
# Añadir todos los archivos
git add .

# Confirmar cambios
git commit -m "feat: Inicializando estructura de la tarea y archivos de documentación"

# Subir al repositorio remoto
git push origin main
```
# 1.5  Obtenemos como resultado la creación de este repositorio en GitHub
![Captura GitHub](imagenes/captura1.png)
