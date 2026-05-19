# Auditoría técnica de plantilla HTML5 UP: Twenty

## 1. Datos generales

| Elemento | Descripción |
|---|---|
| Plantilla auditada | Twenty by HTML5 UP |
| Fuente | html5up.net |
| Tipo de proyecto | Sitio web estático multipágina |
| Licencia declarada | Creative Commons Attribution 3.0 Unported |
| Archivo revisado | `html5up-twenty.zip` |
| Total de elementos encontrados | 63 archivos y carpetas |
| Páginas HTML principales | 5 archivos HTML |
| Enfoque de la auditoría | Identificación de tecnologías, estructura, dependencias, funcionamiento general y observaciones técnicas |

## 2. Objetivo de la auditoría

El objetivo de esta auditoría es revisar la plantilla **Twenty** de HTML5 UP para identificar las tecnologías utilizadas, su estructura de archivos, sus componentes principales, dependencias, funcionamiento general y posibles puntos de mejora antes de usarla como base para un proyecto web.

## 3. Resumen tecnico

La plantilla **Twenty** es un sitio web estático responsivo desarrollado principalmente con **HTML5**, **CSS3**, **JavaScript**, **jQuery** y **Sass**. Está pensada para funcionar sin backend y puede publicarse en servicios de hosting estático como GitHub Pages, Netlify, Vercel o cualquier servidor web tradicional.

La plantilla incluye varias páginas prediseñadas, un sistema de navegación con submenús, diseño adaptable a dispositivos móviles, integración con Font Awesome para iconos y estilos compilados desde Sass. También incluye una página de contacto visual, aunque el formulario no tiene funcionalidad real de envío porque no cuenta con backend ni atributo `action`.

Durante la revisión se detectó una referencia a un archivo JavaScript llamado `jquery.scrollgress.min.js` en varias páginas HTML, pero dicho archivo no está incluido dentro del paquete revisado. Esto puede provocar errores 404 en consola cuando esas páginas se carguen en el navegador.

## 4. Tecnologías utilizadas

| Tecnología | Uso dentro de la plantilla |
|---|---|
| HTML5 | Estructura principal de las páginas, uso de etiquetas semánticas como `header`, `nav`, `section`, `article` y `footer`. |
| CSS3 | Estilos visuales, diseño responsivo, animaciones, transiciones y adaptación a diferentes tamaños de pantalla. |
| JavaScript | Comportamiento interactivo de la plantilla, menú móvil, animaciones de carga, desplazamiento suave y efectos de navegación. |
| jQuery | Librería base utilizada por los scripts interactivos de la plantilla. |
| Sass / SCSS | Preprocesador CSS utilizado para organizar mejor los estilos fuente antes de compilarlos a CSS. |
| Font Awesome | Librería de iconos usada mediante archivos CSS y fuentes locales. |
| Google Fonts | Fuente externa `Lato`, importada desde CSS. |
| Responsive Tools / Breakpoints | Utilidades para manejar puntos de quiebre responsivos. |
| Scrolly / Scrollex | Plugins para desplazamiento suave y efectos basados en scroll. |
| Dropotron | Plugin usado para crear menús desplegables. |

## 5. Estructura general de archivos

```text
html5up-twenty/
├── index.html
├── left-sidebar.html
├── right-sidebar.html
├── no-sidebar.html
├── contact.html
├── README.txt
├── LICENSE.txt
├── images/
│   ├── banner.jpg
│   ├── pic01.jpg
│   ├── pic02.jpg
│   ├── pic03.jpg
│   └── pic04.jpg
└── assets/
    ├── css/
    │   ├── main.css
    │   ├── noscript.css
    │   ├── fontawesome-all.min.css
    │   └── images/
    ├── js/
    │   ├── jquery.min.js
    │   ├── jquery.dropotron.min.js
    │   ├── jquery.scrolly.min.js
    │   ├── jquery.scrollex.min.js
    │   ├── browser.min.js
    │   ├── breakpoints.min.js
    │   ├── util.js
    │   └── main.js
    ├── sass/
    │   ├── main.scss
    │   ├── noscript.scss
    │   └── libs/
    └── webfonts/
```

## 6. Páginas incluidas

| Archivo | Función |
|---|---|
| `index.html` | Página principal de la plantilla. Incluye banner, secciones informativas, tarjetas y llamadas a la acción. |
| `left-sidebar.html` | Página de contenido con barra lateral izquierda. |
| `right-sidebar.html` | Página de contenido con barra lateral derecha. |
| `no-sidebar.html` | Página de contenido sin barra lateral. |
| `contact.html` | Página de contacto con formulario visual. |

## 7. Análisis del HTML

La plantilla utiliza una estructura HTML5 correcta y semántica. Se identifican etiquetas como:

- `header`
- `nav`
- `section`
- `article`
- `footer`
- `form`

La página principal `index.html` incluye una navegación superior, un banner principal, contenido organizado en secciones y un pie de página. También se usa la etiqueta `noscript` para cargar una hoja de estilos alternativa cuando JavaScript está deshabilitado.

