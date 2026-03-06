# Landing Page — Curso de Cursor · Trinchera WP

Landing page de venta para el curso de Cursor AI, desarrollada con HTML semántico y Tailwind CSS v4.

## Stack tecnológico

- **HTML5** — estructura semántica
- **Tailwind CSS v4** — estilos mediante clases de utilidad
- **Google Fonts** — tipografía Inter
- **Node.js + npm** — compilación del CSS

## Estructura del proyecto

```
Proy LandingPage/
├── index.html          # Página principal
├── src/
│   └── input.css       # CSS fuente (Tailwind + estilos propios)
├── dist/
│   └── output.css      # CSS compilado y minificado (generado automáticamente)
├── package.json        # Dependencias y scripts
└── node_modules/       # Dependencias instaladas
```

## Instalación

Requiere [Node.js](https://nodejs.org/) v18 o superior.

```bash
npm install
```

## Comandos disponibles

| Comando | Descripción |
|---|---|
| `npm run dev` | Modo desarrollo: vigila cambios y regenera el CSS automáticamente |
| `npm run build` | Genera el CSS final minificado para producción |

## Flujo de trabajo

### Durante el desarrollo

```bash
npm run dev
```

Deja este proceso corriendo en la terminal. Cada vez que guardes cambios en `index.html` o `src/input.css`, el CSS se regenera automáticamente en `dist/output.css`.

### Para producción

```bash
npm run build
```

Genera `dist/output.css` minificado con solo las clases de Tailwind que se usan en el proyecto.

## Personalización de estilos

Todos los estilos se gestionan desde `src/input.css`:

```css
@import "tailwindcss";

/* Tema: personalización de variables de Tailwind */
@theme {
    --font-sans: 'Inter', sans-serif;
}

/* Estilos base: elementos HTML globales */
@layer base {
    /* FAQ accordion (details/summary) */
}

/* Componentes: clases reutilizables propias */
@layer components {
    /* Syntax highlighting del bloque de código */
    .code-comment { ... }
    .code-keyword  { ... }
}
```

> **Importante:** `index.html` carga `./dist/output.css`, nunca `src/input.css` directamente. Siempre ejecuta `npm run build` o `npm run dev` después de modificar `src/input.css`.

## Secciones de la landing page

1. **Navbar** — navegación sticky con enlace de compra
2. **Hero** — titular principal y llamada a la acción
3. **El Problema** — puntos de dolor del desarrollador
4. **La Solución** — propuesta de valor de Cursor
5. **Para quién es** — perfiles de WordPress, Laravel y Frontend
6. **Temario** — módulos del curso
7. **Meta-gancho** — esta página fue creada con Cursor
8. **Precio** — tarjeta de compra con garantía
9. **FAQ** — preguntas frecuentes con accordion

## Proyecto

Forma parte de [Trinchera WP](https://trincherawp.com), plataforma de cursos de desarrollo web para WordPress, Laravel y desarrollo frontend.
