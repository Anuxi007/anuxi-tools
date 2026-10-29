# Anuxi Tools

Panel CEP para **Adobe After Effects** con herramientas para acelerar tareas de edición.

| | | |
|---|---|---|
| ![panel 1](https://github.com/user-attachments/assets/3abac933-ac46-42e9-90ab-2eb3873041d0) | ![panel 2](https://github.com/user-attachments/assets/95fecf32-8cb6-4bbb-8fe9-6df8b2f106d9) | ![panel 3](https://github.com/user-attachments/assets/f172ed2b-6837-4784-96a4-1a110b078066) |

## Qué incluye

**Editing**
- Motion Tile, ADJ/SLD (capa de ajuste o sólido), Twixtor Pro, Null por capa, Precomp (simple o con capa de ajuste), Center, Align.
- Cache: limpia RAM + caché en disco de After Effects (también borra el historial de deshacer).
- Organizer (ordena el proyecto por extensión y comps), Screenshot (captura del visor a la línea de tiempo), Splitter (divide una imagen en partes).

**Effects**
- Wiggle (Position/Rotation), Elastic, Bounce, Wiggle Loop, Reverse.
- Anchor Point, presets FFX (aplica tus propios `.ffx` desde una carpeta elegida).
- Paste IMG (pega una imagen del portapapeles), MP3 (extrae audio, usa `ffmpeg`), Audio Sync (copia una capa de audio a cada precomp, incluso anidadas, recortada al tiempo exacto).

**Remap**
- Reagroup, Precomp + rename (por lotes), Sequence Layers.

**3D**
- Add Camera según la selección, Cube rig, vista de cámara.

**Web**
- **Scene Search**: busca el anime/escena de una captura de pantalla (API de trace.moe).
- **YT Downloader**: descarga video/audio integrado, usa `yt-dlp` y `ffmpeg` (el propio panel los descarga e instala).

**Extras**
- **Subtítulos automáticos**: transcribe el audio de la composición y genera subtítulos usando Whisper (whisper.cpp), con varios modelos para elegir según precisión/velocidad.

**Personalización del panel**
- Favoritos/accesos personalizados arrastrando bloques a tu propio layout, con varios perfiles guardados.
- Nombre, color de acento, foto de perfil y banner, idioma (ES/EN/DE/RU/JA) y animaciones.
- **Backup**: exporta/importa un archivo con tus perfiles y favoritos, y los ajustes visuales del panel (las imágenes no se guardan dentro del archivo, solo se ofrecen de nuevo al importar).
- Actualizaciones: el panel revisa e instala nuevas versiones desde dentro de After Effects.

## Requisitos

- Adobe After Effects (16.0 o superior).
- Conexión a internet para Scene Search (API de trace.moe), YT Downloader, y la descarga de modelos de Subtítulos automáticos.

## Instalación

1. Descarga **[`AnuxiTools.zxp`](./AnuxiTools.zxp)** de este repositorio.
2. Instálalo con un instalador ZXP (por ejemplo [ZXP Installer](https://aescripts.com/learn/zxp-installer/) o [Anastasiy's Extension Manager](https://install.anastasiy.com/)) arrastrando el archivo `.zxp` sobre el programa.
   - Si prefieres instalarlo a mano sin un instalador ZXP, descomprime el `.zxp` (es un `.zip`) y copia la carpeta resultante a:
     - **Windows:** `C:\Program Files (x86)\Common Files\Adobe\CEP\extensions\` (o `%APPDATA%\Adobe\CEP\extensions\`)
     - **macOS:** `~/Library/Application Support/Adobe/CEP/extensions/`
3. Reinicia After Effects y abre el panel desde **Ventana > Extensiones > Anuxi Tools**.

> El `.zxp` incluido está firmado, así que no necesitas activar el modo debug de CEP para instalarlo con un instalador ZXP.

## Notas de uso

**Scene Search** (pestaña Web)
- Necesita conexión a internet.
- Para habilitar la captura de pantalla dentro de AE: **Preferencias > Scripting y expresiones > "Permitir que los scripts escriban archivos y accedan a la red"**.
- Guarda el proyecto antes de capturar: las imágenes se guardan en una carpeta `Scene Search Screenshots` junto al proyecto.

**YT Downloader** (pestaña Web, arriba de Scene Search)
- Usa `yt-dlp` y `ffmpeg`. La primera vez, abre el engranaje del bloque > Herramientas, y pulsa "Descargar / actualizar" (yt-dlp) e "Instalar" (ffmpeg).
- Descarga solo contenido que tengas derecho a usar.

**Subtítulos automáticos** (pestaña Extras)
- La primera vez necesita descargar el motor whisper.cpp y el modelo que elijas.
- Elige el modelo según tu equipo: los más grandes son más precisos pero más lentos.

**Dónde guarda sus datos el panel**
- Todo vive bajo `~/.anuxi-panels/`: los binarios compartidos (`ffmpeg`, `yt-dlp`) en `bin/`, y los datos propios de Anuxi Tools (ajustes, modelos de subtítulos, preferencias) en `anuxi-tools/`.
- Si venías de una versión anterior, el panel migra automáticamente lo que tenías en las carpetas viejas la primera vez que lo abres.

## Licencia

Uso personal / no comercial. Si quieres distribuirlo o modificarlo más allá de eso, contacta antes al autor.