### Observaciones sobre HTML

| Aspecto | Evaluación |
|---|---|
| Uso de HTML5 | Correcto |
| Estructura semántica | Correcta |
| Navegación | Funcional y organizada |
| Separación de contenido y estilos | Correcta |
| Formulario de contacto | Visual, pero sin funcionalidad real de envío |
| Accesibilidad básica | Aceptable, aunque puede mejorarse |

## 8. Análisis del CSS y Sass

La plantilla utiliza un archivo principal `assets/css/main.css`, generado a partir de archivos Sass ubicados en `assets/sass/`.

Los estilos incluyen:

- Reset CSS.
- Diseño responsivo.
- Sistema de columnas.
- Estilos para botones, formularios, tablas e imágenes.
- Animaciones y transiciones.
- Estilos específicos para navegación móvil.
- Importación de Font Awesome.
- Importación de Google Fonts.

### Archivos relevantes

| Archivo | Descripción |
|---|---|
| `assets/css/main.css` | Hoja de estilos principal compilada. |
| `assets/css/noscript.css` | Estilos alternativos cuando JavaScript está deshabilitado. |
| `assets/css/fontawesome-all.min.css` | Estilos de Font Awesome. |
| `assets/sass/main.scss` | Archivo Sass principal. |
| `assets/sass/libs/_vars.scss` | Variables de diseño, colores y medidas. |
| `assets/sass/libs/_mixins.scss` | Mixins reutilizables. |
| `assets/sass/libs/_breakpoints.scss` | Configuración de puntos de quiebre. |

### Observaciones sobre CSS/Sass

La existencia de archivos Sass es positiva porque permite modificar la plantilla de forma más ordenada. Sin embargo, para proyectos sencillos puede bastar con editar directamente `main.css`, siempre que se tenga cuidado de no perder organización.

## 9. Análisis del JavaScript

La plantilla utiliza JavaScript principalmente para mejorar la experiencia visual e interactiva. El archivo más importante es `assets/js/main.js`, que inicializa los comportamientos principales.

### Scripts incluidos

| Archivo | Función |
|---|---|
| `jquery.min.js` | Librería jQuery base. |
| `jquery.dropotron.min.js` | Menús desplegables. |
| `jquery.scrolly.min.js` | Desplazamiento suave al navegar por anclas. |
| `jquery.scrollex.min.js` | Efectos relacionados con el scroll. |
| `browser.min.js` | Detección de navegador y sistema. |
| `breakpoints.min.js` | Manejo de puntos de quiebre responsivos. |
| `util.js` | Funciones auxiliares, como panel móvil y navegación. |
| `main.js` | Inicialización general de la plantilla. |

### Funcionalidades detectadas

- Animaciones iniciales al cargar la página.
- Remoción de la clase `is-preload` después de cargar.
- Menú desplegable en escritorio.
- Panel de navegación lateral en dispositivos móviles.
- Scroll suave en enlaces con clase `scrolly`.
- Cambio visual del encabezado al hacer scroll.

## 10. Dependencias externas e internas

| Dependencia | Tipo | Estado |
|---|---|---|
| jQuery | Interna/local | Incluida |
| Dropotron | Interna/local | Incluida |
| Scrolly | Interna/local | Incluida |
| Scrollex | Interna/local | Incluida |
| Browser.js | Interna/local | Incluida |
| Breakpoints.js | Interna/local | Incluida |
| Font Awesome | Interna/local | Incluida |
| Google Fonts Lato | Externa | Se carga desde internet |
| Formspree | Sugerida en README | No implementada |

## 11. Hallazgos técnicos

### Hallazgo 1: Archivo JavaScript referenciado pero no incluido

En las páginas `left-sidebar.html`, `right-sidebar.html`, `no-sidebar.html` y `contact.html` se referencia el archivo:

```html
<script src="assets/js/jquery.scrollgress.min.js"></script>
```

Sin embargo, este archivo no está presente dentro de la carpeta `assets/js/`.

#### Impacto

Esto puede generar un error 404 en la consola del navegador. Aunque la página puede seguir funcionando, es una mala práctica dejar referencias a archivos inexistentes.

#### Recomendación

Eliminar esa línea de las páginas afectadas o agregar el archivo correspondiente si realmente se necesita.

---

### Hallazgo 2: Formulario de contacto sin configuración de envío

El archivo `contact.html` incluye un formulario, pero este no tiene atributos como `action` o `method`.

Ejemplo del formulario detectado:

```html
<form>
```

#### Impacto

El formulario no enviará la información a ningún servidor o servicio externo. Solo funciona visualmente.

#### Recomendación

Agregar un servicio como Formspree, un backend propio o una función serverless para procesar los mensajes.

Ejemplo:

```html
<form action="https://formspree.io/f/tu-id" method="POST">
```

---

### Hallazgo 3: Uso de una fuente externa

La plantilla importa la fuente `Lato` desde Google Fonts:

```css
@import url("https://fonts.googleapis.com/css?family=Lato:300,400,900");
```

