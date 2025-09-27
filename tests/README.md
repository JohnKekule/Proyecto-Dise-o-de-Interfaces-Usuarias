# Pruebas del Proyecto

Esta carpeta contendrá todas las pruebas automatizadas del proyecto.

## Estructura de Pruebas

- `unit/` - Pruebas unitarias de funciones individuales
- `integration/` - Pruebas de integración entre componentes
- `e2e/` - Pruebas end-to-end de funcionalidad completa
- `accessibility/` - Pruebas específicas de accesibilidad

## Tecnologías de Pruebas (Planificadas)

- **Jest** - Framework de pruebas unitarias
- **Cypress** - Pruebas end-to-end
- **axe-core** - Pruebas de accesibilidad
- **Lighthouse CI** - Pruebas de rendimiento

## Ejecutar Pruebas

```bash
# Instalar dependencias (cuando estén disponibles)
npm install

# Ejecutar todas las pruebas
npm test

# Ejecutar pruebas específicas
npm run test:unit
npm run test:integration
npm run test:e2e

# Generar reporte de cobertura
npm run test:coverage
```

## Escribir Pruebas

- Sigue el patrón AAA (Arrange, Act, Assert)
- Usa nombres descriptivos para las pruebas
- Incluye casos edge y de error
- Mantén las pruebas simples y enfocadas