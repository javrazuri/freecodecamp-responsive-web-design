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