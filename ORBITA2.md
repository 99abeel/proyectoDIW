# Órbita 2: sistema visual de D&D Solo Adventure Platform

## Enlaces

| Qué | Enlace |
|---|---|
| Archivo de Figma (versión "Entrega Órbita 2") | [enlace](https://www.figma.com/design/rXQT0CUpgMyoFADKGzxZMx/wireframe-proyecto-DIW?node-id=166-1870&p=f&t=57LW0gQuaxyepGFA-0) |
| Prototipo (enlace que empieza por `figma.com/proto/`) |  |
| Proyecto de Google Stitch (solo si lo has usado) | [enlace](https://stitch.withgoogle.com/projects/3555903911542581377?pli=1) |

## Dónde está cada cosa en Figma

| Entregable | Página y sección del archivo |
|---|---|
| Inventario de decisiones | Página `Guía de estilo`, marco superior |
| Wireframes rediseñados con sus notas | Página `Wireframes`, sección derecha `Wireframes rediseñados` |
| Componentes | Página `Componentes`, secciones `Átomos` y `Organismos` |
| Mockups del happy path | Página `Mockups` (en proceso) |
| Pantalla principal en el segundo ancho | Página `Mockups` (pendiente) |
| Pantallas en modo oscuro | Página `Componentes` (verificado en componentes maestros con selector de modo) |
| Guía de estilo | Página `Guía de estilo`, lienzo central |

## Lista de comprobación de Figma

- [x] Variables en dos colecciones (primitivos y semánticos), con alias, modos claro y oscuro, ámbito, descripción y sintaxis de código.
- [x] Estilos de texto, efecto y retícula vinculados a las variables.
- [x] Componentes con Auto layout, variables, propiedades y variantes de estado.
- [ ] Mockups construidos enteros con Auto layout y espacios sacados de variables.
- [ ] Pantalla principal en un segundo ancho, con los mismos componentes.
- [ ] Modo oscuro aplicado con el selector de modo en todas las pantallas completas.
- [ ] Prototipo que recorre el happy path completo.
- [x] Prueba 1 superada: al cambiar `color/primary`, cambian todas las pantallas a la vez.
- [ ] Prueba 2 superada: con todos los mockups en modo oscuro, nada desaparece contra el fondo.

## Resumen de decisiones

### Color
* **Color principal:** Púrpura arcano (`#7C3AED` en primitivos, asignado a `color/primary`). Lo he elegido porque es el típico color con el que se representa la magia y siento que pega bien con el estilo de la página.
* **Color secundario:** Ámbar dorado (`#D97706`, asignado a `color/secondary`), pensado para acentos de éxito y elementos activos.
* **Pareja de contraste más bajo:**
  * Modo claro: texto secundario `color/on-surface-variant` (`#6B7280`) sobre fondo `color/surface` (`#FFFFFF`), con ratio de **4.6:1** (supera el mínimo WCAG AA de 4.5:1).
  * Modo oscuro: texto secundario `color/on-surface-variant` (`#9CA3AF`) sobre tarjeta `color/surface-container` (`#1F2937`), con ratio de **4.8:1**.

### Tipografía
Se ha utilizado la familia tipográfica **Plus Jakarta Sans** (Google Fonts) en tres pesos: Regular (400), Medium (500) y Bold (700). Se eligió por su altura de la x amplia y su claridad geométrica, lo que facilita leer párrafos largos generados por la IA tanto en pantallas de ordenador como en móvil. Además, limitar la escala a una única familia en tres pesos permite no superar el límite de 500 KB para mantener un rendimiento óptimo de carga web.

### Espaciado y retícula
Se ha configurado una escala basada en **8 píxeles** (con valor submúltiplo de 4 px para paddings compactos de botones e iconos). Para la resolución de escritorio (1280 px), se estableció una retícula de **12 columnas** con margen lateral de **32 px** y medianil (*gutter*) de **24 px**, facilitando la agrupación de elementos relacionados mediante la ley de proximidad de Gestalt.

### Componentes
Se han organizado en la página `Componentes` aplicando Atomic Design:
* **Átomos:**
  * `Button`: botón con Auto Layout, altura mínima accesible de 44 px, variables de relleno y variantes de estado (`Default` y `Hover`).
* **Organismos:**
  * `Card / Action`: tarjeta contenedora para opciones de campaña con Auto Layout vertical, padding interno de 24 px (`spacing/card-padding`), esquinas redondeadas (`radius/card`), soporte nativo de modo oscuro y botón primario integrado.

### Responsive y modo oscuro
En la configuración de componentes, se definieron los textos y elementos interiores en *Fill container* (llenar contenedor) para permitir que las tarjetas se adapten fluidamente a distintos anchos de pantalla sin romperse. En el modo oscuro, se ajustaron las variables de superficie para elevar sutilmente el brillo de las tarjetas (`surface-container` en `#1F2937`) respecto al fondo general (`surface` en `#111827`), garantizando que la jerarquía y los límites visuales sigan siendo claros sin depender de sombras.

## Uso de IA
Se utilizó IA como asistente de consulta para estructurar el sistema de variables semánticas en dos colecciones, calcular los contrastes WCAG, organizar las prioridades de entrega y consultar dudas con Figma. También se empleó una pantalla base en Google Stitch para la mejora de algunos wireframes. El registro detallado de prompts, respuestas y decisiones conservadas o descartadas está documentado en el [CHANGELOG.md](CHANGELOG.md).

## Lo que ha quedado pendiente
Por falta de tiempo antes de la hora de entrega, no se ha podido completar el volcado de los mockups definitivos en su página correspondiente, ni la versión adaptada a móvil (412 px) con el prototipo navegable. La base del sistema de diseño (colecciones de variables semánticas y primitivas (sin sintaxis CSS), estilos de texto, efectos de elevación y componentes maestros de botón y tarjeta en Auto Layout) está completamente funcional en Figma, quedando pendiente la composición final de las pantallas y el enlace del flujo, además de mejorar un poco mas la guia de estilos.
