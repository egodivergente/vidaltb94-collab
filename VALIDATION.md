# Qué he comprobado

Actualizado el **6 de octubre de 2026**. He revisado fuentes de 35 entradas Android y 10 ediciones web/servicios. He probado flujos concretos de 10 aplicaciones en el Pixel; la [tabla individual](REVIEW.md) muestra qué funciona, qué falla y qué sigue pendiente.

## AXEL

Revisé los puentes Codex CLI/Grok/AGY, streaming, cancelación, trabajos y servicios de archivos/ADB. Consulté servicios del S25: health respondió 200, una ruta esperada de capacidades respondió 404 y una consulta protegida respondió 401 sin credenciales. Los valores de capacidades declarados no demuestran su ejecución.

Me falta reconciliar el servicio activo con las fuentes y repetir conversación → proveedor → herramienta → resultado. Play Protect rechazó la copia Native en el Pixel. No hice generaciones de pago. La búsqueda de archivos por nombre y tamaño tampoco acredita reconocimiento de personas en fotos.

## AXEL Editor de vídeo

**Comprobado en Pixel con el APK del S25 anterior al cambio de nombre:** crear proyecto, importar vídeo con audio, exportar H.264 720p/30 fps mediante SAF, recuperar y decodificar el archivo completo. Resultado: seis segundos de vídeo, 180 fotogramas y audio con el tono de 440 Hz conservado. El contenedor dura 6,03 s por el audio/codificación.

También comprobé duplicación de la pareja vídeo/audio y deshacer leyendo el proyecto guardado: dos parejas a 0 y 6 s, y una pareja después de deshacer.

- SHA-256 de entrada: `0185fbc25c0e1bb4084ed3e785d60c517fe7a18edf2a881ec83ae490a08b1bc8`.
- SHA-256 de exportación: `938cba510bf0aff8c33356f7e85140e0e3ca16da12c95c98a89bac580220a01c`.

La fuente de prueba no declara matriz de color y la exportación declara BT.709. Los tres fotogramas muestreados coinciden al interpretar ambos explícitamente como BT.709; no he validado toda la gestión de color ni otros reproductores.

Conservo como históricas las 83 pruebas JVM y 20 instrumentadas documentadas. No las reejecuté. Ripple, keyframes, transiciones, otros formatos y funciones avanzadas mantienen validaciones pendientes. El nuevo nombre está en las fuentes; el APK probado todavía se presenta como Corte.

## ALEXIA

Comprobé apertura, proyecto y filtro de tipo sin alterar originales. El Pixel usa versionCode 63 y el S25 tenía versionCode 68: no son la misma versión.

Conservo el informe anterior de 63 pruebas unitarias y la validación v68 de importación, hash, idempotencia y proveedor de documentos. Importación e interoperabilidad de las versiones actuales siguen pendientes.

## NEXUS

Android mostró catálogo guardado y recuperación de conexión. Eso valida navegación local, no la disponibilidad actual de los proveedores.

La revisión separada de escritorio incluye navegación, conservación de prompt, importación local y rechazo de entradas inválidas con datos de laboratorio. Su informe registra 838 modelos, 85 trabajos y 84 resultados del estado revisado; no hice llamadas de pago en esta auditoría.

## NutriShift

Comprobé menú semanal, avance tras marcar una comida, alta de un producto sintético en despensa y objetivo manual de 2100 kcal visible como activo. Denegué acceso al calendario privado en la copia de prueba.

Me falta repetir consumo/reversión de existencias, persistencia del objetivo y turnos con calendario sintético. Las 42 pruebas JVM y 28 Android documentadas son anteriores. Las estimaciones nutricionales no son validación clínica.

## AudioTrim

**WAV convencional:** entrada de cuatro segundos, PCM mono de 16 bits y 48 kHz. El recorte recuperado tiene 143.760 muestras, dura 2,995 s y coincide exactamente con el tramo original.

- Entrada: `45476dcdc32bf0aae2841292ee9b6d19b334ced9446d92544443716da600a28a`.
- Salida: `7cfb2c9095d1ed175cffc4de5e41ab3cad6d204d88bcc2513c1540dc0869d7fa`.

**WAV con chunk JUNK adicional:** reconocido y recortado; 147.168 muestras, 3,066 s y PCM exacto. Salida: `60ca29fba765959175acbe5ccf101701faf4b12af1cc6b8d1b7ee9bff9f39f74`.

MP3, M4A y extracción de vídeo siguen pendientes en esta revisión.

## Otros resultados

- **AXEL Task:** pedir un hueco de dos horas devuelve opciones de 30 minutos. La instalación nueva también contiene datos personales predefinidos que debo retirar antes de distribuirla.
- **AXEL Drobe:** guardar dos prendas, proponer un conjunto, vestirlo, separar colada y devolver prendas lavadas a disponibles funcionó. Corregí manualmente los nombres para continuar: el autocompletado deja solo la primera letra. El Pixel API 37 también advierte de alineación de librerías de 16 KB.
- **ClipTree:** creé un fragmento, comprobé su escritura JSON, lo copié y pegué en la búsqueda: un resultado coincidente. Reinicio y overlay pendientes. El almacenamiento revisado es local y sin cifrado.
- **Despeja:** capturé una nota, se clasificó en Comprar y la marqué como despejada. Deshacer, persistencia y planificación pendientes.
- **Recortar Audio:** el WAV convencional conserva el PCM tras recortarlo, pero el tipo MIME y la extensión M4A no corresponden al contenido WAV. Un WAV válido con chunk JUNK adicional falla con «divide by zero» y deja un archivo vacío.
- **DisAster Web:** trabaja con registros de ejemplo; mantengo separada la evaluación de DisAster Android sobre archivos reales.
- **PhotoLayers:** el código revisado amplía por interpolación y enfoque; no implementa superresolución neuronal.

## Alcance

Algunas pruebas necesitan TV, robot, servicios autenticados o un entorno profesional. Mantengo esos pendientes en la tabla. No clasifico rendimiento sostenido con una sola apertura o una muestra de memoria.

Conservo privadas las fuentes, credenciales, datos personales y capturas sin revisar. Las pruebas de escritura aquí descritas usan copias de auditoría y contenido sintético.
