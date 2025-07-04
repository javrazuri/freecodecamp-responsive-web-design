# Anotaciones de HTML: `aria-labelledby` y Roles de Región (Paso 16)

## Entendiendo `aria-labelledby` y la Accesibilidad en Regiones

El Paso 16 te introduce a una práctica fundamental para hacer tus páginas web accesibles, especialmente para usuarios que dependen de lectores de pantalla.

### El Problema de las "Regiones" sin Etiqueta

Cuando defines un `role="region"` (como a menudo se hace implícitamente con elementos como `<section>` o `<aside>` que tienen un significado estructural en la página), estás creando un área de contenido importante.

Imagina a un usuario de lector de pantalla navegando por tu página. Sin una etiqueta clara, el lector de pantalla podría anunciar "Región" o "Sección", pero el usuario no sabría **cuál es el propósito** de esa región (¿es la información del estudiante? ¿Preguntas de HTML? ¿Un área de navegación?). Esto puede ser muy confuso y frustrante.

### La Solución: `aria-labelledby` y un Encabezado (`h2`)

`aria-labelledby` es un atributo de ARIA que sirve como una **etiqueta accesible** para un elemento. Le dice a las tecnologías de asistencia (como los lectores de pantalla) que el "nombre" o "título" de este elemento está definido por el texto de **otro elemento** en la página.

En este paso, la técnica es la siguiente:

1.  **Dentro de cada `<section>`** (que actúa como una "región" de contenido):
    * Creas un elemento de encabezado (en este caso, un `<h2>`).
    * A ese `<h2>` le das un **`id` único** (ej., `id="student-info"`). Este `h2` contendrá el texto que describe el propósito de la sección.

    ```html
    <section>
      <h2 id="student-info">Información del Estudiante</h2>
      </section>
    ```

2.  **Al elemento `<section>` mismo:**
    * Le añades el atributo `aria-labelledby`.
    * El valor de `aria-labelledby` será el **`id` del `h2`** que acabas de crear (ej., `aria-labelledby="student-info"`).

    ```html
    <section aria-labelledby="student-info">
      <h2 id="student-info">Información del Estudiante</h2>
      </section>
    ```

### ¿Qué logra esto?

Cuando un lector de pantalla llega a la `<section>`:

* Reconoce que es una "región" (por su semántica o un `role="region"` explícito).
* Busca el `aria-labelledby` en esa sección.
* Encuentra el `id` (`student-info`) y luego busca el elemento con ese `id` (nuestro `<h2>`).
* Lee el texto del `<h2>` ("Información del Estudiante") para anunciar al usuario el **propósito de esa sección**.

Esto proporciona una experiencia de navegación mucho más clara y eficiente para usuarios de tecnologías de asistencia.

### Aplicación en tu Código:

Se te pide aplicar esto a tres secciones:

* **`section` para "student-info"**:
    ```html
    <section aria-labelledby="student-info">
      <h2 id="student-info">Información del Estudiante</h2>
      </section>
    ```
* **`section` para "html-questions"**:
    ```html
    <section aria-labelledby="html-questions">
      <h2 id="html-questions">Preguntas de HTML</h2>
      </section>
    ```
* **`section` para "css-questions"**:
    ```html
    <section aria-labelledby="css-questions">
      <h2 id="css-questions">Preguntas de CSS</h2>
      </section>
    ```

En resumen, `aria-labelledby` es una herramienta ARIA vital para la accesibilidad. Permite asociar un texto descriptivo (generalmente de un encabezado existente) a un elemento de "región", permitiendo que los lectores de pantalla anuncien claramente el propósito de esa sección a los usuarios.