# Notas freeCodeCamp - HTML Básico

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