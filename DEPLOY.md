# 🚀 Guía de Deploy en Vercel

## Opción 1: Deploy desde CLI (Recomendado)

### Paso 1: Instalar Vercel CLI

```bash
npm i -g vercel
```

### Paso 2: Login

```bash
vercel login
```

### Paso 3: Deploy

Desde la raíz del proyecto:

```bash
cd /Users/fiorellacisneros/Documents/demo
vercel
```

Sigue las instrucciones:
- ¿Set up and deploy? → **Y**
- ¿Which scope? → Selecciona tu cuenta
- ¿Link to existing project? → **N** (primera vez) o **Y** (si ya existe)
- ¿Project name? → `webflowlatam` (o el nombre que prefieras)
- ¿Directory? → **.** (punto, raíz del proyecto)

### Paso 4: Deploy a Producción

```bash
vercel --prod
```

## Opción 2: Deploy desde GitHub (Recomendado para CI/CD)

### Paso 1: Sube el código a GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/tu-usuario/webflowlatam.git
git push -u origin main
```

### Paso 2: Conecta con Vercel

1. Ve a [vercel.com](https://vercel.com)
2. Click en **"New Project"**
3. Importa tu repositorio de GitHub
4. Vercel detectará automáticamente la configuración

### Paso 3: Configuración Automática

Vercel usará automáticamente:
- ✅ `vercel.json` para rutas y configuración
- ✅ Deploy automático en cada push a `main`
- ✅ Preview deployments en PRs

## 📍 URLs después del Deploy

Después del deploy, tendrás:

- **Producción**: `https://tu-proyecto.vercel.app/`
- **Academia**: `https://tu-proyecto.vercel.app/academia`
- **VPMN Map**: `https://tu-proyecto.vercel.app/vpmn`

## ✅ Verificación Post-Deploy

1. **Verifica la landing page principal**:
   - Debe cargar en `/`
   - Los estilos CSS deben funcionar
   - El JavaScript debe ejecutarse

2. **Verifica los assets**:
   - CSS: `/academia-landing/css/styles.css`
   - JS: `/academia-landing/js/main.js`

3. **Verifica el mapa VPMN**:
   - Debe cargar en `/vpmn`
   - Los diagramas deben renderizarse

## 🔧 Troubleshooting

### Problema: "Cannot find module"

**Solución**: Vercel no necesita `node_modules` para sitios estáticos. Asegúrate de que `package.json` no tenga dependencias requeridas en runtime.

### Problema: Assets 404

**Solución**: Verifica que los paths en `index.html` sean relativos correctos:
- ✅ `href="css/styles.css"` (correcto)
- ❌ `href="/css/styles.css"` (puede fallar)

### Problema: Rutas no funcionan

**Solución**: Verifica `vercel.json`. Las rutas deben apuntar a archivos existentes.

### Problema: Deploy lento

**Solución**: Normal en primera vez. Los siguientes deploys son más rápidos gracias al cache.

## 📊 Monitoreo

Después del deploy, puedes:

1. **Ver logs**: Dashboard de Vercel → Deployments → Logs
2. **Ver analytics**: Dashboard → Analytics (si está habilitado)
3. **Ver performance**: Dashboard → Speed Insights

## 🔄 Actualizaciones

Para actualizar el sitio:

```bash
# Hacer cambios en los archivos
git add .
git commit -m "Update landing page"
git push
```

Vercel desplegará automáticamente si está conectado a GitHub.

O manualmente:

```bash
vercel --prod
```

## 🎯 Optimizaciones Incluidas

El proyecto ya incluye:

- ✅ Headers de seguridad
- ✅ Cache para assets estáticos
- ✅ Rutas optimizadas
- ✅ Configuración de Vercel lista

## 📝 Notas Importantes

1. **Tailwind CDN**: Actualmente usa CDN. Para producción, considera usar Tailwind CLI para optimizar el CSS.

2. **Imágenes**: Cuando agregues imágenes reales, optimízalas antes de subirlas (WebP, compresión).

3. **Dominio personalizado**: Puedes agregar un dominio personalizado desde el dashboard de Vercel.

---

**¡Listo para deploy!** 🚀

