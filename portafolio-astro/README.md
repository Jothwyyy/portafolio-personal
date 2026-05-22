# Portafolio Astro

Esta es la version actual de mi portafolio personal, construida con Astro y basada visualmente en la plantilla `Twenty` de HTML5 UP.

## Objetivo

En este sitio presento mi perfil profesional con foco en desarrollo backend, las tecnologias que uso, proyectos destacados y una pagina de contacto.

## Secciones actuales

- `/`: landing principal con `Banner`, perfil, tecnologias, habilidades, proyectos y CTA
- `/contact`: formulario visual de contacto

## Stack

- Astro 6
- CSS global + estilos inline en componentes `.astro`
- Font Awesome cargado desde `assets/`
- scripts heredados de la plantilla original: jQuery, Scrolly, Scrollex, Dropotron y utilidades responsivas

## Requisitos

- Node.js `>=22.12.0`
- npm

## Comandos

```bash
npm install
npm run dev
```

Comandos disponibles:

- `npm run dev`: servidor local en modo desarrollo
- `npm run build`: genera la salida estatica en `dist/`
- `npm run preview`: previsualiza el build generado
- `npm run astro -- --help`: ayuda de la CLI de Astro

## Estructura relevante

```text
portafolio-astro/
├── public/
│   ├── assets/             # js y recursos estaticos servidos tal cual
│   └── images/             # imagenes del sitio
├── assets/
│   └── css/                # Font Awesome y recursos bundleados
├── src/
│   ├── components/
│   ├── layouts/
│   ├── pages/
│   └── styles/
├── package.json
└── astro.config.mjs
```

## Arquitectura rapida

- `src/pages/index.astro` compone la home usando `BaseLayout`, `Banner`, `MainContent` y `CTA`.
- `src/components/MainContent.astro` conecta las secciones principales de la home.
- `src/layouts/BaseLayout.astro` centraliza `Navbar`, `Footer`, `global.css` y todos los scripts globales.
- Los IDs de scroll del navbar viven dentro de los componentes de seccion, por ejemplo `#proyectos`, `#tecnologias` y `#sobre-mi`.

## Relacion con las otras carpetas del repo

- `../docs/` guarda una version estatica anterior de mi portafolio, ya personalizada.
- `../vendor/twenty/` guarda la plantilla original de HTML5 UP en la que me base.
- Aqui concentro la version mantenible y activa del proyecto.

## Convenciones de estilos y assets

- No todo lo que esta en `/assets` viene del mismo lugar.
- `assets/` contiene recursos fuente bundleados por Astro.
- `public/assets/` contiene archivos estaticos accesibles directamente por URL, por ejemplo `/assets/js/main.js`.
- Los estilos estan repartidos entre `src/styles/global.css` y bloques `<style>` dentro de varios componentes. Antes de mover o borrar estilos, revisa ambas capas.

## Verificacion

La comprobacion real del proyecto es:

```bash
npm run build
```

Actualmente no hay scripts propios de lint, tests o typecheck separados.

## Referencias

- Version estatica previa: `../docs/`
- Plantilla original: `../vendor/twenty/`
- Auditoria tecnica de la plantilla base: `../auditoria_plantilla_twenty.md`
