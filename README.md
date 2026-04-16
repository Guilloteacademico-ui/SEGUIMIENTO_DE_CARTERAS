# Portfolio Manager 📊

Aplicación web para gestionar carteras de inversión en acciones, con cotizaciones en tiempo real de Finnhub API.

## 🚀 Características

- ✅ **Gestión de múltiples clientes** con carteras independientes
- ✅ **Cotizaciones en tiempo real** vía Finnhub API
- ✅ **Cálculo automático de rendimiento** basado en precio de entrada
- ✅ **Historial de 30 días** con snapshots diarios
- ✅ **Auto-actualización configurable** (5min, 15min, 30min, 1h)
- ✅ **Indicador de mercado** (abierto/cerrado)
- ✅ **Dashboard consolidado** con métricas totales
- ✅ **PWA ready** - Funciona como app nativa en iOS/Android
- ✅ **Optimizado para móviles** - Diseño iOS-first
- ✅ **Persistencia local** - Datos guardados en localStorage

## 📱 Uso en iOS

1. Abre Safari en tu iPhone
2. Ve a: `https://tu-usuario.github.io/portfolio-manager/`
3. Toca el botón "Compartir" (icono cuadrado con flecha)
4. Selecciona "Añadir a pantalla de inicio"
5. ¡Listo! Ahora tienes una app nativa

## 🔧 Instalación Local

```bash
# Clonar repositorio
git clone https://github.com/tu-usuario/portfolio-manager.git

# Abrir con servidor local
cd portfolio-manager
python -m http.server 8000
# O simplemente abrir index.html en el navegador
```

## 📖 Cómo usar

### Agregar Cliente
1. Click en "Agregar Cliente"
2. Ingresa el nombre
3. Listo

### Agregar Inversión
1. Entra a un cliente
2. Click "Agregar Inversión"
3. Ingresa:
   - **Ticker** (ej: AAPL, GOOGL, MSFT)
   - **Capital invertido** en USD
   - **Fecha** de compra
4. El sistema captura automáticamente el precio actual como precio base

### Actualizar Cotizaciones
- **Manual**: Click en "🔄 Actualizar Cotizaciones"
- **Automático**: Activa el toggle "Auto" y selecciona intervalo

## 🧮 Cálculo de Rendimiento

```
% Rendimiento = (Precio Actual - Precio Base) / Precio Base × 100
Valor Actual = Capital × (1 + % Rendimiento / 100)
```

**Ejemplo:**
- Capital invertido: $1000
- Precio base: $100
- Precio actual: $110
- Rendimiento: +10%
- Valor actual: $1100

## 🕐 Horarios del Mercado

**NYSE/NASDAQ:**
- Apertura: 9:30 AM EST (13:30 UTC)
- Cierre: 4:00 PM EST (20:00 UTC)
- Días: Lunes a Viernes

## 🔐 API Key

Este proyecto usa la API de Finnhub. La clave está incluida en el código para simplicidad, pero es **solo para demo**.

Para uso en producción:
1. Obtén tu propia API key gratis en [finnhub.io](https://finnhub.io)
2. Reemplaza la clave en `index.html` línea ~440:
```javascript
const API_KEY = 'TU_API_KEY_AQUI';
```

## 📊 Stack Técnico

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **API**: Finnhub Stock API
- **Almacenamiento**: localStorage (navegador)
- **Hosting**: GitHub Pages
- **PWA**: Service Worker ready

## 🐛 Problemas Conocidos

- Los datos históricos se acumulan desde que agregas cada inversión (no se obtienen históricos previos)
- La API gratuita de Finnhub tiene límite de 60 llamadas/minuto

## 📝 Licencia

MIT License - Uso libre

## 👨‍💻 Autor

Creado con ❤️ para gestionar inversiones de forma simple y efectiva.

---

**¿Preguntas o sugerencias?** Abre un issue en GitHub.
