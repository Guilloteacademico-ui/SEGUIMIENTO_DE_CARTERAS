# 🚀 Cómo subir a GitHub Pages

## Opción 1: Desde la terminal (recomendado)

```bash
# 1. Crear repositorio en GitHub
# Ve a https://github.com/new y crea un repo llamado "portfolio-manager"

# 2. Inicializar Git en tu carpeta
cd /ruta/a/tu/carpeta
git init

# 3. Agregar archivos
git add .

# 4. Hacer commit
git commit -m "Initial commit - Portfolio Manager v1.0"

# 5. Conectar con GitHub
git remote add origin https://github.com/TU-USUARIO/portfolio-manager.git

# 6. Subir código
git branch -M main
git push -u origin main

# 7. Activar GitHub Pages
# Ve a: Settings → Pages → Source: main branch → Save
```

## Opción 2: Desde la interfaz de GitHub

1. **Crear repositorio:**
   - Ve a https://github.com/new
   - Nombre: `portfolio-manager`
   - Público o Privado (tu eliges)
   - NO inicializar con README

2. **Subir archivos:**
   - Click en "uploading an existing file"
   - Arrastra estos archivos:
     - `index.html`
     - `manifest.json`
     - `README.md`
     - `.gitignore`
   - Click "Commit changes"

3. **Activar GitHub Pages:**
   - Settings → Pages
   - Source: Deploy from a branch
   - Branch: `main` → `/ (root)` → Save

4. **¡Listo!**
   - Tu app estará en: `https://TU-USUARIO.github.io/portfolio-manager/`
   - Espera 1-2 minutos para que se despliegue

## Actualizar después

```bash
# Hacer cambios en index.html

git add .
git commit -m "Update: descripción del cambio"
git push

# Los cambios se verán en 1-2 minutos
```

## Probar localmente antes de subir

```bash
# Python
python -m http.server 8000

# O Node.js
npx http-server

# Abrir: http://localhost:8000
```

## Notas importantes

- ✅ GitHub Pages es **GRATIS** para repos públicos
- ✅ Incluye **HTTPS** automático
- ✅ **Sin límites** de visitas
- ✅ Perfecto para **PWAs**
- ⚠️ La API key de Finnhub está en el código (considera variables de entorno para producción)
