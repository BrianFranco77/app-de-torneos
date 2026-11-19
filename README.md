# Torneo (ruleta + llave + podio)

Una sola base de código para **página web**, **app instalable (PWA)** y **app de tienda (Android / iOS)**.

## 1) Página web con URL
La carpeta `web/` es el sitio completo. Subila a cualquier hosting estático:
- **Netlify**: entrá a app.netlify.com/drop y arrastrá la carpeta `web`. Te da una URL al instante.
- **GitHub Pages**, **Vercel** o **Cloudflare Pages**: publicá el contenido de `web/`.
Necesita HTTPS (todos los de arriba lo tienen).

## 2) App instalable (PWA)
Al abrir la URL en el celular, el navegador ofrece instalarla:
- **Android (Chrome):** menú ⋮ → *Instalar app*.
- **iPhone (Safari):** Compartir → *Agregar a inicio*.
Funciona sin internet después de la primera carga.

## 3) App de tienda (Android / iOS) con Capacitor
Requisitos: Node.js 18+, y Android Studio (Android) o Xcode en Mac (iOS).
```
npm install
npm run android     # abre Android Studio -> Build > Build APK / Bundle
npm run ios         # abre Xcode (solo Mac)
```
Cuando cambies algo en `web/`, corré `npm run sync`.
Para subir a Play Store / App Store necesitás una cuenta de desarrollador de cada tienda.

## Cambiar nombre o paquete
`capacitor.config.json` (`appId`, `appName`) y `web/manifest.webmanifest`.
