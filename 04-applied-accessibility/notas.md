### 27 de junio de 2025

# Anotaciones de CSS: `box-sizing` y el Modelo de Caja

## Entendiendo `box-sizing` (Paso 8 - Colored Markers)

El `box-sizing` es una propiedad CSS crucial que define **cómo el navegador calcula el tamaño total de un elemento** (su `width` y `height`) cuando le aplicas `padding` (relleno) y `border` (borde).

Por defecto, los navegadores usan el modelo `content-box`.

### 1. El modelo `content-box` (valor por defecto)

-   **¿Cómo calcula el tamaño?** Con `content-box`, cuando le das un `width` o `height` a un elemento, ese tamaño se aplica **SOLO al contenido del elemento**.
-   **¿Qué pasa con el `padding` y `border`?** Cualquier `padding` (relleno) o `border` (borde) que añadas a ese elemento se **SUMARÁ** al `width` y `height` que ya definiste para el contenido.
-   **Resultado:** El elemento **crecerá más allá** del `width` y `height` que especificaste inicialmente.

**Ejemplo visual:**

Si tienes un `div` con `width: 100px;` y `padding: 10px; border: 5px solid;`:


Como puedes ver, el ancho total del elemento (incluyendo bordes y rellenos) es mayor que los 100px que le diste inicialmente.

### ¿Por qué lo notas en el Paso 8 del curso?

El curso menciona que el borde azul de la imagen se extiende más allá del borde rojo de la galería. Esto ocurre porque la `width` del elemento de la imagen solo considera el contenido, y su `padding` y `border` se **añaden a ese ancho**, haciéndolo "desbordarse" de su contenedor.

### `box-sizing: content-box;` con el selector universal `*`

-   El ejercicio te pide que configures explícitamente `box-sizing: content-box;` usando el selector universal (`*`).
-   El selector universal (`*`) aplica la regla a **todos los elementos** de tu página.
-   **No verás cambios en este paso** porque `content-box` es el **valor por defecto** en los navegadores. Lo que freeCodeCamp busca es que lo configures explícitamente y lo notes, antes de presentarte la alternativa (`border-box`) que sí genera un cambio visual.

### En resumen:

`box-sizing: content-box;` es el modelo predeterminado donde el `width` y `height` solo se aplican al **contenido**. El `padding` y el `border` **se añaden** a ese tamaño, haciendo que el elemento total sea más grande de lo que esperabas si solo mirabas el `width/height` definido. Es fundamental entender esto antes de pasar al modelo alternativo que soluciona muchos problemas de layout.