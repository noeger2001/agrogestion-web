# Publicar AgroGestión gratis en GitHub Pages

## Opción recomendada: desde la interfaz de GitHub

### 1. Descomprimir

Descomprime `AgroGestion-Web-PWA-1.0.0.zip` en tu computadora.

No subas el ZIP como un único archivo: debes subir el contenido descomprimido.

### 2. Crear el repositorio

1. En GitHub, pulsa **New repository**.
2. Nombre sugerido: `agrogestion-web`.
3. Selecciona **Public**. En GitHub Free, GitHub Pages se publica gratuitamente desde repositorios públicos.
4. Pulsa **Create repository**.

### 3. Subir los archivos

1. Dentro del repositorio, pulsa **Add file → Upload files**.
2. Arrastra todos los archivos y carpetas del proyecto a la raíz del repositorio:
   - `index.html`
   - `manifest.webmanifest`
   - `sw.js`
   - `.nojekyll`
   - `robots.txt`
   - `icons`
   - `docs`
   - los demás archivos de documentación
3. Pulsa **Commit changes**.

### 4. Activar GitHub Pages

1. Abre **Settings** del repositorio.
2. En el menú lateral, abre **Pages**.
3. En **Build and deployment**, selecciona:
   - **Source:** `Deploy from a branch`
   - **Branch:** `main`
   - **Folder:** `/ (root)`
4. Pulsa **Save**.

La dirección tendrá esta forma:

```text
https://TU_USUARIO.github.io/agrogestion-web/
```

Si el repositorio tiene otro nombre, reemplaza `agrogestion-web` por ese nombre.

### 5. Abrir e instalar en el celular

1. Abre la URL desde Chrome para Android.
2. Pulsa **Instalar** dentro de AgroGestión.
3. Si no aparece el aviso, abre `⋮` y selecciona **Instalar aplicación** o **Agregar a pantalla principal**.
4. Abre la aplicación una vez con conexión.
5. Después prueba activar el modo avión y volver a abrirla.

## Actualizar la aplicación

Cuando recibas una versión nueva:

1. Sustituye los archivos del repositorio por los nuevos.
2. Haz un nuevo commit.
3. Vuelve a abrir AgroGestión con Internet.
4. Cierra y abre la aplicación para que el Service Worker active la nueva versión.

Antes de actualizar, descarga un respaldo JSON.

## Seguridad

- Nunca subas al repositorio respaldos JSON con datos reales.
- Nunca agregues tokens de Telegram, contraseñas o claves privadas al código.
- En un repositorio público cualquiera puede ver el código, aunque no puede ver los datos almacenados localmente en tu celular.
- Mantén activado HTTPS en GitHub Pages.

## Alternativa con comandos Git

```bash
git init
git add .
git commit -m "Publicar AgroGestión Web PWA 1.0.0"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/agrogestion-web.git
git push -u origin main
```

Después activa GitHub Pages desde **Settings → Pages** como se explica arriba.
