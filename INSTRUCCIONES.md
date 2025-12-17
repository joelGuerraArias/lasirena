# 🔑 Configuración de API Keys - La Sirena

## ✅ Sistema de Configuración Actualizado

Las API keys se guardan **permanentemente** y persisten incluso cuando cierras y abres la aplicación.

### 🔄 Sistema de Persistencia:
1. **localStorage del navegador** (prioritario) - Se guarda automáticamente cuando ingresas keys por la UI
2. **config.json** (opcional) - Para configuración inicial en desarrollo

## 📝 Cómo Configurar tus API Keys

### Paso 1: Crear el archivo config.json

El archivo `config.json` ya existe en la raíz del proyecto. Solo necesitas editarlo:

```json
{
  "gemini_api_key": "TU_API_KEY_DE_GEMINI_AQUÍ",
  "wavespeed_api_key": "TU_API_KEY_DE_WAVESPEED_AQUÍ"
}
```

### Paso 2: Obtener las API Keys

#### Para Gemini (Google AI Studio):
1. Ve a: https://aistudio.google.com/app/apikey
2. Inicia sesión con tu cuenta de Google
3. Haz clic en "Create API Key"
4. Copia la clave (empieza con `AIza...`)
5. Pégala en `config.json` en el campo `gemini_api_key`

#### Para Wavespeed (SeeDream & Flux):
1. Ve a: https://wavespeed.ai
2. Crea una cuenta o inicia sesión
3. Ve a "API Keys" en tu dashboard
4. Copia tu clave (empieza con `ws_...`)
5. Pégala en `config.json` en el campo `wavespeed_api_key`

### Paso 3: Guardar y Usar

1. Guarda el archivo `config.json`
2. Recarga la aplicación en el navegador
3. ¡Listo! Las keys se cargarán automáticamente

## 🔒 Seguridad

- ✅ El archivo `config.json` está en `.gitignore` (no se sube a GitHub)
- ✅ Tus keys permanecen locales en tu computadora
- ✅ Nunca compartas tu `config.json` con nadie

## 🎯 Ejemplo de config.json completo

```json
{
  "gemini_api_key": "AIzaSyC1234567890abcdefghijklmnopqrst",
  "wavespeed_api_key": "ws_1a2b3c4d5e6f7g8h9i0j"
}
```

## 🆘 Método Recomendado: Usar la UI (Más Fácil)

**Este método guarda las keys PERMANENTEMENTE:**

1. Hacer clic en el botón rojo "Configure API Key" en el header de la app
2. Ingresar tu API key manualmente
3. Hacer clic en "Save API Key"
4. ✅ **Las keys se guardan en localStorage del navegador y persisten para siempre**

**Ventaja**: No necesitas editar archivos, las keys se guardan automáticamente.

**Nota**: Las keys guardadas por la UI tienen prioridad sobre config.json.

## 📂 Ubicación del Archivo

El archivo debe estar en:
```
la-sirena-clean/
├── config.json          ← Aquí (edita este)
├── config.example.json  ← Ejemplo (no edites)
├── App.tsx
├── package.json
└── ...
```

## ✨ Ventajas del Sistema

- ✅ **Persistencia automática** - Las keys se guardan para siempre en localStorage
- ✅ **No necesitas ingresar las keys cada vez** - Se cargan automáticamente
- ✅ **Fácil de actualizar** - Usa la UI para cambiar keys cuando quieras
- ✅ **Más seguro** - localStorage no se sube a GitHub
- ✅ **Funciona sin archivos** - No necesitas editar config.json si usas la UI

## 🔒 ¿Dónde se Guardan las Keys?

Cuando usas la UI para guardar las keys, se almacenan en **localStorage del navegador**:
- ✅ **Persisten para siempre** (no se borran al cerrar el navegador)
- ✅ **Solo en tu computadora** (no se envían a ningún servidor)
- ✅ **Específicas del dominio** (cada proyecto tiene sus propias keys)

Para borrar las keys, puedes:
1. Hacer clic en el botón verde "Gemini Connected" o "Wavespeed Connected"
2. O limpiar el localStorage del navegador

---

¿Necesitas ayuda? Revisa el README.md completo o contacta al desarrollador.
