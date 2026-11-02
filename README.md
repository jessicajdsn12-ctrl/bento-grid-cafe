# Grano Norte · Bento Grid Layout

Proyecto de diseño web responsive con interfaz estilo **Bento Box**, desarrollado utilizando **CSS Grid anidado**, variables CSS, tema claro/oscuro automático y sintaxis de CSS anidado nativo (*CSS Nesting*).

---

## 📋 Descripción del Proyecto

El proyecto consiste en una página promocional para una marca ficticia de café de especialidad (*Grano Norte*). El layout está estructurado mediante celdas dinámicas de tamaños heterogéneos (estilo Bento), distribuidas en tres secciones principales que se adaptan de forma fluida según el tamaño del viewport.

---

## ✨ Requisitos Cumplidos

- [x] **Grid Layout Anidado de 2 Niveles:**
  - **Nivel 1 (Principal):** Estructura general de 3 columnas principales en pantallas grandes.
  - **Nivel 2 (Interno):** Sub-grids independientes dentro de cada `<section>` con celdas de $1 \times 1$, celdas ocupando una fila completa (`grid-column: 1 / -1`), y celdas span multidireccionales (`span 2` y `span 3`).
- [x] **Diseño Responsive (< 700px / > 700px):**
  - Pantallas $> 700\text{px}$: Disposición de 3 columnas horizontales principales.
  - Pantallas $\le 700\text{px}$: Las 3 secciones pasan a apilarse verticalmente (1 columna).
- [x] **Variables CSS en Fichero Independiente:**
  - Archivo `variables.css` exportado e importado al inicio de `styles.css` con `@import`.
- [x] **Sintaxis CSS Anidado (Native Nesting):**
  - Uso de selecciones anidadas nativas (`& > section`, `&:hover`, etc.) sin necesidad de preprocesadores como SASS.
- [x] **Modo Claro y Oscuro Automático:**
  - Integración de `@media (prefers-color-scheme: dark)` utilizando tokens CSS centralizados en `variables.css`.
- [x] **Animaciones y Transiciones Sutiles:**
  - Efecto *elevation* y suavizado en el `:hover` de cada celda.
  - Escalado suave en las imágenes al pasar el cursor (`transform: scale(...)`).
  - Animación de entrada `@keyframes` en el hero principal.
  - Adaptación para accesibilidad mediante `@media (prefers-reduced-motion: reduce)`.
- [x] **Tipografía y Aspecto Visual Cuidado:**
  - Integración de fuentes tipográficas desde Google Fonts (*Fraunces* para titulares display y *Inter* para cuerpo de texto).

---

## 🛠️ Tecnologías Utilizadas

* **HTML5:** Estructura semántica (`<main>`, `<section>`, `<article>`, `<figure>`, `<figcaption>`).
* **CSS3:**
  * Grid Layout (Nivel 1 y Nivel 2).
  * Custom Properties / Variables CSS.
  * Media Queries.
  * CSS Native Nesting.
  * Transiciones y Keyframe Animations.
* **Google Fonts:** Fraunces & Inter.

---

## 📂 Estructura del Archivo

```text
├── index.html        # Estructura principal HTML5
├── styles.css        # Estilos principales y reglas del layout Bento
├── variables.css     # Tokens de diseño, tipografía y paleta claro/oscuro
└── README.md         # Documentación del proyecto
```

---

## ⚙️ Instrucciones de Instalación y Uso

1. Clonar este repositorio:
   ```bash
   git clone https://github.com/tu-usuario/bento-grid-cafe.git
   ```
2. Navegar a la carpeta del proyecto:
   ```bash
   cd bento-grid-cafe
   ```
3. Abrir el archivo `index.html` en el navegador de tu preferencia o desplegar mediante **Live Server** en Visual Studio Code.

---

## 🎨 Demostración del Sistema de Colores (Modo Claro vs. Oscuro)

El esquema de color detecta la preferencia del sistema operativo mediante `color-scheme: light dark`:

* **Modo Claro:** Fondos en tonos cálidos (*beige* / pergamino), texto en tono café oscuro y acentos caramelo/cereza.
* **Modo Oscuro:** Fondos en tonos espresso profundo, texto claro de alta legibilidad y sombras atenuadas.