# SeguraVenta Backend

Backend en Node.js + Express + `@google/genai` optimizado para ahorrar tokens y llamadas a Gemini sin perder inteligencia comercial.

## Caracteristicas clave
- **Modelo economico por defecto:** `gemini-3.1-flash-lite-preview` (con escalado opcional a `gemini-3.6-flash` en cierres dificiles).
- **Respuestas rapidas sin IA:** Horarios, ubicacion, envios y preguntas frecuentes definidas por la tienda responden al instante con costo $0.
- **Memoria corta:** Recorta el historial automaticamente para no inflar tokens en cada turno.
- **Limite por sesion:** Evita consumo excesivo por bucles o spam.
- **Control de intensidad, habilidades e interruptores:** Respeta `intensity` (0-100), `skills` y `switches`.

## Como desplegar en Render (Web Service)
1. Sube el contenido de esta carpeta a un repositorio en GitHub.
2. En Render: **New + -> Web Service** y conecta el repositorio.
3. **Build Command:** `npm install`
4. **Start Command:** `npm start`
5. En **Environment Variables**, agrega `GEMINI_API_KEY` con tu clave de Google AI Studio.
