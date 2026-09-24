---
doc_id: css-flexbox-y-grid
institucion: Instituto Politécnico Formosa
carrera: Tecnicatura en Desarrollo de Software Multiplataforma
materia: Taller de Lenguaje de Programación I
unidad: "Unidad 2 — Diseño de Aplicaciones Web"
tema: "Diseño Web Moderno: Flexbox y Grid"
fuentes_origen:
  - "Material de Lectura CSS-GRID-FLEX.pdf (parte 2: Diseño Web Moderno, Flexbox y Grid)"
relacion_con_otros_docs: >
  Continúa docs-ia/css/01-css-selectores-y-propiedades.md. Es el fundamento CSS nativo equivalente
  al sistema de cuadrícula (grid de 12 columnas) que implementa
  docs-ia/bootstrap/01-bootstrap-diseno-responsive.md, sección 3 (Bootstrap resuelve con clases
  predefinidas lo que aquí se resuelve escribiendo CSS directamente).
nivel: introductorio-intermedio
---

# CSS — Diseño Web Moderno: Flexbox y Grid

## Índice
1. [Introducción a Flexbox y Grid](#1-introducción-a-flexbox-y-grid)
2. [Propiedades de Flexbox](#2-propiedades-de-flexbox)
3. [Propiedades de Grid](#3-propiedades-de-grid)
4. [Combinación de Flexbox y Grid](#4-combinación-de-flexbox-y-grid)

---

## 1. Introducción a Flexbox y Grid

### 1.1 ¿Qué es Flexbox?

**Flexbox** es una herramienta de diseño en CSS que permite maquetar elementos de manera flexible en **una sola dimensión**, ya sea en una fila o en una columna. Facilita el centrado, el posicionamiento y la distribución de elementos en una línea, y es ideal para maquetar elementos en sitios web responsive.

### 1.2 ¿Qué es Grid?

**Grid** es otra herramienta de diseño en CSS que permite maquetar elementos en una cuadrícula de **dos dimensiones**, tanto en filas como en columnas. Es ideal para maquetar diseños complejos y adaptativos.

### 1.3 Función de Flexbox y Grid en la maquetación moderna

Ambas herramientas permiten crear diseños adaptables y flexibles para sitios web. Utilizadas en conjunto, los diseñadores pueden crear diseños complejos y adaptativos con mayor facilidad.

## 2. Propiedades de Flexbox

Se activa declarando `display: flex;` en el contenedor.

### 2.1 Propiedades para maquetar elementos en línea (fila)

```css
{
  display: flex;               /* establece el contenedor como flexible */
  justify-content: "valor";    /* alinea elementos horizontalmente */
  align-items: "valor";        /* alinea elementos verticalmente */
  flex-direction: "valor";     /* establece la dirección de los elementos */
  flex-wrap: "valor";          /* establece si los elementos se envuelven en una nueva línea */
}
```

### 2.2 Propiedades para maquetar elementos en columnas

```css
{
  flex-direction: column;      /* establece la dirección de los elementos en una columna */
  align-items: "valor";        /* alinea elementos horizontalmente */
  justify-content: "valor";    /* alinea elementos verticalmente */
  flex-wrap: "valor";          /* establece si los elementos se envuelven en una nueva línea */
}
```

### 2.3 Resumen de propiedades Flexbox

| Propiedad | Función |
|---|---|
| `display: flex` | Convierte al elemento en un contenedor flexible. |
| `flex-direction` | Define el eje principal: `row` (fila, por defecto) o `column` (columna). |
| `justify-content` | Alinea los elementos a lo largo del eje principal. |
| `align-items` | Alinea los elementos a lo largo del eje transversal (cruzado). |
| `flex-wrap` | Define si los elementos se envuelven en una nueva línea cuando no entran en una sola. |

> **Nota:** el significado de `justify-content` y `align-items` se invierte según el valor de `flex-direction` (en `row`, `justify-content` alinea horizontalmente; en `column`, alinea verticalmente).

## 3. Propiedades de Grid

Se activa declarando `display: grid;` en el contenedor.

### 3.1 Propiedades para maquetar elementos en filas

```css
{
  display: grid;                  /* establece el contenedor como cuadrícula */
  grid-template-rows: "valor";    /* establece el tamaño de las filas */
  grid-gap: "valor";              /* establece el espacio entre las filas */
  grid-row: "valor";              /* coloca elementos en una fila específica */
}
```

### 3.2 Propiedades para maquetar elementos en columnas

```css
{
  grid-template-columns: "valor"; /* establece el tamaño de las columnas */
  grid-gap: "valor";              /* establece el espacio entre las columnas */
  grid-column: "valor";           /* coloca elementos en una columna específica */
  grid-auto-flow: "valor";        /* establece la dirección de las columnas */
}
```

### 3.3 Resumen de propiedades Grid

| Propiedad | Función |
|---|---|
| `display: grid` | Convierte al elemento en un contenedor de cuadrícula. |
| `grid-template-rows` | Define el tamaño de cada fila de la cuadrícula. |
| `grid-template-columns` | Define el tamaño de cada columna de la cuadrícula. |
| `grid-gap` | Espacio entre filas y/o columnas. |
| `grid-row` / `grid-column` | Ubica un elemento en una fila/columna específica de la cuadrícula. |
| `grid-auto-flow` | Controla la dirección en la que se acomodan automáticamente los elementos. |

## 4. Combinación de Flexbox y Grid

### 4.1 ¿Cómo combinarlos para diseños complejos?

Se puede usar **Flexbox** para maquetar elementos en una fila (o columna) y **Grid** para maquetar en columnas (o filas), o viceversa. También es posible usar Flexbox **dentro** de un elemento de Grid, combinando ambas herramientas para lograr mayor flexibilidad en la distribución y alineación de los elementos.

### 4.2 Ventajas de usarlos en conjunto

- Mayor **flexibilidad y adaptabilidad** en el diseño.
- Facilita la maquetación de **diseños complejos**.
- Permite mayor **control** en la distribución y alineación de los elementos.

---

**Relación con otros documentos:** este documento es el equivalente en CSS nativo del sistema de grid de 12 columnas que Bootstrap resuelve mediante clases predefinidas (`col-*`, `d-flex`, etc.) — ver `docs-ia/bootstrap/01-bootstrap-diseno-responsive.md`, sección 3. Se apoya en los selectores y propiedades básicas de `docs-ia/css/01-css-selectores-y-propiedades.md`.
