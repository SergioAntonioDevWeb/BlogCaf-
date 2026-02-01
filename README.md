# BlogDeCafé �☕

Un blog web estático sobre café desarrollado con HTML5 y CSS3 puro, diseñado para compartir recetas, consejos y cursos sobre el mundo del café.

## 📋 Descripción del Proyecto

BlogDeCafé es un sitio web informativo que presenta:
- Artículos sobre tipos de granos de café y recetas
- Cursos y talleres sobre técnicas de preparación
- Sección de contacto para consultas
- Diseño totalmente responsive y optimizado

## 🚀 Características Principales

### ⚡ Rendimiento
- **Carga optimizada**: Preload de CSS crítico
- **Imágenes optimizadas**: Formato WebP con lazy loading
- **Fuentes optimizadas**: Preconnect a Google Fonts
- **Sin dependencias**: HTML/CSS puro para máxima velocidad

### 📱 Diseño Responsivo
- **Mobile-first**: Diseño adaptativo para todos los dispositivos
- **Breakpoint único**: 768px para tablets y superiores
- **CSS Grid y Flexbox**: Layout moderno y flexible
- **Unidades rem**: Escalado consistente basado en 10px

### 🎨 Estilo y Branding
- **Paleta de colores**: Tonos café profesional (#784d3c)
- **Tipografía**: Open Sans para párrafos, PT Sans para encabezados
- **BEM Naming**: Convenciones CSS consistentes y mantenibles
- **Variables CSS**: Facilidad de personalización y mantenimiento

## 📁 Estructura del Proyecto

```
BlogCafe/
├── 📄 index.html              # Página principal
├── 📄 nosotros.html           # Sobre nosotros
├── 📄 cursos.html             # Catálogo de cursos
├── 📄 contacto.html           # Formulario de contacto
├── 📄 entrada.html            # Plantilla de entrada de blog
├── 📁 css/
│   ├── 📄 normalize.css       # Reset CSS
│   └── 📄 styles.css          # Hoja de estilos principal
├── 📁 img/
│   ├── 🖼️ banner.webp         # Imagen del header
│   ├── 🖼️ blog1.webp          # Imágenes de blog
│   ├── 🖼️ blog2.webp
│   ├── 🖼️ blog3.webp
│   ├── 🖼️ nosotros.webp       # Sección sobre nosotros
│   ├── 🖼️ contacto.webp       # Fondo de contacto
│   └── 🖼️ curso1-3.webp       # Imágenes de cursos
├── 📄 README.md               # Documentación del proyecto
└── 📄 AGENTS.md               # Guía para desarrolladores
```

## 🛠️ Tecnologías Utilizadas

### Frontend
- **HTML5**: Semántica moderna y accesibilidad
- **CSS3**: Diseño avanzado con Grid y Flexbox
- **Variables CSS**: Personalización de temas
- **Media Queries**: Diseño responsivo

### Optimización
- **WebP**: Formato de imagen optimizado
- **Lazy Loading**: Carga diferida de imágenes
- **Preload**: Carga crítica prioritaria
- **Normalize.css**: Consistencia cross-browser

## 📋 Requisitos del Sistema

### Para Desarrollo Local
- Navegador web moderno (Chrome, Firefox, Safari, Edge)
- Servidor local opcional (ver sección de despliegue)
- Editor de código (VSCode, Sublime, etc.)

### Para Producción
- Servidor web estático (Apache, Nginx, GitHub Pages, Netlify)
- HTTPS recomendado

## 🚀 Instalación y Configuración

### 1. Clonar el Repositorio
```bash
git clone [URL-del-repositorio]
cd BlogCafe
```

### 2. Ejecución Local

#### Opción A: Abrir directamente
```bash
# Simplemente abre index.html en tu navegador
open index.html
```

#### Opción B: Servidor Python
```bash
python -m http.server 8000
# Abre http://localhost:8000
```

#### Opción C: Servidor Node.js
```bash
npx serve .
# Abre http://localhost:3000
```

## 📱 Navegación del Sitio

### Páginas Principales
1. **Inicio** (`index.html`) - Blog con artículos recientes
2. **Nosotros** (`nosotros.html`) - Información sobre el proyecto
3. **Cursos** (`cursos.html`) - Catálogo de cursos disponibles
4. **Contacto** (`contacto.html`) - Formulario de contacto
5. **Entrada** (`entrada.html`) - Plantilla para artículos individuales

### Componentes Reutilizables
- **Header**: Navegación principal con logo
- **Footer**: Enlaces de navegación duplicados
- **Sidebar**: Widget de cursos en página principal

## 🎯 Guía de Estilo y Convenciones

### HTML
- Usar atributo `lang="es"` para contenido en español
- Estructura semántica HTML5
- Atributos `alt` descriptivos en imágenes
- `loading="lazy"` en imágenes no críticas

### CSS
- **Metodología BEM**: `bloque__elemento--modificador`
- **Variables CSS**: Definidas en `:root`
- **Units**: `rem` para medidas, `px` solo para bordes
- **Mobile-first**: Media queries con `min-width`

### Nomenclatura
- **Archivos**: `kebab-case` (ej: `entrada.html`)
- **Clases**: BEM methodology
- **Imágenes**: Descriptivas en formato WebP

## 🔧 Personalización

### Cambiar Colores
Edita las variables CSS en `css/styles.css`:
```css
:root {
    --primario: #784d3c;  /* Color café principal */
    --gris: #e1e1e1;      /* Gris para bordes */
    --blanco: #ffffff;    /* Fondo */
    --negro: #000000;     /* Texto oscuro */
}
```

### Modificar Fuentes
Cambia las fuentes en el mismo archivo:
```css
:root {
    --fuenteHeading: 'PT Sans', sans-serif;
    --fuenteParrafos: 'Open Sans', sans-serif;
}
```

## 🌐 Despliegue

### Opciones de Hosting Gratuito
1. **GitHub Pages**
   - Configuración: Settings → Pages → Source: Main branch
   - URL: `https://[username].github.io/BlogCafe`
   - ✅ Optimizado con SEO y accesibilidad

2. **Netlify**
   - Arrastra la carpeta del proyecto
   - Despliegue automático con Git
   - ✅ Form compression y HTTPS automático

3. **Vercel**
   - Importa desde GitHub
   - Configuración cero para sitios estáticos
   - ✅ CDN global y edge optimization

### Hosting Propio
- Subir archivos al directorio público del servidor
- Asegurar configuración MIME para `.webp`
- Configurar HTTPS

## 🐛 Troubleshooting

### Problemas Comunes
1. **Imágenes no cargan**: Verificar rutas en `/img/`
2. **Fuentes no aparecen**: Revisar conexión a Google Fonts
3. **CSS no aplica**: Validar rutas a archivos CSS
4. **Responsividad rota**: Comprobar viewport meta tag

### ✅ Últimas Actualizaciones (v1.1)
- **SEO optimizado**: Metadatos únicos por página
- **Accesibilidad completa**: WCAG 2.1 AA compliance
- **Idioma corregido**: `lang="es"` en todo el sitio
- **Alt text mejorado**: Descriptivo y accesible
- **Microinteracciones**: Transiciones suaves y focus visible

## 📚 Documentación Adicional
- `ESTRUCTURA.md` - Desglose detallado de archivos
- `CAMBIOS.md` - Historial completo de optimizaciones
- `AGENTS.md` - Guía para desarrolladores

### Herramientas de Depuración
- **W3C Validator**: Validar HTML
- **CSS Lint**: Revisar calidad del CSS
- **Lighthouse**: Auditoría de rendimiento
- **Chrome DevTools**: Inspección responsive

## 🤝 Contribución

### Flujo de Trabajo
1. Fork del repositorio
2. Crear rama de feature: `git checkout -b nueva-funcionalidad`
3. Commit de cambios: `git commit -m 'Agregar nueva funcionalidad'`
4. Push: `git push origin nueva-funcionalidad`
5. Pull Request

### Estándares de Código
- Seguir convenciones BEM para CSS
- Validar HTML antes de commitear
- Mantener consistencia en indentación
- Comentarios descriptivos en CSS complejo

## 📄 Licencia

Este proyecto está bajo licencia MIT. Consulta el archivo `LICENSE` para más detalles.

## 📞 Contacto

Para consultas sobre el proyecto:
- **Email**: [email-del-proyecto]
- **GitHub Issues**: Reportar bugs o sugerencias
- **Formulario del sitio**: Página de contacto

---

**BlogDeCafé** - El aroma del conocimiento digital ☕📚