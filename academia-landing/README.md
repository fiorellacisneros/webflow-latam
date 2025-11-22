# Landing Page - Academia WebflowLATAM

Landing page para el módulo de Academia de la plataforma WebflowLATAM, diseñada siguiendo el PRD y las mejores prácticas de desarrollo web.

## 📁 Estructura de Carpetas

```
academia-landing/
├── index.html          # Página principal
├── css/
│   └── styles.css      # Estilos personalizados
├── js/
│   └── main.js         # JavaScript principal
├── images/             # Imágenes y assets
├── assets/             # Otros recursos
└── README.md           # Este archivo
```

## 🎨 Tecnologías Utilizadas

- **HTML5**: Semántico y accesible
- **Tailwind CSS**: Framework CSS utility-first (vía CDN)
- **CSS Custom**: Estilos personalizados siguiendo el design system del PRD
- **JavaScript Vanilla**: Sin dependencias, código limpio y mantenible
- **Google Fonts**: Inter (tipografía del PRD)

## 🎯 Características

### Diseño
- ✅ Responsive (Mobile-first)
- ✅ Accesible (WCAG guidelines)
- ✅ Performance optimizado
- ✅ SEO friendly
- ✅ Design system del PRD implementado

### Secciones
1. **Hero Section**: CTA principal, social proof
2. **Benefits**: 3 beneficios clave
3. **Cursos**: Grid de cursos con filtros
4. **Certificaciones**: Información sobre certificaciones
5. **Comunidad**: Características de la comunidad
6. **Precios**: 3 planes (Free, Pro, Agency)
7. **CTA Final**: Conversión principal
8. **Footer**: Links y información

### CTAs Implementados
- **Primario**: "Explorar Cursos Gratis", "Comenzar Gratis"
- **Secundario**: "Ver Preview", "Ver Planes"
- **Terciario**: Links con iconos

## 🚀 Cómo Usar

### Desarrollo Local

1. Abre `index.html` en tu navegador
2. O usa un servidor local:
   ```bash
   # Con Python
   python -m http.server 8000
   
   # Con Node.js (http-server)
   npx http-server
   ```

### Personalización

#### Colores
Los colores están definidos en el PRD y configurados en Tailwind:
- Primary: `#0066FF`
- Secondary Green: `#00C853`
- Secondary Orange: `#FF6B35`
- Secondary Yellow: `#FFC107`

#### Tipografía
- Fuente: Inter (Google Fonts)
- Tamaños según jerarquía del PRD

## 📱 Responsive Breakpoints

- **Mobile**: < 640px
- **Tablet**: 640px - 1024px
- **Desktop**: > 1024px
- **Large Desktop**: > 1440px

## 🔧 Próximos Pasos

### Mejoras Sugeridas
1. Agregar imágenes reales en lugar de placeholders
2. Implementar formulario de registro funcional
3. Conectar con backend para cursos dinámicos
4. Agregar analytics (Google Analytics, Mixpanel)
5. Implementar A/B testing para CTAs
6. Agregar testimonios reales
7. Implementar sistema de reviews

### Optimizaciones
1. Minificar CSS y JS para producción
2. Optimizar imágenes (WebP, lazy loading)
3. Implementar service worker para PWA
4. Agregar meta tags para SEO
5. Implementar schema.org markup

## 📝 Notas

- Los estilos personalizados están en `css/styles.css`
- El JavaScript está en `js/main.js`
- Tailwind CSS se carga vía CDN (considera usar build process para producción)
- Todos los CTAs tienen tracking preparado en el código

## 🎨 Design System

Sigue el design system definido en el PRD:
- Colores primarios y secundarios
- Tipografía Inter
- Espaciado basado en 8px
- Componentes reutilizables (botones, cards, badges)
- Microinteracciones suaves

## 📄 Licencia

Este proyecto es parte de WebflowLATAM.

---

**Creado siguiendo el PRD v1.0**

