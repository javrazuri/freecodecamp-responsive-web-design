# Anotaciones de CSS: Unidades de Viewport (`vh`) y `width: 100%`

## Entendiendo `vh` (Viewport Height) y `width: 100%`

En este paso, estamos configurando el tamaño inicial de nuestro `<body>` (el cuerpo de toda la página web) para asegurarnos de que ocupe el espacio completo de la ventana del navegador.

### 1. `width: 100%`

- **¿Qué es?** Esta propiedad le dice al `<body>` que debe ocupar el **100% del ancho disponible** de su elemento padre. Dado que el padre del `<body>` es el `<html>` y el `<html>` se ajusta a la ventana del navegador, `width: 100%` significa que el `<body>` se estirará horizontalmente para ocupar todo el ancho de la ventana visible.

### 2. `height: 100vh`

- **¿Qué es `vh`?** `vh` significa "viewport height" (altura del viewport). Es una **unidad de medida relativa** que se basa en la altura de la ventana visible del navegador (el "viewport").
- **¿Cómo funciona?**
    - `1vh` equivale al `1%` de la altura del viewport.
    - Por lo tanto, `100vh` significa que el elemento (`<body>` en este caso) ocupará el **100% de la altura total de la ventana visible** del navegador.

### ¿Por qué se usa `width: 100%` y `height: 100vh` en el `<body>`?

- **Rellenar la pantalla:** El objetivo principal es hacer que el `<body>` ocupe completamente la pantalla del usuario (tanto a lo ancho como a lo alto) desde el inicio.
- **Diseño de página completa:** Esto es fundamental para diseños donde quieres que el contenido se extienda por toda la pantalla, o si vas a centrar algo verticalmente, necesitas que el contenedor principal tenga una altura definida. Si no das una altura, el `<body>` solo crecerá hasta donde llegue su contenido. `100vh` lo fuerza a tomar toda la altura visible, incluso si el contenido es corto.

```css
body {
  width: 100%;  /* Ocupa todo el ancho de la ventana */
  height: 100vh; /* Ocupa toda la altura visible de la ventana */
}