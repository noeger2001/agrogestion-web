# AgroGestión Web PWA 1.0.0

Aplicación web progresiva para administrar un negocio familiar agropecuario desde un celular Android.

## Qué incluye

- Dashboard con caja, cuentas por cobrar/pagar, inventario, préstamos, ventas y gastos.
- Terrenos y campañas agrícolas.
- Aplicaciones agrícolas y cosechas.
- Lotes avícolas.
- Compras, ventas e inventario por lotes.
- Clientes y proveedores.
- Trabajadores y jornales.
- Caja y cuentas financieras.
- Cuentas por cobrar y pagar.
- Préstamos.
- Reportes básicos.
- PIN local opcional.
- Respaldo y restauración mediante archivo JSON.
- Instalación como PWA en Android.
- Funcionamiento offline después de la primera carga.

## Arquitectura de esta versión

- Sitio estático: HTML, CSS y JavaScript, sin backend.
- Publicación: GitHub Pages.
- Datos: IndexedDB del navegador, con fallback a localStorage si IndexedDB no estuviera disponible.
- Offline: Service Worker y Cache API.
- Respaldo: archivo JSON descargable o compartible desde Android.

## Importante sobre los datos

GitHub Pages publica **solo el código de la aplicación**. Los registros del negocio no se guardan en GitHub: permanecen en el navegador del celular asociado a la URL exacta de la aplicación.

Haz respaldos frecuentes desde:

`Más → Respaldos → Descargar archivo`

No uses el modo incógnito. No borres los datos del sitio ni la caché de la aplicación sin haber creado antes un respaldo. Cambiar la URL, el nombre del repositorio o usar otro navegador crea un almacenamiento diferente.

## Instalación en Android

1. Publica el proyecto siguiendo `DEPLOYAR_EN_GITHUB.md`.
2. Abre la URL publicada desde Chrome en el celular.
3. Pulsa el botón **Instalar** de AgroGestión.
4. Si Chrome no muestra el aviso, abre el menú `⋮` y selecciona **Instalar aplicación** o **Agregar a pantalla principal**.
5. Abre AgroGestión una vez con Internet para que el Service Worker almacene los archivos necesarios.

## Estructura

```text
.
├── .nojekyll
├── index.html
├── manifest.webmanifest
├── sw.js
├── robots.txt
├── icons/
│   ├── icon-192.png
│   ├── icon-512.png
│   ├── maskable-512.png
│   └── apple-touch-icon.png
└── docs/
    └── vista-celular.png
```

## Limitaciones actuales

Esta es una versión web funcional del prototipo, no la implementación productiva completa planteada originalmente en Flutter/SQLite.

Todavía no incluye:

- fotografías o comprobantes;
- respaldo automático cifrado a Telegram;
- SQLite/Drift;
- exportación XLSX/PDF;
- sincronización entre varios celulares;
- contabilidad completa con costo de ventas y devengo.

El PIN local es una barrera de uso casual; no cifra la base de datos del navegador.

## Validaciones realizadas

- sintaxis JavaScript;
- carga en viewport móvil de 390 × 844;
- persistencia mediante IndexedDB;
- recarga completa conservando registros;
- funcionamiento offline tras instalar el Service Worker;
- descarga de respaldo JSON;
- manifiesto PWA e iconos;
- navegación principal del prototipo.
