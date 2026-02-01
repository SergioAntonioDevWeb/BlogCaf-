# AGENTS.md

## Project Overview

BlogDeCafé is a static HTML/CSS blog website about coffee. This is a simple frontend project with no build tools, package managers, or testing frameworks.

## Development Commands

Since this is a static website, there are no build commands. Development workflow:

- **Local development**: Open HTML files directly in a browser or use a local server
- **Live server**: `python -m http.server 8000` or `npx serve .` (if Node.js available)
- **Validation**: Use HTML validator and CSS linting tools manually

## Code Style Guidelines

### HTML Structure
- Use semantic HTML5 elements appropriately (`<header>`, `<main>`, `<article>`, `<aside>`, `<footer>`)
- Use double quotes for attributes
- Include proper meta tags: charset, viewport, description
- Use `lang="es"` for Spanish content (✅ FIXED: All pages now use correct language)
- Include `loading="lazy"` on images for performance
- Use BEM-style class naming with double underscores for elements and double hyphens for modifiers

### CSS Architecture
- Follow CSS custom properties (variables) for colors and fonts defined in `:root`
- Use mobile-first responsive design with `@media (min-width: 768px)` breakpoints
- Organize CSS with clear section comments:
  ```css
  /** Header **/
  /** Globales **/
  /** Utilidades **/
  ```
- Use rem units for font sizes and spacing (base: 62.5% = 10px)
- Use BEM naming convention for classes
- Maintain consistent spacing patterns (2rem base unit)

### File Organization
```
/
├── index.html          # Homepage
├── nosotros.html       # About page  
├── cursos.html         # Courses page
├── contacto.html       # Contact page
├── entrada.html        # Blog entry page
├── css/
│   ├── normalize.css   # CSS reset
│   └── styles.css      # Main stylesheet
└── img/               # Images directory
```

### Naming Conventions
- **Files**: Use lowercase with hyphens (kebab-case)
- **Classes**: BEM methodology (block__element--modifier)
  - `header__texto` (element)
  - `boton--primario` (modifier)
  - `widget-curso` (block)
- **Images**: Use descriptive names with webp format for performance

### Accessibility Guidelines
- Include proper alt text for all images
- Use semantic heading hierarchy (h1 → h2 → h3)
- Maintain color contrast ratios
- Use proper link text descriptions
- Include `lang` attribute on HTML tags

### Performance Considerations
- Use `rel="preload"` for critical CSS
- Optimize images in WebP format
- Use lazy loading for non-critical images
- Minimize external font requests with `preconnect`

### Code Quality
- Keep HTML semantic and well-indented
- Use consistent indentation (2-4 spaces)
- Group related CSS rules together
- Add descriptive comments for complex sections
- Validate HTML and CSS regularly

### Spanish Language Support
- Primary language should be Spanish (lang="es")
- Content should be in Spanish
- Maintain consistent language across all pages

## ✅ Recent Fixes Applied (v1.1)
- ✅ Fixed: All pages now use `lang="es"` instead of `lang="en"`
- ✅ Fixed: Improved alt text for all images with descriptive content
- ✅ Fixed: Added unique meta descriptions and keywords per page
- ✅ Added: Schema.org microdata for blog posts
- ✅ Added: Focus visible states and keyboard navigation
- ✅ Added: Smooth transitions and microinteractions
- ✅ Optimized: Google Fonts loading (removed unused weights)

## Remaining Improvements
- Consider adding a proper 404 page
- Implement proper form validation on contact page
- Add favicon for better branding
- Consider CSS critical inlining for performance

## Browser Support
- Target modern browsers (Chrome, Firefox, Safari, Edge)
- Use CSS Grid and Flexbox for layout
- Ensure responsive design works on mobile devices
- Test cross-browser compatibility

## Security Notes
- No server-side components, minimal security concerns
- Validate user inputs in contact forms (client-side only)
- Use HTTPS in production
- Consider CSP headers if deployed