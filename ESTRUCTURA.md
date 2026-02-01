# 📁 Estructura de Archivos y Carpetas

## 📂 Desglose Detallado del Proyecto

### 🗂️ Archivos Principales HTML

#### `index.html` - Página Principal (125 líneas)
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <!-- Meta tags optimizados para SEO -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Página Web de Blog de Café">
    <title>BlogDecafé</title>
    
    <!-- Preload crítico para rendimiento -->
    <link rel="preload" href="css/normalize.css" as="style">
    <link rel="preload" href="css/styles.css" as="style">
    
    <!-- Google Fonts optimizadas -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
</head>
```

**Secciones principales:**
- **Header**: Navegación + banner hero
- **Main**: Blog con 3 artículos recientes + sidebar de cursos
- **Footer**: Navegación duplicada + logo

#### `nosotros.html` - Sobre Nosotros (~50 líneas)
- Estructura similar al index
- Contenido informativo sobre el blog
- Imagen de presentación `nosotros.webp`
- **Nota**: Usa `lang="en"` (debería ser `lang="es"`)

#### `cursos.html` - Catálogo de Cursos
- Lista de cursos disponibles
- Imágenes individuales para cada curso
- Estructura de grid responsive
- **Nota**: Usa `lang="en"` (debería ser `lang="es"`)

#### `contacto.html` - Formulario de Contacto (79 líneas)
```html
<form class="formulario">
    <div class="campo">
        <label class="campo__label" for="nombre">Nombre:</label>
        <input class="campo__field" type="text" placeholder="Tu Nombre" id="nombre">
    </div>
    <!-- Más campos... -->
