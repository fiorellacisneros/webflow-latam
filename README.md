# WebflowLATAM Platform

Plataforma integral para Webflow y Design as a Service en Latinoamérica.

## 📁 Estructura del Proyecto

```
.
├── academia-landing/          # Landing page del módulo Academia
│   ├── index.html
│   ├── css/
│   │   └── styles.css
│   ├── js/
│   │   └── main.js
│   ├── images/
│   └── assets/
├── vpmn-map.html             # Mapa de procesos VPMN interactivo
├── vercel.json               # Configuración de Vercel
├── package.json              # Dependencias y scripts
└── README.md                 # Este archivo
```

## 🚀 Deploy en Vercel

### Opción 1: Deploy desde CLI

1. **Instala Vercel CLI** (si no lo tienes):
   ```bash
   npm i -g vercel
   ```

2. **Login en Vercel**:
   ```bash
   vercel login
   ```

3. **Deploy**:
   ```bash
   vercel
   ```

4. **Deploy a producción**:
   ```bash
   vercel --prod
   ```

### Opción 2: Deploy desde GitHub

1. **Conecta tu repositorio** a Vercel:
   - Ve a [vercel.com](https://vercel.com)
   - Click en "New Project"
   - Importa tu repositorio de GitHub

2. **Configuración automática**:
   - Vercel detectará automáticamente que es un sitio estático
   - El archivo `vercel.json` configurará las rutas

3. **Deploy automático**:
   - Cada push a `main` desplegará automáticamente

## 📍 Rutas Disponibles

- `/` → Landing page de Academia
- `/academia` → Landing page de Academia (alias)
- `/vpmn` → Mapa de procesos VPMN

## ⚙️ Configuración

### vercel.json

El archivo `vercel.json` incluye:
- **Routes**: Configuración de rutas y rewrites
- **Headers**: Seguridad y cache headers
- **Builds**: Configuración de builds estáticos

### Optimizaciones Incluidas

- ✅ Cache headers para assets estáticos (CSS, JS, imágenes)
- ✅ Headers de seguridad (XSS, Frame Options, etc.)
- ✅ Rutas optimizadas
- ✅ Soporte para SPA routing

## 🔧 Desarrollo Local

### Con Vercel CLI

```bash
vercel dev
```

Esto iniciará un servidor local en `http://localhost:3000`

### Con servidor HTTP simple

```bash
# Python
python -m http.server 8000

# Node.js
npx http-server
```

## 📦 Assets y Recursos

- **CSS**: `/academia-landing/css/styles.css`
- **JavaScript**: `/academia-landing/js/main.js`
- **Imágenes**: `/academia-landing/images/`
- **Otros assets**: `/academia-landing/assets/`

## 🌐 Variables de Entorno (Opcional)

Si necesitas variables de entorno, crea un archivo `.env.local`:

```env
NEXT_PUBLIC_API_URL=https://api.webflowlatam.com
NEXT_PUBLIC_ANALYTICS_ID=your-analytics-id
```

Y agrega en `vercel.json`:
```json
{
  "env": {
    "NEXT_PUBLIC_API_URL": "@api_url"
  }
}
```

## 📊 Performance

El proyecto está optimizado para:
- ✅ Fast loading (CDN de Vercel)
- ✅ Cache de assets estáticos
- ✅ Headers de seguridad
- ✅ Optimización de imágenes (cuando se agreguen)

## 🔒 Seguridad

Headers de seguridad configurados:
- `X-Content-Type-Options: nosniff`
- `X-Frame-Options: DENY`
- `X-XSS-Protection: 1; mode=block`
- `Referrer-Policy: strict-origin-when-cross-origin`

## 📝 Notas

- El proyecto usa Tailwind CSS vía CDN (considera usar build process para producción)
- Las imágenes están en carpetas pero aún no hay imágenes reales
- El JavaScript es vanilla, sin dependencias

## 🆘 Troubleshooting

### Problema: Rutas no funcionan
- Verifica que `vercel.json` esté en la raíz
- Asegúrate de que las rutas en `vercel.json` coincidan con tu estructura

### Problema: Assets no cargan
- Verifica que los paths en HTML sean relativos correctos
- Revisa la consola del navegador para errores 404

### Problema: Deploy falla
- Verifica que no haya errores de sintaxis en `vercel.json`
- Revisa los logs de Vercel en el dashboard

---

**Listo para deploy en Vercel** ✅

