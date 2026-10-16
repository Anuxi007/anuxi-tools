# Anuxi Tools

Panel CEP para **Adobe After Effects** con herramientas para acelerar tareas de edición: reagrupado y renombrado de capas, secuencias, búsqueda de escenas (Scene Search) y un descargador de video/audio integrado (YT Downloader).

| | | |
|---|---|---|
| ![panel 1](https://github.com/user-attachments/assets/3abac933-ac46-42e9-90ab-2eb3873041d0) | ![panel 2](https://github.com/user-attachments/assets/95fecf32-8cb6-4bbb-8fe9-6df8b2f106d9) | ![panel 3](https://github.com/user-attachments/assets/f172ed2b-6837-4784-96a4-1a110b078066) |

## Requisitos

- Adobe After Effects (16.0 o superior).
- Conexión a internet para Scene Search (API de trace.moe) y para el YT Downloader (usa `yt-dlp` y `ffmpeg`, que el propio panel puede descargar).

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
- Usa `yt-dlp` y `ffmpeg`. La primera vez, abre el engranaje del bloque > Herramientas, y pulsa "Descargar / actualizar" (yt-dlp) e "Instalar" (ffmpeg). Se guardan en `~/.ytdl-cep/bin`.
- Descarga solo contenido que tengas derecho a usar.

## Licencia

Uso personal / no comercial. Si quieres distribuirlo o modificarlo más allá de eso, contacta antes al autor.
