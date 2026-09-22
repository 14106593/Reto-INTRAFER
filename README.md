# Reto Intrafer — rompecabezas interactivo

Página estática (HTML puro, sin dependencias de servidor) lista para subir a GitHub y publicar con GitHub Pages.

## Archivos

- `index.html` — el juego completo (cronómetro, arrastrar y soltar, pista, ficha informativa al ganar).
- `puzzle.jpg` — imagen que se arma como rompecabezas.
- `info.jpg` — ficha informativa que se muestra al completarlo.
- `unipharm-logo.png` / `intrafer-logo.jpg` — logos usados en la página.

Todo el CSS y JavaScript está dentro de `index.html`, así que solo necesitas estos 5 archivos.

## Subirlo a GitHub

1. Crea un repositorio nuevo en GitHub (por ejemplo `reto-intrafer`). Puede ser público o privado (para Pages gratis en repos privados necesitas cuenta GitHub Pro/Team/Enterprise; con repo público funciona en cualquier plan).
2. Sube estos 5 archivos a la raíz del repositorio (arrastrándolos en la web de GitHub, o con git):
   ```bash
   git init
   git add .
   git commit -m "Reto Intrafer: rompecabezas interactivo"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/reto-intrafer.git
   git push -u origin main
   ```
3. En el repositorio, ve a **Settings → Pages**.
4. En "Build and deployment", selecciona **Deploy from a branch**, rama `main`, carpeta `/ (root)`, y guarda.
5. Espera 1–2 minutos; GitHub te dará una URL tipo:
   `https://TU-USUARIO.github.io/reto-intrafer/`

Esa es la página pública que puedes compartir.

## Editar después

Puedes editar `index.html` directamente en GitHub (ícono de lápiz) o clonando el repo y editando localmente. Los puntos más comunes que vas a querer tocar:

- **Textos**: título, subtítulo y pista están cerca del inicio del `<body>` (dentro de `<div class="wrap">`).
- **Colores**: variables CSS al inicio del `<style>` (`--maroon`, `--teal`, `--gold`, etc.).
- **Tamaño del rompecabezas**: variable `var N = 4;` en el `<script>` (4 = 4x4 = 16 piezas). Cambiarla a 3 da 9 piezas, a 5 da 25 piezas.
- **Imágenes**: reemplaza `puzzle.jpg` o `info.jpg` por otras (mismo nombre de archivo) para cambiar el producto sin tocar el código.

Cualquier cambio que subas a `main` se refleja solo en la URL de GitHub Pages, no hace falta reconfigurar nada.
