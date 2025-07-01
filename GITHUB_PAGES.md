# 🌐 GitHub Pages - GS | Timer

## 📋 Configuración para GitHub Pages

Este repositorio está configurado para desplegarse automáticamente en GitHub Pages usando GitHub Actions.

### 🚀 URL de Deployment

Una vez configurado en GitHub, el complemento estará disponible en:
```
https://tu-usuario.github.io/gs-timer-onenote/
```

### 📁 Archivos de Configuración

- **`.github/workflows/deploy.yml`** - Workflow de GitHub Actions
- **`scripts/generate-manifest.js`** - Generador de manifest para producción
- **`config.json`** - Configuración de URLs para diferentes entornos

### ⚙️ Configuración en GitHub

1. **Ve a tu repositorio** en GitHub
2. **Settings** → **Pages**
3. **Source**: GitHub Actions
4. **El workflow se ejecutará automáticamente** en cada push a `main`/`master`

### 🔧 Scripts Disponibles

```bash
# Generar manifest para desarrollo (localhost)
npm run manifest:dev

# Generar manifest para producción (GitHub Pages)
npm run manifest:prod

# Construir para GitHub Pages
npm run build:pages

# Deploy completo
npm run deploy
```

### 📝 Personalización de URLs

Para cambiar las URLs, edita el archivo `config.json` o usa el script personalizado:

```bash
# Generar para usuario específico
node scripts/generate-manifest.js production tu-usuario-github nombre-repo
```

### 🎯 Usar el Complemento desde GitHub Pages

1. **Descarga el manifest** desde:
   ```
   https://tu-usuario.github.io/gs-timer-onenote/manifest.xml
   ```

2. **Haz sideload** en OneNote:
   - OneNote Online: **Insertar** → **Complementos** → **Cargar Mi Complemento** → **Subir Mi Complemento**
   - OneNote Windows: **Insertar** → **Mis Complementos** → **Cargar Mi Complemento**

### 🔒 Consideraciones de Seguridad

- GitHub Pages sirve archivos con HTTPS automáticamente
- Los certificates de desarrollo locales no son necesarios en producción
- El manifest de producción apunta a las URLs de GitHub Pages

### 🛠️ Troubleshooting

Si el deployment falla:

1. **Verifica** que GitHub Pages esté habilitado en el repositorio
2. **Revisa** el log del workflow en la pestaña "Actions"
3. **Asegúrate** de que el branch principal sea `main` o `master`
4. **Confirma** que el repositorio sea público (o tengas GitHub Pro para repos privados)

### 📊 Estado del Deployment

El workflow de GitHub Actions incluye:
- ✅ **Checkout** del código
- ✅ **Setup** de Node.js 18
- ✅ **Instalación** de dependencias
- ✅ **Build** del proyecto
- ✅ **Upload** a GitHub Pages
- ✅ **Deploy** automático

¡Tu complemento GS | Timer estará disponible mundialmente una vez configurado! 🌍
