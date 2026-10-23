# NES HD — listo para Vercel

## Subir desde GitHub
1. Descomprimí este ZIP.
2. Subí el **contenido** de la carpeta al repositorio: `index.html`, `vercel.json` y `assets/` deben quedar en la raíz.
3. En Vercel: Add New → Project → importá tu repositorio.
4. Framework Preset: **Other**. Root Directory: la carpeta que contiene `index.html` (la raíz, si seguiste el paso 2).
5. Build Command e Install Command: sin comando. Output Directory: **.** (punto). El archivo `vercel.json` ya lo configura.
6. Deploy. Abrí la URL que entregue Vercel.

Si tu proyecto tenía antes configuraciones de otro framework, corregí esos campos antes de volver a desplegar. No selecciones `dist`, `build` ni `public`: este paquete no usa esas carpetas.

## Alternativa con terminal
Desde la carpeta que contiene index.html y vercel.json:
```sh
npx vercel
```
Seguí las instrucciones para iniciar sesión y crear el despliegue. No hay dependencias de npm ni compilación. Para producción, después de revisar el despliegue: `npx vercel --prod`.

## Probar en tu Mac
```sh
python3 -m http.server 8000
```
Abrí http://localhost:8000. También podés abrir index.html directamente. Mantené la carpeta assets junto al HTML para ver la imagen.

## Usar el emulador
- Cargar un juego: botón de portada, Cargar ROM o arrastrar un archivo.
- Teclado: flechas, Z=B, X=A, Enter=Start, Shift=Select, P=Pausa.
- Controles táctiles disponibles en pantallas con entrada táctil.
- Reiniciar conserva el juego cargado y reinicia la partida.
- Full HD 1920×1080, 720p o automático; 4:3 conserva la proporción. 16:9 estira la imagen.
- Cinco filtros de imagen y tres perfiles de audio; si no se escucha, pulsá Activar audio.
- Los ZIP deben contener una ROM .nes y usar almacenamiento sin compresión o Deflate, sin contraseña. Si el navegador no admite descompresión, extraé el .nes primero.
- Las ROM se procesan localmente: no se envían al servidor. No se incluyen juegos.

## Alcance real
Este es un emulador NES experimental de mapper 0 y 4, formato iNES y temporización NTSC. No es compatible con todos los juegos NES. No admite NES 2.0, PAL preciso, audio de expansión ni mirroring de cuatro pantallas. No implementa guardado persistente de partidas. Los filtros HD y perfiles 16/32 bits son efectos sobre gráficos/sonidos originales. No cambian los recursos del juego ni agregan gráficos 3D.

## Imagen de presentación
Ilustración generada para este proyecto con la herramienta de generación de imágenes integrada.
Prompt: control retro gris con cruceta negra y dos botones rojos sobre una plataforma arcade, iluminación roja y azul, fondo azul oscuro y espacio a la izquierda para el título, sin texto.
La imagen se incluye localmente en assets/presentacion.webp; no depende de un servidor de imágenes.
