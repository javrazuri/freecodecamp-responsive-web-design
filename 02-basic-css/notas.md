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