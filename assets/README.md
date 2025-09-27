# Assets del Proyecto

Esta carpeta contiene todos los recursos estáticos del proyecto.

## Estructura de Assets

- `icons/` - Iconos del sistema (SVG preferentemente)
- `images/` - Imágenes y fotografías
- `fonts/` - Fuentes tipográficas personalizadas
- `mockups/` - Diseños y wireframes del proyecto
- `logos/` - Logotipos y marca del proyecto

## Guías de Assets

### Iconos
- Formato preferido: SVG
- Tamaño estándar: 24x24px
- Usa nomenclatura descriptiva: `icon-menu.svg`
- Optimiza los SVG antes de añadirlos

### Imágenes
- Formato: WebP (con fallback a JPG/PNG)
- Optimiza para web (compresión adecuada)
- Incluye versiones responsive cuando sea necesario
- Usa alt text descriptivo en el HTML

### Fuentes
- Formatos: WOFF2, WOFF, TTF
- Incluye solo los pesos necesarios
- Considera la carga de fuentes para rendimiento

### Mockups
- Formato: Figma, Sketch, o PDF
- Incluye versiones para diferentes dispositivos
- Documenta las decisiones de diseño

## Optimización

- Comprime todas las imágenes
- Usa herramientas como TinyPNG o ImageOptim
- Considera lazy loading para imágenes grandes
- Implementa caching apropiado