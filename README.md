# Contador de Dinero — Compilar APK en GitHub

## Estructura
- `www/index.html` → tu app (sin tocar)
- `assets/icon.png` → ícono generado (1024x1024)
- `assets/splash.png` → splash generado (2732x2732)
- `capacitor.config.json` → configuración de la app (appId: com.jose.contador)
- `.github/workflows/build-apk.yml` → compila el APK automáticamente

## Pasos desde el celular

1. **Crear el repositorio**
   - Entra a github.com → botón `+` → "New repository"
   - Ponle un nombre, por ejemplo: `contador-de-dinero`
   - Público o privado, como prefieras → "Create repository"

2. **Subir estos archivos**
   - En la página del repo recién creado, toca "uploading an existing file"
   - Sube TODOS los archivos y carpetas de este paquete manteniendo la estructura (`www/`, `assets/`, `.github/workflows/`, y los archivos sueltos)
   - Si GitHub no te deja arrastrar carpetas completas: sube primero `www/index.html`, luego `assets/icon.png` y `assets/splash.png`, luego crea el archivo `.github/workflows/build-apk.yml` con "Create new file" pegando la ruta completa en el nombre (GitHub crea las carpetas solas)
   - Haz commit directo a `main`

3. **Verificar que se dispare la compilación**
   - Ve a la pestaña "Actions" del repo
   - Debe aparecer "Build APK" corriendo (tarda 3-6 minutos)
   - Si no arrancó solo: Actions → "Build APK" → "Run workflow"

4. **Descargar el APK**
   - Cuando termine (ícono verde ✔), entra a esa ejecución
   - Baja hasta "Artifacts" → descarga `contador-de-dinero-apk`
   - Es un .zip con el `app-debug.apk` — descomprímelo e instálalo en tu Android

## Notas
- El ícono y el splash se generaron a partir de la foto del billete que enviaste.
- Si cambias el ícono, reemplaza `assets/icon.png` (1024x1024) y `assets/splash.png` (2732x2732) y vuelve a subir.
