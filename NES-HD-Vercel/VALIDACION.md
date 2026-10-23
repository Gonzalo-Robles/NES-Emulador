# Validación realizada

- JavaScript: comprobación de sintaxis completada.
- Audio: prueba sintética de 440 Hz (resultado aproximado: 440,05 Hz), cinco canales, IRQ y conexión CPU/APU.
- Video: compilación y enlace de shaders en OpenGL ES, renderizado de los cinco filtros con framebuffer 1920×1080; proporciones 4:3, nativa y 16:9; selector 720p.
- Entrada: lectura serial de botones NES, pausa y continuación.
- Archivos: carga de una ROM sintética; ZIP almacenado y Deflate con README previo y ROM dentro de subcarpeta; rechazo de archivo inválido con mensaje.
- Sitio estático: HTTP 200 para /, index.html, portada, icono y configuración; referencias locales verificadas.
- Paquete ZIP: comprobación de integridad.

## Pendiente en el dispositivo de destino
No se pudo ejecutar una prueba completa en navegador real en este entorno. Las pruebas del JavaScript usan un DOM simulado; los shaders se probaron por separado con OpenGL ES. No se ha probado con una biblioteca de juegos comerciales, Safari/macOS ni un dispositivo táctil real. No se desplegó en Vercel ni se comprobó una URL de producción. Verificar después de desplegar: portada, carga de tu ROM, reproducción audible, controles y pantalla completa. No se garantiza compatibilidad con todas las ROM; consultar README.
