Instrucciones para puesta en marcha
*** Frontend: React

Instalar dependencias:
npm install

Iniciar en desarrollo:
npm run dev

Construir para producción:
npm run build

Vista previa de producción:
npm run preview

*** Backend: Dash (Servidor Principal)

Instalar dependencias:
npm install

Iniciar en desarrollo:
npm run dev

Construir:
npx tsc

Nota:
Necesitas configurar las variables de entorno en un archivo .env con las siguientes claves:

DATABASE_URL

FRONTEND_URL

*** Backend: Local (Servidor Local para Hardware)

Instalar dependencias:
npm install

Iniciar:
npm run dev

Nota:
Este servidor requiere configurar las siguientes variables de entorno en un archivo .env:

PORT

FRONTEND_URL (Para la configuración de CORS)

Orden de inicio recomendado:

Iniciar Backend Dash:
El servidor principal con base de datos.

Iniciar Backend Local:
El servidor local para manejar el hardware.

Iniciar Frontend React:
La interfaz de usuario.

Variables de entorno necesarias:

backend_dash/.env:
DATABASE_URL=tu_url_de_mongodb
FRONTEND_URL=http://localhost:5173
PORT=4000

backend_local/.env:
FRONTEND_URL=http://localhost:5173
PORT=4040

frontend_react/.env:
VITE_API_URL=http://localhost:4000/api