</form>
```

#### `entrada.html` - Plantilla de Blog
- Plantilla reutilizable para artículos individuales
- Incluye imagen destacada
- Contenido de ejemplo con Lorem Ipsum
- **Nota**: Usa `lang="en"` (debería ser `lang="es"`)

---

### 🎨 Hojas de Estilo CSS

#### `css/normalize.css` (6.5 KB)
- Reset CSS para consistencia cross-browser
- Estandariza elementos HTML básicos
- Versión moderna y actualizada

#### `css/styles.css` (4.4 KB, 282 líneas)

##### 🎯 Estructura Organizada:
```css
:root {
    --fuenteHeading: 'PT Sans', sans-serif;
    --fuenteParrafos: 'Open Sans', sans-serif;
    --primario: #784d3c;
    --gris: #e1e1e1;
    --blanco: #ffffff;
    --negro: #000000;
}
```

##### 📋 Secciones Principales:
1. **Variables y Configuración Base** (líneas 1-23)
   - CSS Custom Properties
   - Box-sizing global
   - Tipografía base (62.5% = 10px)

2. **Estilos Globales** (líneas 25-72)
   - `.contenedor`: Layout principal
   - Enlaces y encabezados
   - Clases utilitarias

3. **Header** (líneas 74-124)
   - Background con banner.jpg
   - Navegación responsive
   - Logo y branding

4. **Blog y Contenido** (líneas 134-212)
   - Grid para blog + sidebar
   - Estilos de artículos
   - Botones primary/secondary

5. **Componentes Específicos**
   - Cursos (líneas 230-246)
   - Formulario (líneas 257-282)
   - Footer (líneas 214-218)

---

### 🖼️ Directorio de Imágenes (`/img/`)

#### 📊 Estadísticas:
- **Total**: 14 archivos
- **Formatos**: JPG + WebP (versión optimizada)
- **Peso total**: ~1.6 MB

#### 📋 Listado Completo:

| Archivo | Tamaño | Uso | Descripción |
|---------|--------|-----|-------------|
| `banner.webp` | 43.7 KB | Header principal | Imagen hero del sitio |
| `nosotros.webp` | N/A | Página sobre nosotros | Foto institucional |
| `contacto.webp` | 132.4 KB | Fondo contacto | Background de formulario |
| `blog1.webp` | 96.6 KB | Artículos blog | Imagen destacada |
| `blog2.webp` | 74.3 KB | Artículos blog | Imagen destacada |
| `blog3.webp` | 122.8 KB | Artículos blog | Imagen destacada |
| `curso1.webp` | 109.9 KB | Página cursos | Curso individual |
| `curso2.webp` | 125.2 KB | Página cursos | Curso individual |
| `curso3.webp` | 148.4 KB | Página cursos | Curso individual |

#### ✨ Optimizaciones Implementadas:
- **Formato WebP**: ~30% más ligero que JPEG
- **Lazy Loading**: `loading="lazy"` en imágenes no críticas
- **Preload**: Prioridad para imágenes críticas
- **Alt text**: Descriptivos para SEO y accesibilidad

---

### 🏗️ Arquitectura del Proyecto

#### 📦 Organización por Tipo:
```
BlogCafe/
├── 📄 HTML            # Contenido y estructura
├── 📁 css/           # Estilos y diseño
├── 📁 img/           # Recursos visuales
└── 📄 docs/          # Documentación (README, AGENTS.md)
```

#### 🔄 Flujo de Trabajo:
1. **Estructura HTML**: Semántica y accesible
2. **Estilos CSS**: Modular con BEM
3. **Assets**: Optimizados y versionados
4. **Docs**: Completa y actualizada

---

### 📝 Convenciones de Nomenclatura

#### 🏷️ Archivos:
- **HTML**: `kebab-case` (`pagina-seccion.html`)
- **CSS**: `lowercase` con descriptivos (`styles.css`)
- **Imágenes**: `descriptivo.webp` (`blog-entrada-principal.webp`)

#### 🎨 Clases CSS (BEM Methodology):
```css
.block                    /* Bloque principal */
.block__element           /* Elemento del bloque */
.block--modifier          /* Modificador del bloque */
.block__element--modifier /* Modificador de elemento */
```

**Ejemplos del proyecto:**
- `.header` (bloque)
- `.header__texto` (elemento)
- `.boton--primario` (modificador)
- `.widget-curso` (bloque compuesto)

---

### 🔗 Dependencias y Recursos Externos

#### 🌐 Google Fonts:
```html
<link href="https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&family=PT+Sans:ital,wght@0,400;0,700;1,400;1,700&display=swap" rel="stylesheet">
```
- **Open Sans**: Párrafos (multiple weights)
- **PT Sans**: Encabezados (regular, bold)

#### ⚡ Optimización de Carga:
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="preload" href="css/styles.css" as="style">
```

---

### 📊 Métricas del Proyecto

#### 📈 Estadísticas de Código:
- **Total líneas HTML**: ~400 líneas (5 archivos)
- **Total líneas CSS**: 282 líneas
- **Complejidad**: Baja (estático, sin JavaScript)
- **Mantenibilidad**: Alta (estructura modular)

#### 🎯 Optimizaciones:
- **No dependencies**: Sin framework JavaScript
- **CSS optimizado**: Variables, BEM, mobile-first
- **Imágenes WebP**: Formato moderno y ligero
- **Load performance**: Preload estratégico

---

### 🔄 Flujo de Desarrollo Sugerido

#### 📋 Nuevas Páginas:
1. Copiar estructura HTML existente
2. Mantener consistencia en header/footer
3. Aplicar clases CSS existentes
4. Optimizar imágenes en formato WebP
5. Validar con W3C antes de commitear

#### 🎨 Modificaciones de Estilo:
1. Editar variables CSS en `:root`
2. Usar clases BEM existentes
3. Mantener estructura móvil-first
4. Probar en múltiples dispositivos
5. Validar con herramientas de desarrollador

#### 📱 Testing Responsivo:
- **Móvil**: 320px - 767px
- **Tablet**: 768px - 1023px  
- **Desktop**: 1024px+

---

Esta estructura proporciona una base sólida, escalable y mantenible para el blog BlogDeCafé, siguiendo las mejores prácticas modernas de desarrollo web.