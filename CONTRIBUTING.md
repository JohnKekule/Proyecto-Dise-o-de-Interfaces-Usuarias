# Guía de Contribución

¡Gracias por tu interés en contribuir al proyecto **Mejor Aula para Alumnos (DIU)**! Esta guía te ayudará a entender cómo puedes participar en el desarrollo del proyecto.

## Código de Conducta

Al participar en este proyecto, aceptas mantener un ambiente respetuoso y constructivo. Se espera que todos los colaboradores:

- Sean respetuosos y constructivos en sus comentarios
- Acepten críticas constructivas
- Se enfoquen en lo que es mejor para la comunidad
- Muestren empatía hacia otros miembros de la comunidad

## Cómo Contribuir

### Reportar Bugs

Si encuentras un bug, por favor crea un issue con:

1. **Título descriptivo**: Resumen claro del problema
2. **Descripción detallada**: Qué esperabas que pasara vs. qué pasó realmente
3. **Pasos para reproducir**: Lista numerada de pasos
4. **Entorno**: Navegador, versión, sistema operativo
5. **Screenshots**: Si es aplicable

### Sugerir Mejoras

Para proponer nuevas características:

1. Verifica que no exista un issue similar
2. Crea un nuevo issue con la etiqueta "enhancement"
3. Describe claramente la mejora propuesta
4. Explica por qué sería útil para el proyecto
5. Si es posible, proporciona mockups o ejemplos

### Contribuir con Código

#### Preparación del Entorno

1. **Fork el repositorio**
   ```bash
   # Clona tu fork
   git clone https://github.com/tu-usuario/Proyecto-Dise-o-de-Interfaces-Usuarias.git
   cd Proyecto-Dise-o-de-Interfaces-Usuarias
   
   # Agrega el repositorio original como upstream
   git remote add upstream https://github.com/JohnKekule/Proyecto-Dise-o-de-Interfaces-Usuarias.git
   ```

2. **Crea una rama para tu contribución**
   ```bash
   git checkout -b feature/nombre-de-la-feature
   # o
   git checkout -b fix/descripcion-del-fix
   ```

#### Estándares de Código

##### HTML
- Usa indentación de 2 espacios
- Incluye atributos `alt` en imágenes
- Usa semántica HTML5 apropiada
- Asegúrate de que el código sea accesible (WCAG 2.1)

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Título descriptivo</title>
</head>
<body>
  <main>
    <h1>Título principal</h1>
    <p>Contenido descriptivo</p>
  </main>
</body>
</html>
```

##### CSS
- Usa metodología BEM para nomenclatura
- Agrupa propiedades lógicamente
- Usa variables CSS para valores reutilizables
- Prioriza CSS Grid y Flexbox para layouts

```css
/* Ejemplo de BEM */
.card {
  display: flex;
  flex-direction: column;
}

.card__header {
  padding: 1rem;
}

.card__title {
  font-size: 1.5rem;
  font-weight: 600;
}

.card--featured {
  border: 2px solid var(--primary-color);
}
```

##### JavaScript
- Usa ES6+ features
- Prefiere `const` y `let` sobre `var`
- Usa funciones arrow cuando sea apropiado
- Comenta código complejo

```javascript
// Ejemplo de función bien documentada
const toggleMobileMenu = () => {
  const menu = document.querySelector('.mobile-menu');
  const isOpen = menu.classList.contains('mobile-menu--open');
  
  menu.classList.toggle('mobile-menu--open');
  menu.setAttribute('aria-expanded', !isOpen);
};
```

#### Mensajes de Commit

Usa el formato de [Conventional Commits](https://www.conventionalcommits.org/):

```
<tipo>[ámbito opcional]: <descripción>

[cuerpo opcional]

[pie opcional]
```

**Tipos permitidos:**
- `feat`: Nueva característica
- `fix`: Corrección de bug
- `docs`: Cambios en documentación
- `style`: Cambios de formato (no afectan funcionalidad)
- `refactor`: Refactorización de código
- `test`: Agregar o modificar tests
- `chore`: Tareas de mantenimiento

**Ejemplos:**
```bash
git commit -m "feat: agrega navegación responsive"
git commit -m "fix: corrige alineación en dispositivos móviles"
git commit -m "docs: actualiza guía de instalación"
```

#### Pull Requests

1. **Antes de crear el PR:**
   - Asegúrate de que tu código sigue los estándares establecidos
   - Ejecuta las pruebas (cuando estén disponibles)
   - Actualiza la documentación si es necesario

2. **Crear el PR:**
   - Usa un título descriptivo
   - Incluye una descripción detallada de los cambios
   - Referencia issues relacionados (#123)
   - Agrega screenshots si hay cambios visuales

3. **Template de PR:**
   ```markdown
   ## Descripción
   Breve descripción de los cambios realizados.

   ## Tipo de cambio
   - [ ] Bug fix
   - [ ] Nueva característica
   - [ ] Cambio que rompe compatibilidad
   - [ ] Actualización de documentación

   ## ¿Cómo se ha probado?
   Descripción de las pruebas realizadas.

   ## Screenshots (si aplica)
   Agrega screenshots de los cambios visuales.

   ## Checklist
   - [ ] Mi código sigue los estándares del proyecto
   - [ ] He realizado una auto-revisión de mi código
   - [ ] He comentado mi código, especialmente en áreas difíciles de entender
   - [ ] He realizado los cambios correspondientes en la documentación
   - [ ] Mis cambios no generan nuevas advertencias
   ```

## Estructura de Carpetas

```
├── docs/           # Documentación técnica y de usuario
│   ├── api/        # Documentación de API (si aplica)
│   ├── design/     # Guías de diseño y estilo
│   └── guides/     # Tutoriales y guías
├── src/            # Código fuente
│   ├── css/        # Hojas de estilo
│   ├── js/         # Scripts JavaScript
│   ├── images/     # Imágenes del proyecto
│   └── index.html  # Página principal
├── tests/          # Pruebas automatizadas
│   ├── unit/       # Pruebas unitarias
│   └── integration/ # Pruebas de integración
└── assets/         # Recursos estáticos compartidos
    ├── icons/      # Iconos del proyecto
    ├── fonts/      # Fuentes personalizadas
    └── mockups/    # Mockups y wireframes
```

## Proceso de Revisión

1. Todos los PRs requieren al menos una revisión
2. Los cambios deben pasar las pruebas automatizadas (cuando estén implementadas)
3. Se debe mantener la cobertura de código
4. Los cambios grandes deben discutirse en un issue primero

## Preguntas

Si tienes preguntas sobre cómo contribuir:

1. Revisa los issues existentes
2. Crea un nuevo issue con la etiqueta "question"
3. Contacta a los mantenedores del proyecto

## Reconocimientos

Todos los contribuidores serán reconocidos en el README del proyecto. ¡Gracias por hacer que este proyecto sea mejor!

---

**¡Esperamos tus contribuciones!** 🚀