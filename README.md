# Mi Mes 🌷

Primera versión funcional de una aplicación web para iPhone, diseñada para abrirse y editarse con PyCharm y Codex.

## Cómo abrirla

1. Descomprime el ZIP y abre la carpeta `mi_mes_app` en PyCharm.
2. Abre la terminal de PyCharm y ejecuta `python -m http.server 8000`.
3. En el navegador del ordenador entra en `http://localhost:8000`.
4. Los datos se guardan en **el navegador de ese dispositivo** mediante IndexedDB. El navegador de tu ordenador y Safari del iPhone **no comparten los datos**.

## Uso en iPhone

Para acceder desde tu iPhone e instalarla en la pantalla de inicio, necesitarás publicar el contenido en un sitio HTTPS (por ejemplo, GitHub Pages). En Safari, abre esa dirección y usa Compartir → Añadir a pantalla de inicio. No basta con abrir `localhost` del ordenador desde el iPhone. **No publiques tus archivos de copia de seguridad**: contienen información personal.

## Lo que funciona

- Diseño móvil vertical en español, con paletas pastel por mes.
- Crear y modificar presupuestos por categorías; la app marca en rojo importes que superan el total y desactiva Guardar.
- Anotar gastos personales y compartidos (porcentaje o importe manual).
- Registrar compras manuales, con productos individuales y selección de productos a contabilizar; se guarda el ticket completo como historial de productos.
- Consultar evolución por categorías, saldo, comparación de meses y previsión orientativa de gasto al terminar el mes.
- Buscar productos y ver los precios registrados en distintas compras.
- Historial de meses por años.
- Copia de seguridad JSON exportable e importable en Ajustes (el archivo se selecciona desde el dispositivo).
- Persistencia en IndexedDB, sin necesidad de crear una cuenta.

## Pendiente

- Lectura automática de fotografías de tickets (OCR). El botón se muestra como función prevista, no como función activa.
- Adjuntar fotos originales y reconocimiento fiable de descuentos, unidades y productos equivalentes.
- Publicación real, pruebas en Safari de iOS, iconos definitivos y mejoras de accesibilidad.
- Es una PWA, no una app nativa publicada en App Store.

## Copias de seguridad

Ve a **Ajustes → Exportar copia** y guarda el JSON en Archivos/iCloud Drive. Para restaurarlo, pulsa **Importar copia** y elige el archivo. **Importar sustituye todos los registros actuales**, por eso se pide confirmación. Haz copias frecuentes; el almacenamiento local puede perderse si se eliminan los datos de Safari, se desinstala o restablece el dispositivo, o se cambia de navegador/origen.

## Codex: próximo encargo sugerido

> Trabaja sobre este proyecto sin cambiar el diseño pastel ni la estructura de datos sin migración. Primero revisa validaciones y accesibilidad de la PWA en Safari para iPhone. Después implementa adjuntar imagen de ticket, OCR local y una pantalla de revisión antes de guardar productos. Conserva la opción de introducir y corregir productos manualmente. No envíes imágenes ni datos financieros a servicios externos sin consentimiento explícito.
