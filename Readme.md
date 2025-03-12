

# Nombre del Proyecto




Descripción breve del proyecto. Explica qué hace, su propósito y a quién está dirigido.




## Tabla de Contenidos




- [Características](#características)


- [Instalación](#instalación)


- [Uso](#uso)


- [Pruebas](#pruebas)


- [Lanzamiento de la Versión 1.0](#lanzamiento-de-la-versión-10)


- [Changelog](#changelog)


- [Contribuciones](#contribuciones)


- [Licencia](#licencia)


- [Contacto](#contacto)




## Características




- **Característica 1**: Descripción de la característica 1.


- **Característica 2**: Descripción de la característica 2.


- **Característica 3**: Descripción de la característica 3.




## Instalación


Instrucciones sobre cómo instalar y configurar el proyecto.


## Uso




Instrucciones sobre cómo usar el proyecto. Incluye ejemplos si es posible.


1. Ejecuta el proyecto con el comando correspondiente



```bash


# Clonar el repositorio


git clone https://github.com/usuario/nombre-del-repo.git


# Navegar al directorio del proyecto


cd nombre-del-repo


# Instalar dependencias


npm install  # o el comando correspondiente para tu proyecto


```

---------


# Guía de Git: Revertir un Commit y Hacer un Merge


Este documento proporciona instrucciones sobre cómo revertir un commit y cómo hacer un merge de una rama a otra en Git. Estas son operaciones comunes que pueden ser útiles en el flujo de trabajo de desarrollo.


## Tabla de Contenidos


- [Revertir un Commit](#revertir-un-commit)

- [Hacer un Merge de una Rama a Otra](#hacer-un-merge-de-una-rama-a-otra)

- [Ejemplo Completo](#ejemplo-completo)


## Revertir un Commit en la rama interface


Revertir un commit significa deshacer los cambios introducidos por ese commit, creando un nuevo commit que revierte esos cambios.

Necesitaremos utilizar este rever para un commit echo por Damian en este determinado proyecto


### Pasos para Revertir un Commit

#### En caso de querer realizarlo por consola

1. **Identificar el Commit**: Usa el comando `git log` para ver el historial de commits y encontrar el hash del commit que deseas revertir. Busca el hash del commit (una cadena larga de caracteres) que deseas revertir.


2. **Revertir el Commit**: Ejecuta el comando `git revert COMMIT_HASH`, reemplazando `COMMIT_HASH` con el hash del commit que deseas revertir. Esto abrirá tu editor de texto para que puedas escribir un mensaje de commit. Guarda y cierra el editor para completar el revert.


3. **Confirmar el Revert**: Verifica que el commit ha sido revertido correctamente usando el comando `git log`.

#### En caso de querer realizarlo por intuicion


![Commit revertido](revert%20commit.png)


## Hacer un Merge de una Rama a Otra


Hacer un merge significa combinar los cambios de una rama en otra. Esto es útil para integrar características o correcciones de errores.


### Pasos para Hacer un Merge


1. **Cambiar a la Rama de Destino**: Primero, asegúrate de estar en la rama a la que deseas hacer el merge. Por ejemplo, si deseas hacer merge en la rama `main`, usa el comando `git checkout main`.


2. **Hacer el Merge**: Ejecuta el comando `git merge NOMBRE_DE_LA_RAMA`, reemplazando `NOMBRE_DE_LA_RAMA` con el nombre de la rama que deseas fusionar.


3. **Resolver Conflictos (si es necesario)**: Si hay conflictos durante el merge, Git te lo indicará. Deberás resolver los conflictos manualmente en los archivos afectados. Después de resolver los conflictos, agrega los cambios usando `git add .` y completa el merge con `git commit`.


4. **Verificar el Merge**: Asegúrate de que el merge se haya realizado correctamente revisando el historial de commits con el comando `git log`.


## Ejemplo Completo


Supongamos que tienes un commit con el hash `abc123` que deseas revertir y una rama llamada `feature` que deseas fusionar en `main`.


1. **Revertir el Commit**: Usa `git log` para encontrar el hash del commit y luego ejecuta `git revert abc123`.


2. **Hacer Merge de la Rama `feature` en `main`**: Cambia a la rama `main` usando `git checkout main` y luego ejecuta `git merge feature`.


3. **Resolver Conflictos (si es necesario)**: Si hay conflictos, edita los archivos con conflictos, agrega los cambios y completa el merge.




---------

## Lanzamiento de la Versión 1.0




### 1. Preparar tu proyecto




Asegúrate de que tu proyecto esté listo para ser lanzado. Esto incluye:




- Revisar el código y asegurarte de que no haya errores.


- Actualizar la documentación (README.md).


- Asegurarte de que todas las pruebas pasen (si tienes pruebas automatizadas).




### 2. Crear una nueva etiqueta (tag)




Las versiones en GitHub se suelen gestionar mediante etiquetas. Para crear una etiqueta para la versión 1.0, sigue estos pasos:




1. Abre tu terminal o línea de comandos.


2. Navega al directorio de tu proyecto.


3. Asegúrate de que todos los cambios estén confirmados (committed).


4. Crea una nueva etiqueta con el siguiente comando:


git tag -a v1.0 -m "Release version 1.0"


Aquí, -a indica que estás creando una etiqueta anotada, y -m permite agregar un mensaje a la etiqueta.




### 3. Subir la etiqueta a GitHub




Después de crear la etiqueta, debes subirla a tu repositorio en GitHub usando el siguiente comando:


git push origin v1.0




### 4. Crear una nueva versión en GitHub




1. Ve a tu repositorio en GitHub.


2. Haz clic en la pestaña "Releases" (Lanzamientos).


3. Haz clic en "Draft a new release" (Borrador de un nuevo lanzamiento).


4. Selecciona la etiqueta que acabas de crear (v1.0).


5. Completa el título y la descripción de la versión. Puedes incluir notas sobre los cambios, nuevas características, correcciones de errores, etc.


6. Haz clic en "Publish release" (Publicar lanzamiento).




### 5. (Opcional) Crear un changelog




Si deseas, puedes crear un archivo CHANGELOG.md en tu repositorio para documentar los cambios en cada versión.




### 6. Comunicar el lanzamiento




Finalmente, si tienes una comunidad o usuarios que siguen tu proyecto, considera anunciar el lanzamiento a través de tus canales de comunicación (como redes sociales, foros, etc.).




## Changelog




### [v1.0] - YYYY-MM-DD


- Lanzamiento inicial.


- Implementación de la característica 1.


- Corrección de errores en la funcionalidad X.


- Mejora en la documentación.




## Contribuciones




Si deseas contribuir, por favor sigue estos pasos:




1. Haz un fork del proyecto.


2. Crea una nueva rama (git checkout -b feature/nueva-caracteristica).


3. Realiza tus cambios y haz commit (git commit -m 'Añadir nueva característica').


4. Sube tus cambios (git push origin feature/nueva-caracteristica).




## Licencia




Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.




## Contacto




Tu nombre - tu-email@example.com




Enlace al proyecto en GitHub: https://github.com/usuario/nombre-del-repo
