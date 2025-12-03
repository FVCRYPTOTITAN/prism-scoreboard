INSTRUCCIONES V2 - Marcador TV para PRISM Live (cronómetro integrado y control por postMessage)

Archivos incluidos:
- overlay.html   -> Página del overlay con cronómetro integrado y soporte para comandos postMessage (start/pause/reset/set).
- controller.html -> Panel para generar rápidamente la URL editable, abrir el overlay y controlarlo en tiempo real con botones Start/Pause/Reset/Set.
- README.txt -> Este archivo.

Cómo usar (rápido):
1. Hospeda ambos archivos (overlay.html y controller.html) en el mismo sitio (GitHub Pages, Netlify, Vercel).
2. Abre controller.html desde tu móvil. Ajusta iniciales, goles y tiempo.
3. Haz clic en "Generar URL para PRISM" y copia la URL resultante.
4. En PRISM Live: Add -> Web -> pega la URL (ejemplo: https://TU-USUARIO.github.io/prism-scoreboard/overlay.html?teamA=AAA&teamB=BBB&scoreA=0&scoreB=0&time=00:00).
5. Si quieres controlar el marcador desde el mismo móvil: pulsa "Abrir Overlay" (se abrirá en otra pestaña) y usa Start/Pause/Reset/Set. Los comandos llegan al overlay abierto por el controlador mediante postMessage.
6. Nota importante sobre PRISM: Si cargas la URL directamente en la app PRISM, el overlay se mostrará correctamente pero PRISM no recibirá postMessage desde este controlador (porque PRISM carga la página en una WebView separada). Para control remoto que funcione con PRISM sin abrir el overlay desde el controlador, necesitarás una solución con backend (Firebase/Google Sheets) para sincronizar el estado. Puedo ayudarte a montar esa versión si la necesitas.

Formato del tiempo: MM:SS (ej: 45:00, 90:00, 00:30).

Si quieres, subo estos archivos a tu repositorio de GitHub (si me das el usuario) y lo dejo listo en GitHub Pages.