#### Impacto

El sitio depende de conexión a internet para cargar la fuente. También puede afectar ligeramente el rendimiento o la privacidad.

#### Recomendación

Para mayor control, se puede alojar la fuente localmente o usar una fuente del sistema.

---

### Hallazgo 4: Plantilla sin backend

La plantilla es completamente estática. Esto es positivo para rendimiento y facilidad de publicación, pero limita funciones como autenticación, formularios reales, bases de datos o paneles administrativos.

#### Recomendación

Si el proyecto necesita funciones dinámicas, se debe integrar con tecnologías adicionales como Node.js, PHP, Firebase, Supabase, Formspree o servicios serverless.

## 12. Evaluación de responsividad

La plantilla está diseñada para ser responsiva. Utiliza breakpoints definidos tanto en JavaScript como en Sass/CSS.

### Breakpoints detectados

| Nombre | Rango aproximado |
|---|---|
| wide | 1281px a 1680px |
| normal | 981px a 1280px |
| narrow | 841px a 980px |
| narrower | 737px a 840px |
| mobile | hasta 736px |

### Evaluación

La responsividad es uno de los puntos fuertes de la plantilla. El menú se adapta a pantallas pequeñas mediante un panel lateral generado con JavaScript.

## 13. Evaluación de accesibilidad

La plantilla tiene una base aceptable, pero puede mejorar en accesibilidad.

### Aspectos positivos

- Uso de estructura semántica.
- Navegación clara.
- Botones y enlaces visibles.
- Diseño adaptable a diferentes dispositivos.

### Aspectos por mejorar

| Área | Recomendación |
|---|---|
| Imágenes | Revisar y mejorar textos `alt` cuando se personalice la plantilla. |
| Formularios | Agregar etiquetas `label` asociadas a cada campo. |
| Contraste | Verificar contraste de colores según WCAG. |
| Navegación por teclado | Probar menú y submenús sin mouse. |
| Idioma | Cambiar `<html>` a `<html lang="es">` si el sitio estará en español. |

## 14. Evaluación de rendimiento

La plantilla es relativamente ligera y adecuada para sitios estáticos. Sin embargo, carga varios archivos JavaScript y una fuente externa.

### Puntos positivos

- Sitio estático.
- Imágenes locales.
- Librerías minificadas.
- CSS centralizado.
- No requiere base de datos.

### Posibles mejoras

- Comprimir imágenes antes de publicar.
- Eliminar scripts que no se usen.
- Corregir referencias inexistentes.
- Evitar dependencias externas si se busca carga completamente local.
- Minificar archivos modificados después de personalizar la plantilla.

## 15. Evaluación de seguridad

Al ser una plantilla estática, la superficie de ataque es baja. No hay autenticación, conexión a base de datos ni procesamiento del lado del servidor.

### Riesgos mínimos identificados

| Riesgo | Nivel | Comentario |
|---|---|---|
| Formulario sin validación real | Bajo | Actualmente no envía datos. Si se conecta a un backend, se debe validar. |
| Dependencia externa de Google Fonts | Bajo | Puede evitarse alojando fuentes localmente. |
| Librerías antiguas | Medio | Conviene verificar versiones si el proyecto será público o de producción. |
| Enlaces con `#` | Bajo | Deben reemplazarse por rutas reales al personalizar. |

## 16. Licencia

La plantilla declara estar bajo la licencia **Creative Commons Attribution 3.0 Unported**. Esto significa que puede usarse de forma personal o comercial, siempre que se mantenga la atribución correspondiente al autor original.

### Recomendación

Mantener un crédito visible o documentado hacia HTML5 UP, por ejemplo en el footer, README o documentación del proyecto.

## 17. Recomendaciones generales

1. Corregir o eliminar la referencia faltante a `jquery.scrollgress.min.js`.
2. Personalizar los textos de ejemplo.
3. Cambiar el idioma del documento a español si el sitio será usado en español.
4. Optimizar las imágenes antes de publicar.
5. Configurar correctamente el formulario de contacto.
6. Revisar accesibilidad básica con herramientas como Lighthouse.
7. Mantener la atribución de HTML5 UP por la licencia.
8. Usar Sass si se planean cambios grandes de diseño.
9. Eliminar páginas que no se vayan a usar.
10. Probar el sitio en móvil, tablet y escritorio.

## 18. Conclusión

La plantilla **Twenty** de HTML5 UP es una base sólida para crear un sitio web estático, responsivo y visualmente atractivo. Utiliza tecnologías ampliamente conocidas como HTML5, CSS3, JavaScript, jQuery y Sass. Su estructura está bien organizada y permite una personalización relativamente sencilla.

Como puntos a corregir, se recomienda atender la referencia faltante al archivo `jquery.scrollgress.min.js`, configurar el formulario de contacto si se necesita funcionalidad real y revisar aspectos de accesibilidad antes de publicar el sitio. En general, la plantilla es adecuada para portafolios, sitios informativos, páginas institucionales pequeñas o proyectos académicos.
