# SeguraVenta - paquete instalable (PWA)

Es la misma app de siempre, empacada para que funcione de dos formas con un solo código:
1. Como página web, con su enlace y su QR.
2. Como aplicación instalada en el celular, con el ícono del escudo, a pantalla completa y con lo ya visitado disponible aunque falle la señal.

## Qué trae
- index.html: la app completa.
- manifest.webmanifest: nombre, colores e íconos para poder instalarla.
- sw.js: guarda la app para que abra aunque haya mala señal.
- icons/: el escudo en los tamaños que piden Android e iPhone.
- render.yaml: configuración opcional para Render.

## Cómo publicarla en Render (sitio estático, gratis)
1. Crea un repositorio nuevo en GitHub y sube todo el contenido de esta carpeta (los archivos, no la carpeta).
2. En Render: New + > Static Site > elige ese repositorio.
3. Build Command: déjalo vacío (o escribe: echo sin compilar). Publish Directory: . (un punto).
4. Crear el sitio. Render te da una dirección tipo https://seguraventa.onrender.com
5. Abre esa dirección en Chrome del celular y prueba.

(Si prefieres usar render.yaml, entra a Blueprints > New Blueprint Instance. Yo no lo probé en Render, así que si te marca error usa los pasos de arriba.)

## Cómo se instala como app
- Android (Chrome): menú de tres puntos > Instalar aplicación (o Agregar a pantalla principal).
- iPhone (Safari): botón Compartir > Agregar a pantalla de inicio.
- Computadora (Chrome o Edge): el ícono de instalar al final de la barra de direcciones.

## Importante
- Esta versión NO trae backend: los datos de la tienda se guardan en el navegador de cada dispositivo. Para que los pedidos lleguen de otros celulares, para las cuentas, las notificaciones al teléfono y el bot con Gemini hace falta el servidor, que es la siguiente etapa.
- No es un APK de Android. Para la burbuja que flota sobre otras apps se necesita una app Android nativa. Si más adelante quieres un APK, se puede generar a partir de esta misma página con un servicio como PWABuilder.
- El aviso de privacidad es una plantilla básica: revísala con un asesor legal antes de usarla con clientes reales.
