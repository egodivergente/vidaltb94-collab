# Pruebas y pendientes

Resultados del 6 de octubre de 2026. Las pruebas de esta revisión usaron el Pixel y contenido de prueba. La revisión de fuentes cubre 35 entradas Android y 10 ediciones web o servicios; se probaron recorridos concretos de 10 apps.

## AXEL

Se consultaron los servicios del S25 sin manejar su pantalla. Health respondió; una ruta de capacidades devolvió 404 y una consulta protegida, 401 sin credenciales. Hay que reconciliar las rutas antes de probar conversación, proveedor, herramienta y resultado. Native no pudo instalarse en el Pixel por Play Protect.

Las capacidades declaradas y el código de una herramienta no demuestran que el servicio esté disponible. No se hicieron generaciones de pago ni pruebas de reconocimiento de personas en fotos.

## AXEL Editor de vídeo

Pasaron crear proyecto, importar un clip con audio, exportar por SAF y recuperar el resultado. La salida H.264 tiene 1280 × 720, 30 fps y 180 fotogramas; se decodifica completa y conserva el tono de audio de 440 Hz. El contenedor dura 6,03 s.

También pasaron duplicar la pareja vídeo/audio y deshacer: el proyecto guardado pasó de una a dos parejas a 0 y 6 s, y volvió a una.

- Entrada: `0185fbc25c0e1bb4084ed3e785d60c517fe7a18edf2a881ec83ae490a08b1bc8`.
- Exportación: `938cba510bf0aff8c33356f7e85140e0e3ca16da12c95c98a89bac580220a01c`.

El fixture es un clip uniforme de seis segundos. No cubre todos los efectos, formatos ni gestión de color. La fuente no declara matriz y la exportación declara BT.709: los tres fotogramas muestreados coinciden al interpretar ambas como BT.709.

El APK probado todavía se llama Corte. Las 83 pruebas JVM y 20 instrumentadas documentadas son anteriores; no se repitieron aquí.

## ALEXIA

Pasaron apertura, navegación de proyecto y filtro por tipo. Pixel usaba versionCode 63 y S25, 68. Las pruebas anteriores de importación, hash, idempotencia y DocumentsProvider pertenecen a sus versiones documentadas.

Queda repetir importación e interoperabilidad en las versiones actuales.

## NEXUS

Android mostró el catálogo guardado mientras recuperaba la conexión. La revisión separada de escritorio comprobó navegación e importación local con datos de laboratorio.

Estos resultados no prueban disponibilidad, tarifas ni generaciones de todos los proveedores. No se hicieron llamadas de pago.

## NutriShift

Se comprobaron menú semanal, avance al marcar una comida, alta de un producto y objetivo manual de 2100 kcal visible. El calendario privado no se autorizó en la copia de prueba.

Falta verificar consumo/reversión de existencias, persistencia del objetivo y turnos con un calendario sintético. Las 42 pruebas JVM y 28 Android documentadas son anteriores.

## AudioTrim

Se recortaron dos WAV de 48 kHz, mono y 16 bits, y se recuperaron los archivos. El PCM coincide exactamente con el tramo seleccionado.

| Entrada | Muestras de salida | Duración |
| --- | --- | --- |
| WAV convencional | 143.760 | 2,995 s |
| WAV con chunk JUNK adicional | 147.168 | 3,066 s |

SHA-256 del primer recorte: `7cfb2c9095d1ed175cffc4de5e41ab3cad6d204d88bcc2513c1540dc0869d7fa`. Del segundo: `60ca29fba765959175acbe5ccf101701faf4b12af1cc6b8d1b7ee9bff9f39f74`.

MP3, M4A y extracción de vídeo siguen pendientes de repetir.

## Otras apps

- **AXEL Drobe:** ciclo de guardar dos prendas, proponer conjunto, vestir y lavar comprobado. El nombre automático retiene solo la primera letra; se corrigió a mano para seguir. Android API 37 advierte de alineación de librerías de 16 KB.
- **ClipTree:** crear fragmento, comprobar escritura JSON, copiar, pegar y buscar pasó. Reinicio y overlay pendientes.
- **Despeja:** captura, clasificación en Comprar y completar pasó. Deshacer, persistencia y planificación pendientes.
- **AXEL Task:** al pedir dos horas, el chat devuelve huecos de treinta minutos. La instalación nueva también incluye datos personales predefinidos.
- **Recortar Audio:** conserva el PCM del WAV convencional, pero usa nombre/tipo M4A. Un WAV válido con chunk adicional falla con «divide by zero» y deja un archivo vacío.

[Revisión individual](REVIEW.md). Las pruebas de TV, robot y entorno profesional requieren sus equipos y accesos. No se publican datos personales ni capturas sin revisar.
