# 🌻 Flores Amarillas para Ana Madeley

Página web con **cuenta regresiva animada** hasta el 21 de septiembre (Día de las Flores Amarillas). Al llegar la fecha, se revela automáticamente una animación de flores amarillas cayendo, un mensaje personalizado y música de fondo.

## Contenido
- `index.html`: todo el proyecto (HTML + CSS + JS) en un solo archivo, listo para GitHub Pages.
- `assets/music.mp3`: **debes agregar tú este archivo** (ver abajo).

## Cómo subirlo a GitHub Pages (paso a paso)

1. Crea un repositorio nuevo en GitHub, por ejemplo `flores-amarillas-ana`.
2. Sube el archivo `index.html` a la raíz del repositorio.
3. Crea una carpeta `assets/` y sube ahí tu archivo de música con el nombre exacto `music.mp3`.
4. Ve a **Settings → Pages** del repositorio, selecciona la rama `main` y la carpeta `/root`, guarda.
5. En unos minutos tu página estará disponible en `https://tu-usuario.github.io/flores-amarillas-ana/`.

## Agregar la música

Por límites del entorno no pude descargar un archivo de audio por ti, así que debes colocar uno manualmente:

1. Consigue una canción libre de derechos (por ejemplo en [Pixabay Music](https://pixabay.com/music/), [Uppbeat](https://uppbeat.io/) o la [YouTube Audio Library](https://www.youtube.com/audiolibrary)). Busca algo alegre tipo "happy", "spring" o "acoustic".
2. Descárgala en formato `.mp3` y renómbrala exactamente a `music.mp3`.
3. Colócala dentro de una carpeta llamada `assets` en el repositorio (ruta final: `assets/music.mp3`).
4. Si prefieres usar una canción con derechos (por ejemplo alguna especial para Ana), solo tú puedes subirla porque no puedo reproducir contenido con copyright; asegúrate de tener permiso de uso.

Nota: los navegadores bloquean el autoplay de audio sin interacción del usuario. Por eso la página incluye un botón "🎵 Activar música" y también intenta reproducir automáticamente cuando llega la fecha (puede requerir un clic si el navegador lo bloquea).

## Personalizar

Dentro de `index.html` puedes ajustar:

- **Fecha objetivo**: variable `TARGET_DATE` en el `<script>` (formato `"2026-09-21T00:00:00-05:00"`, ya configurada en hora de Perú).
- **Nombres y mensaje**: textos dentro de `#countdown-screen` y `#final-screen`.
- **Colores**: variables CSS `--amarillo`, `--amarillo2`, `--naranja` al inicio del `<style>`.
- **Cantidad de flores**: número en `Array.from({length: 26}, ...)` (fondo) y `{length: 70}` (explosión final) dentro del script.

## Qué verá Ana

1. Mientras falten días, verá un contador en vivo (días, horas, minutos, segundos) con fondo animado en degradado y pétalos amarillos cayendo suavemente.
2. Justo al llegar el 21 de septiembre (hora de Perú), la pantalla cambia automáticamente: aparece una lluvia intensa de flores amarillas, un mensaje de "¡Feliz Día de las Flores Amarillas!" y la firma "Con cariño, Renato." además de la música de fondo.
