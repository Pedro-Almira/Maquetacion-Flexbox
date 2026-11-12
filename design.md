# Design Specification — Mi página web

## 1. Identidad visual

El proyecto utiliza una estética minimalista y moderna, inspirada en el diseño visual de Apple.com.

Principios visuales:
- Simplicidad y claridad.
- Distribución ordenada del contenido.
- Espacios equilibrados entre elementos.
- Jerarquía visual fácil de identificar.
- Interfaz limpia y funcional.

## 2. Paleta de colores

La interfaz utiliza una paleta neutra con un color de acento azul.

| Variable CSS | Valor | Aplicación |
|---|---|---|
| `--color-primary` | `#111111` | Elementos principales y navegación |
| `--color-secondary` | `#f5f5f7` | Fondos secundarios |
| `--color-accent` | `#0071e3` | Enlaces y elementos destacados |
| `--color-background` | `#e0e3e3` | Fondo general |
| `--color-text` | `#1d1d1f` | Texto principal |
| `--color-text-secondary` | `#6e6e73` | Texto secundario |
| `--color-border` | `#d2d2d7` | Bordes y separadores |

## 3. Tipografía

- Fuente principal: Roboto.
- Fuentes alternativas: Arial, Helvetica, sans-serif.
- Los encabezados destacan mediante tamaño y peso.
- Los párrafos mantienen una lectura cómoda.
- La jerarquía tipográfica debe ser coherente.

Roboto se carga mediante Google Fonts CDN.

## 4. Estructura y distribución

La página utiliza HTML semántico y Flexbox como sistema principal de distribución.

Estructura:
- Header: cabecera de la página.
- Nav: navegación principal.
- Main: contenido central.
- Aside: barra lateral.
- Section: área de contenido y tarjetas.
- Footer: pie de página.
- Bottom bar: barra fija inferior.

### Distribución vertical

El contenedor principal tiene una altura de `120vh`.

Sus cuatro secciones utilizan las siguientes dimensiones:

| Sección | Regla CSS | Dimensión |
|---|---|---|
| Header | `flex: 0 0 12vh` | 12vh |
| Nav | `flex: 0 0 8vh` | 8vh |
| Main | `flex: 0 0 73vh` | 73vh |
| Footer | `flex: 0 0 21%` | 21% del contenedor |

El porcentaje del footer es intencional y debe mantenerse. Permite que su dimensión dependa del contenedor principal.

No sustituir esta regla por una altura fija en `vh`.

## 5. Distribución horizontal

El área principal utiliza un diseño Flexbox en fila.

- Sidebar: ocupa el 25% del espacio disponible.
- Content: ocupa el espacio restante.
- La separación entre ambos utiliza la variable `--spacing-medium`.
- Los elementos mantienen sus dimensiones mediante las propiedades flex correspondientes.

## 6. Componentes visuales

### Navegación
- Fondo oscuro.
- Texto claro.
- Elementos alineados mediante Flexbox.
- Separación uniforme entre enlaces.
- Transiciones visuales al pasar el cursor.

### Barra lateral
- Separada del contenido principal.
- Distribución mediante Flexbox.
- Anchura proporcional al espacio disponible.

### Tarjetas de contenido
- Distribución flexible mediante Flexbox.
- Imágenes con `object-fit: cover`.
- Bordes redondeados.
- Texto limitado para mantener uniformidad visual.
- Separación constante entre tarjetas.

### Footer
- Fondo coherente con la identidad visual.
- Contenido organizado en grupos.
- Enlaces e iconos sociales.

### Bottom bar
- Posición fija en la parte inferior de la ventana.
- Acceso directo para volver al inicio.
- Fondo y contraste coherentes con el resto de la interfaz.

## 7. Bordes y espaciado

Los componentes comparten un sistema de bordes redondeados definido mediante variables CSS:

- `--border-small`: 8px.
- `--border-medium`: 16px.
- `--border-large`: 24px.

Sistema de espaciado:
- `--spacing-small`: 10px.
- `--spacing-medium`: 20px.
- `--spacing-large`: 40px.

## 8. Imágenes e iconografía

- Todas las imágenes deben incluir atributos `alt` descriptivos.
- Las imágenes de las tarjetas deben conservar proporciones uniformes.
- Los iconos se implementan mediante Material Symbols.
- La iconografía debe mantener coherencia visual.

## 9. Diseño adaptable

El contenedor principal utiliza:
- Ancho: `100%`.
- Ancho mínimo: `1000px`.
- Ancho máximo: `2000px`.
- Centrado horizontal mediante `margin: 0 auto`.

La distribución se realiza principalmente mediante Flexbox.

Existe una adaptación mediante media query para pantallas de hasta 768px, que modifica los tamaños de los encabezados y la separación del contenido.

## 10. Criterios de implementación

- Mantener HTML semántico.
- Utilizar Flexbox como sistema principal de distribución.
- Centralizar colores, tipografías y medidas reutilizables en `:root`.
- Separar estructura HTML y presentación CSS.
- Mantener los estilos organizados en archivos independientes.
- Evitar duplicación de reglas CSS.
- Priorizar legibilidad, consistencia y sencillez.
- No alterar las proporciones verticales establecidas sin autorización.

## 11. Objetivo final

Conseguir una página web minimalista, ordenada y visualmente coherente, con una estructura clara, navegación sencilla y distribución flexible del contenido.