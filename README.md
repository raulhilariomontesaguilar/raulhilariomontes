# Nombre Artista — Sitio web

Web minimalista para artista contemporáneo.
Diseño tipo archivo / publicación.

---

## Archivos incluidos

```
index.html          → Página de inicio (cuadrícula de proyectos)
projects.html       → Lista de todos los proyectos
project-01.html     → Página individual de proyecto (plantilla)
project-02.html     → Segundo ejemplo de proyecto
texts.html          → Textos / ensayos
cv.html             → Currículum
info.html           → Información / contacto
style.css           → Toda la estética visual
images/             → Carpeta donde van tus imágenes
```

---

## Cómo añadir un proyecto nuevo

### 1. Crea la página del proyecto

Duplica el archivo `project-01.html` y renómbralo, por ejemplo `project-04.html`.

Edita dentro:
- El título en `<title>` (línea 5)
- El `<h1>` con el título del proyecto
- La `<span class="year">` con el año
- El texto dentro de `<div class="project-text">`
- Las imágenes dentro de `<div class="project-images">`

### 2. Añade la tarjeta en el índice

En `index.html` y en `projects.html`, copia este bloque y pégalo dentro de `<section class="project-list">`:

```html
<article class="project-item">
  <a href="project-04.html">
    <div class="project-cover">
      <img src="images/project-04-cover.jpg" alt="Título del proyecto">
    </div>
    <div class="project-meta">
      <span class="project-title">Nuevo Proyecto</span>
      <span class="project-year">2025</span>
    </div>
  </a>
</article>
```

### 3. Añade las imágenes

Coloca las imágenes en la carpeta `images/`.

Nombres sugeridos:
- `project-04-cover.jpg` → imagen de portada (aparece en la cuadrícula)
- `project-04-img-01.jpg`, `project-04-img-02.jpg`, etc. → imágenes interiores

Formatos recomendados: JPG o WebP.
Tamaño: portadas entre 800–1200px de ancho. Interiores: hasta 2000px.

---

## Tipografía

El CSS usa **Josefin Sans** (Google Fonts, gratuita), que tiene un trazo cercano a Museo Sans.

Si tienes licencia de **Museo Sans** vía Adobe Fonts:
1. Crea un kit en fonts.adobe.com e incluye Museo Sans.
2. En `style.css`, sustituye la línea `@import url(...)` por el `<link>` de Adobe Fonts.
3. Cambia `--font` a `'museo-sans', sans-serif;`.

---

## Colores y espaciado

Todo el diseño se controla desde las variables CSS al inicio de `style.css`:

```css
:root {
  --color-text: #111111;    /* texto principal */
  --color-muted: #888888;   /* años, labels, nav inactivo */
  --color-border: #e0e0e0;  /* líneas finas */
  --page-padding: 2.5rem;   /* márgenes laterales */
}
```

---

## Publicar el sitio

Esta web es HTML/CSS estático: no necesita servidor ni base de datos.

Opciones gratuitas y rápidas:
- **GitHub Pages**: sube los archivos a un repositorio público y activa Pages.
- **Netlify**: arrastra la carpeta del proyecto al panel de Netlify.
- **Vercel**: conecta el repositorio y despliega en un clic.

El dominio propio se configura en cada plataforma una vez publicado.

---

## Estructura de imágenes recomendada

```
images/
  project-01-cover.jpg
  project-01-img-01.jpg
  project-01-img-02.jpg
  project-02-cover.jpg
  project-02-img-01.jpg
  ...
  portrait.jpg   (opcional, para la página Info)
```
