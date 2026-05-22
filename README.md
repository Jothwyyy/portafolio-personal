# Portafolio Personal

En este repositorio guardo la evolucion de mi portafolio personal desde una base HTML estatica hasta la version actual en Astro.

Aqui conviven tres estados utiles del proyecto:

- `portafolio-astro/`: mi version actual y activa del portafolio, montada con Astro.
- `docs/`: una version estatica ya adaptada con mi contenido, anterior a la migracion a Astro.
- `vendor/twenty/`: la plantilla original `Twenty` de HTML5 UP en la que me base.

## Versiones del proyecto

### 1. Version actual: Astro

La aplicacion que ejecuto y edito hoy vive en `portafolio-astro/`.

Incluye:

- pagina principal con secciones de perfil, tecnologias, habilidades y proyectos
- pagina de contacto en `/contact`
- estilos globales y estilos inline dentro de componentes `.astro`
- scripts heredados de la plantilla original para scroll, menu y efectos visuales

### 2. Version estatica previa

La carpeta `docs/` conserva una version HTML/CSS/JS de mi portafolio ya personalizada con mi informacion.

Me sirve para:

- revisar una etapa anterior del sitio antes de migrarlo a Astro
- comparar contenido, estilos y assets ya adaptados
- conservar una salida estatica facil de publicar o consultar

### 3. Plantilla base original

La carpeta `vendor/twenty/` conserva la plantilla `Twenty` original de HTML5 UP.

La uso como referencia para:

- comparar la estructura y los estilos base del autor original
- revisar los assets originales de HTML5 UP
- entender que partes adapte primero en `docs/` y despues en `portafolio-astro/`

No la considero una version mia del proyecto, sino la base externa desde la que parti.

La auditoria tecnica de esa plantilla esta en `auditoria_plantilla_twenty.md`.

## Estructura del repositorio

```text
.
├── portafolio-astro/        # app real en Astro
├── docs/                    # version estatica personalizada
├── vendor/twenty/           # plantilla HTML5 UP original
├── auditoria_plantilla_twenty.md
```

## Como ejecutar la version actual

Todos los comandos de Node se ejecutan dentro de `portafolio-astro/`:

```bash
cd portafolio-astro
npm install
npm run dev
```

Comandos disponibles:

- `npm run dev`: inicia el servidor local
- `npm run build`: genera la version estatica en `dist/`
- `npm run preview`: sirve el build generado localmente

## Requisitos

- Node.js `>=22.12.0`
- npm

## Notas utiles

- El `README.md` dentro de `portafolio-astro/` documenta la app real.
- `docs/` y `vendor/twenty/` son sitios estaticos; no dependen de npm para abrirse o inspeccionarse.
- La raiz del repo no es un proyecto Node ejecutable por si sola.

## Creditos

La base visual original proviene de la plantilla `Twenty` de [HTML5 UP](https://html5up.net/), creada por AJ (`@ajlkn`) y distribuida bajo la licencia indicada en `docs/README.txt` y `vendor/twenty/README.txt`.

## Verificacion

La verificacion disponible hoy es:

```bash
cd portafolio-astro
npm run build
```

No hay scripts propios de lint, test o typecheck separados en este repositorio.
