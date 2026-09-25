# Landing ACONES (QR del stand)

## Antes de subir
1. Pon el video en `assets/bienvenida.mp4` (vertical 9:16).
   Comprímelo para que cargue rápido con datos móviles:
   ffmpeg -i original.mp4 -vf "scale=720:-2" -c:v libx264 -crf 26 -preset slow -c:a aac -b:a 128k -movflags +faststart assets/bienvenida.mp4
   (`+faststart` hace que empiece a reproducir antes de descargarse completo.)

## Probar local
npm install
npm start   # http://localhost:3000

## Railway
1. Sube esta carpeta a un repo de GitHub.
2. Railway → New Project → Deploy from GitHub repo.
3. Railway detecta Node y corre `npm start` (usa la variable PORT automáticamente).
4. Settings → Networking → Generate Domain (o Custom Domain, recomendado: p.ej. bienvenida.acones.org con un CNAME).
5. Genera el QR apuntando a ese dominio.
