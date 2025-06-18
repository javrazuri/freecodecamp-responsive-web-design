### 12 de junio de 2025 - CSS

# 🔄 Flujo básico para commits
```bash
# 1. Navegar al directorio del proyecto
cd ruta/a/tu/proyecto

# 2. Verificar archivos modificados
git status

# 3. Añadir cambios al staging area
git add .

# 4. Crear commit con mensaje descriptivo
git commit -m "✨ Descripción breve de los cambios"

# 5. Subir cambios a GitHub (rama principal)
git push origin main

## ¿Qué es un div?
Es una etiqueta genérica que sirve para agrupar cosas en el HTML, normalmente para diseñar mejor la página con CSS . No tiene significado especial, solo es útil para organizar el diseño.

## 📝 Clases (`.class`) e IDs (`#id`) en HTML y CSS

### 🔹 Clase `.menu`
- Se usa con el atributo `class` en HTML.
- Ejemplo: `<div class="menu"></div>`
- En CSS: `.menu { ... }`
- ✅ Puedes usarla en **múltiples elementos**.
- Ideal para aplicar **estilos repetidos** o comunes.

### 🔹 ID `#menu`
- Se usa con el atributo `id` en HTML.
- Ejemplo: `<div id="menu"></div>`
- En CSS: `#menu { ... }`
- ❗ Solo debe usarse **una vez por página**.
- Ideal para elementos **únicos**, como menús, encabezados o secciones principales.

### ⚠️ Importante:
- Usar varios `id` iguales **no es correcto semánticamente**, aunque el navegador lo acepte.
- Para aplicar estilos a muchos elementos, **usa clases**.
- Usa `id` cuando necesites apuntar a un elemento único desde CSS o JavaScript.

---

### 💡 Consejo adicional:

> Si vas a usar JavaScript para manipular elementos, las **clases** son más flexibles, mientras que los **ids** te permiten seleccionar rápidamente un elemento con `document.getElementById("menu")`.

### 18 de junio de 2025 - CSS
# Anotaciones de CSS: Selectores Específicos (Clase + Elemento)

## Concepto Clave: Selectores Descendentes (`.clase elemento`)

Cuando usamos un selector que combina una clase y un elemento, como por ejemplo:

`.nombre-de-la-clase etiqueta-html`

...lo que estamos haciendo es ser **muy específicos** con qué elementos HTML queremos aplicar un estilo.

### ¿Qué significa exactamente?

Este tipo de selector le dice a CSS:

- **"Encuentra cualquier elemento que tenga la clase `nombre-de-la-clase`."**
- **"Y, *dentro* de ese elemento (o de cualquier descendiente suyo), encuentra todos los `etiqueta-html`."**
- **"Solo a *esos* elementos `etiqueta-html` (los que están dentro de la clase especificada) se les aplicarán los estilos definidos."**

### Ejemplo práctico:

Imagina este HTML:

```html
<div class="contenedor-principal">
  <p>Este párrafo es azul.</p>
</div>

<p>Este párrafo NO es azul.</p>

# Anotaciones de CSS: `display: inline-block`

## Entendiendo `display: inline-block` y el control de ancho

La propiedad `display: inline-block;` es una combinación de dos comportamientos de visualización de elementos HTML:

1.  **Como `inline`**: Permite que el elemento se coloque **en la misma línea** que otros elementos (si hay espacio). Esto es ideal cuando quieres que varios elementos aparezcan uno al lado del otro, como en un menú donde el nombre del producto y su precio comparten la misma línea.

2.  **Como `block`**: A diferencia de un elemento `inline` puro, un `inline-block` te permite **establecer propiedades de bloque** como `width` (ancho), `height` (alto), `margin` (margen) y `padding` (relleno). Esto te da control sobre sus dimensiones y el espacio a su alrededor.

### El punto clave sobre el ancho con `inline-block`:

Por defecto, los elementos `inline-block` **solo ocupan el ancho necesario para su propio contenido**. Esto significa que si no les indicas un ancho específico, se "pegarán" a los elementos contiguos, sin expandirse para llenar el espacio disponible en su línea.

**Ejemplo:** Si tienes un nombre de producto y un precio como `inline-block` sin un ancho definido:

### La solución para distribuir el espacio: Usar `width`

Para que los elementos `inline-block` se distribuyan y ocupen el espacio deseado (por ejemplo, para que uno se alinee a la izquierda y otro a la derecha dentro de un contenedor), necesitas asignarles una propiedad `width` explícitamente.

**Ejemplo:** Si asignas `width: 50%;` a dos elementos `inline-block` adyacentes dentro de un contenedor:

```css
.elemento-izquierdo {
  display: inline-block;
  width: 50%; /* Ocupará la mitad del ancho del padre */
}
.elemento-derecho {
  display: inline-block;
  width: 50%; /* Ocupará la otra mitad del ancho del padre */
}

# Anotaciones de CSS: `max-width` (Ancho Máximo)

## Entendiendo `max-width`

La propiedad `max-width` (ancho máximo) es como un "techo" para el tamaño de un elemento. Le dice al navegador que un elemento **nunca debe ser más ancho que el valor especificado**.

### ¿Por qué y cuándo usar `max-width`?

Imagina tu menú del café:
- Le diste un `width: 80%;`, lo que significa que siempre ocupará el 80% del ancho de la pantalla.
- En pantallas pequeñas, esto funciona bien. Pero en pantallas **muy anchas** (como un monitor grande), ese 80% puede ser ¡enorme! Los nombres del café y los precios se verían súper separados y el menú se estiraría demasiado.

Aquí es donde entra `max-width: 500px;` (en el caso de tu menú):

- Le estás diciendo al `.menu`: "Puedes crecer hasta ocupar el 80% de la pantalla, **PERO NUNCA PASES DE 500 píxeles de ancho**, incluso si el 80% es más grande que 500px."

### Cómo funciona en la práctica:

- **Si la pantalla es pequeña (ej., 600px de ancho):**
    - El `width: 80%` haría que el menú sea 480px de ancho (80% de 600px).
    - Como 480px es **menor** que `max-width: 500px`, el menú se quedará en 480px. ¡Todo bien!

- **Si la pantalla es muy grande (ej., 1000px de ancho):**
    - El `width: 80%` haría que el menú sea 800px de ancho (80% de 1000px).
    - Pero como `max-width` es 500px, el menú **no crecerá más allá de 500px**, aunque tenga espacio. Se mantendrá en 500px. ¡Así evitas que se estire demasiado!

### En resumen:

`max-width` es clave para el **diseño responsivo**. Asegura que tus elementos sean flexibles y ocupen un porcentaje del espacio disponible, pero los **limita** a un tamaño máximo para que no se vean raros o ilegibles en pantallas muy grandes. Ayuda a que tu diseño se vea bien en cualquier dispositivo.