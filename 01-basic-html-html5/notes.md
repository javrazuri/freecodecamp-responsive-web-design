# Notas freeCodeCamp - HTML Básico
## 💻 Guía Rápida: Comandos Git en Terminal

### 🔄 Flujo básico para commits
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


## 📝 Comentarios en HTML

**Sintaxis:**
```html
<!-- Este es un comentario de prueba para html, también se puede poner números 123 -->
```

**Características:**
- No se muestran en la página web
- Útiles para documentar el código
- Pueden contener texto y números

---

## 🎯 Elemento `<main>`

**Definición:**
- Representa la parte más importante de una página
- **Solo un elemento** `<main>` por página
- Contiene el contenido principal y único del documento

**¿Por qué usarlo?**
- ✅ Buenas prácticas de desarrollo
- ✅ Mejor organización del código
- ✅ Mejora SEO y accesibilidad
- ✅ Estándar de la industria

**Ejemplo:**
```html
<main>
  <h1>Contenido principal</h1>
  <p>Información importante...</p>
</main>
```

---

## 📐 Indentación/Sangría

**Definición:**
Espacios que se utilizan en programación para dar jerarquía y mayor legibilidad visual.

**Propósito:**
- 🔍 **Legibilidad**: Código más fácil de leer
- 📊 **Jerarquía**: Muestra qué elementos están dentro de otros
- 👥 **Profesionalismo**: Estándar en la industria

**Ejemplo:**
```html
<main>
  <h1>Título</h1>        <!-- 2 espacios de indentación -->
  <p>Párrafo</p>          <!-- 2 espacios de indentación -->
</main>
```

---

## 📈 Progreso
- [ ] Step 1-4: Completados
- [x] Step 5: Elemento `<main>` ✅
- [ ] Step 6: Pendiente

---

*💡 Tip: Usar `Shift + Alt + F` en VS Code para auto-indentar*

## elemento Figure
- Es un contenedor semántico que se utiliza para poner elementos como imágenes y gráficos. Es importante porque a ese contenedor se le puede dar más adelante estilo CSS y ya no usar un div. También es positivo para el SEO y para accesibilidad.
- **`<figcaption>`**: Proporciona una descripción o título para el contenido de `<figure>`.

**Ejemplo**
<figure>
  <img src="gato.jpg" alt="Un gato naranja">
  <figcaption>Este es mi gato Garfield durmiendo</figcaption>
</figure>

## Form ##
- Acá empezamos con los formularios que sirven para enviar la información de un usuario y que se envía a un servidor.

**Ejemplo:**
<form action="https://freecatphotoapp.com/submit-cat-photo">
  <!-- Aquí van los campos del formulario -->
</form>

- **action**: En este caso, action es un atributo, y este atributo nos indica hacía donde va dirigida la información que se envía mediante el formulario. 
- **Sin action**: Si no especificas una URL, el formulario se envía a la misma página actual, pero esto generalmente no es útil porque la página no está preparada para procesar esos datos.
- **Con action específico**: Los datos van al destino correcto donde hay código del servidor esperando procesarlos.

📅 4 de junio de 2025

## FORM: label ##
- El label es una etiqueta descriptiva que se enlaza con el input y sirve para dar un orden al código y para temas de accesibilidad. 
<label> <input type="text"> </label>

## FORM: id ##
- El id es darle un nombre y apellido a la información que va a enviar el input, y también para darle estilo y funcionamiento mediante css/js
<label> <input type="text" id="nombre-de-mascota">Nombre de Mascota</label>

## FORM: name ##
- **Propósito:** Identifica y agrupa elementos del formulario.
- **Funciones clave:**
  - Agrupa elementos relacionados (ej: `radio` buttons con el mismo `name`)
  - Nombre del campo al enviar datos al servidor (aparece en `nombre=valor`)
  - Mejora UX al permitir selección única en `radio` buttons

## FORM: value ##
- **Propósito:** Define valores para diferentes tipos de campos.

### Comportamiento según tipo de campo:
1. **Campos editables** (`text`, `email`, `number`, etc.):
   - Valor inicial mostrado
   - Puede ser modificado por el usuario
   - Ejemplo:
     ```html
     <input type="text" name="user" value="Negrito">
     ```

2. **Opciones seleccionables** (`radio`, `checkbox`, `select`):
   - Valor oculto que se envía al servidor
   - No es lo mismo que el texto visible
   - Ejemplos:
     ```html
     <input type="radio" name="sistema" value="windows"> Windows
     <input type="checkbox" name="color" value="azul"> Azul
     ```

3. **Botones** (`submit`, `button`, `reset`):
   - Texto que muestra el botón
   - En botones de submit con `name`, también se envía el valor
   - Ejemplo:
     ```html
     <input type="submit" value="Enviar">
     ```

### Excepciones:
- `type="file"`: No usa `value` (envía el archivo seleccionado)
  ```html
  <input type="file" name="documento">

## FORM: fieldset ##
- Es un elemento que sirve para agrupar `input` y `label`.

## FORM: legend ##
- Es un elemento que actua como el tidulo del fieldset es una etiqueta con apertura y cierre.

## FORM: Atributo `for` en etiquetas `<label>`

### 📌 Definición
El atributo `for` en un elemento `<label>` crea una conexión explícita entre:
- La descripción textual (lo que ve el usuario)
- El campo de formulario asociado (input, select, textarea)

### 🔍 ¿Cómo funciona?
```html
<!-- Ejemplo básico para freecodecamp, en practica primero va el label-->
<input type="checkbox" id="terminos">
<label for="terminos">Acepto los términos y condiciones</label>

