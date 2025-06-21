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


# Anotaciones de HTML: Atributo `method` en Formularios

## Entendiendo el atributo `method` en `<form>`

El atributo `method` dentro de una etiqueta `<form>` es crucial porque especifica **cómo** los datos del formulario se van a enviar (es decir, cómo van a viajar) al servidor, a la URL que se indica en el atributo `action`.

Los dos métodos más comunes son `GET` y `POST`:

### 1. `method="get"` (Solicitud GET)

- **¿Cómo envía los datos?** Los datos del formulario se añaden directamente a la URL como **parámetros de consulta** (query parameters).
    - Verás los datos en la barra de direcciones del navegador.
    - Ejemplo: `https://tuweb.com/procesar?nombre=Juan&email=juan@ejemplo.com`
- **¿Cuándo usarlo?**
    - Para **solicitudes que solo recuperan datos** (por ejemplo, búsquedas).
    - Cuando los datos **no son sensibles** y no importa que sean visibles en la URL.
    - Cuando los usuarios podrían querer **marcar la página con los parámetros** (ej., resultados de búsqueda).
- **Limitaciones:** Los navegadores y servidores tienen límites en la longitud de las URLs, por lo que no es ideal para enviar grandes cantidades de datos.

### 2. `method="post"` (Solicitud POST)

- **¿Cómo envía los datos?** Los datos del formulario se envían en el **cuerpo de la solicitud HTTP**, no en la URL.
    - Los datos **no son visibles** en la barra de direcciones del navegador.
- **¿Cuándo usarlo?**
    - Para **enviar datos sensibles** (contraseñas, información personal).
    - Cuando se **modifican datos en el servidor** (ej., crear una cuenta, publicar un comentario, subir un archivo).
    - Cuando se envían **grandes cantidades de datos** (no hay límites prácticos como en `GET`).
    - Cuando no quieres que el usuario pueda "recargar" accidentalmente la acción (