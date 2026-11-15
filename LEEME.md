# Sitio del Grupo de Investigación en Ecología Jurídica

Sitio estático en Jekyll, publicado gratis con GitHub Pages. Los integrantes publican desde un panel web (Pages CMS) sin tocar archivos, y las discusiones del seminario funcionan con giscus sobre GitHub Discussions.

## Qué hay en cada carpeta

| Carpeta o archivo | Contenido |
|---|---|
| `_articulos/` | Un archivo `.md` por artículo |
| `_notas/` | Un archivo `.md` por nota |
| `_discusiones/` | Un archivo por discusión (el planteamiento; las intervenciones viven en GitHub Discussions) |
| `_integrantes/` | Un archivo por integrante |
| `_lineas/` | Un archivo por línea de interés |
| `_data/sitio.yml` | Nombre, institución, lema, contacto y presentación del grupo |
| `_data/proyecto.yml` | Proyecto colectivo: descripción, preguntas y fases |
| `assets/archivos/` | PDF e imágenes que se suban desde el panel |
| `.pages.yml` | Configuración del panel de edición |

Todo lo que aparece entre corchetes o marcado «[Ejemplo]» es un lugar reservado para reemplazar o borrar.

## Puesta en marcha

### 1. Crear el repositorio
En GitHub, crear un repositorio **público** llamado `grupo-de-investigacion-en-ecologia-juridica` y subir allí todos estos archivos, incluido `.pages.yml`, que empieza por punto y algunos sistemas ocultan.

Si el repositorio se llama distinto, cambiar `baseurl` en `_config.yml` por `/nombre-del-repositorio`.

### 2. Activar GitHub Pages
En el repositorio: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)`. A los pocos minutos el sitio queda en `https://lorenzoriano8-png.github.io/grupo-de-investigacion-en-ecologia-juridica/`.

### 3. Activar el panel de edición
Entrar a https://app.pagescms.org con la cuenta de GitHub, autorizar la aplicación en el repositorio y abrirlo. Desde la sección de colaboradores se invita por correo a cada integrante; no necesitan cuenta de GitHub. Cada vez que alguien guarda, el sitio se reconstruye solo.

### 4. Activar las discusiones
1. **Settings → General → Features**: marcar **Discussions**.
2. En la pestaña **Discussions**, crear una categoría llamada `Discusiones del grupo`, de tipo **Announcement** (así solo los administradores y giscus abren hilos; los demás responden).
3. Instalar la aplicación giscus en el repositorio: https://github.com/apps/giscus
4. En https://giscus.app/es escribir `USUARIO/grupo-de-investigacion-en-ecologia-juridica`, elegir la categoría y copiar los valores `data-repo-id` y `data-category-id`.
5. Pegarlos en `_config.yml`, sección `giscus`, junto con `repo: "lorenzoriano8-png/grupo-de-investigacion-en-ecologia-juridica"`.

Para intervenir en una discusión hay que iniciar sesión con una cuenta de GitHub (es gratuita).

### 5. Dominio propio (opcional, después)
Comprar el dominio, ponerlo en **Settings → Pages → Custom domain**, seguir las indicaciones de DNS de GitHub y dejar `baseurl: ""` en `_config.yml`.
