# Convertidor HTML ⇄ Illustrator (con biblioteca en GitHub)

## Puesta en marcha
1. Crea un repositorio **público** y sube `index.html`. Activa GitHub Pages (Settings › Pages › Deploy from branch › main / root). Tus editables se guardarán en la carpeta `editables/` del mismo repositorio.
2. En GitHub › Settings › Developer settings › Fine-grained tokens: crea un token limitado a ese repositorio, con permiso **Contents: Read and write**.
3. Abre tu página de GitHub Pages › pestaña «Mi biblioteca» › «Conexión con GitHub» y completa usuario, repositorio, rama, carpeta base y token.

El token se guarda solo en el localStorage de tu navegador (nunca en el repositorio).

## Almacenamiento
La barra superior muestra el espacio usado frente a 1 GB (tamaño recomendado por GitHub). Borrar archivos no libera espacio, porque el historial de Git los conserva.

## Token y acceso
Ver y descargar tus archivos (repositorio público) no requiere token. El token solo se usa para guardar, mover o borrar. Puedes fijar `owner` y `repo` en `GH_DEFAULT` dentro de `index.html`. No pongas el token en el código: en un repositorio público GitHub lo revoca automáticamente.

## Archivos .ai muy pesados
El .ai se lee por rangos (sin cargarlo entero en memoria) y las imágenes se recomprimen a WebP. Si el HTML resultante supera 100 MB, GitHub no lo acepta.
