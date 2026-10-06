# Evidencia y límites de los proyectos

Revisión del **6 de octubre de 2026**. Se compararon fuentes de las 35 entradas Android y 10 ediciones web/servicios; la cobertura funcional actual es parcial. La [matriz individual](REVIEW.md) distingue PASS concreto, parcial, fallo reproducido, bloqueado y no probado. Estos reconocimientos son editoriales por especialidad; no son premios externos ni una clasificación global de todas las apps funcionando.

## AXEL

**Fuente:** puentes Codex CLI/Grok/AGY, streaming, cancelación, trabajos y servicios de archivos/ADB. Búsqueda por nombre y tamaño no acredita reconocer personas en fotografías. Rutas declaradas de OCR, transcripción y generación requieren sus dependencias y permisos.

**Actual:** se consultaron servicios del S25 sin tocar su pantalla. Health respondió 200; una ruta esperada de capacidades respondió 404. Un servicio de capacidades respondió, pero sus valores declarados no demuestran ejecución; la consulta protegida respondió 401 sin credenciales. Hay que reconciliar el servicio en ejecución con la fuente antes de afirmar funcionamiento completo. Play Protect rechazó la copia Native en Pixel; no se eludió la comprobación.

**Pendiente:** comprobar conversación, enrutamiento a proveedor y herramienta con resultado verificable. No se hicieron generaciones de pago. Native, WebView, Portable y AXEL AI se conservan separados.

## AXEL Editor de vídeo

**Fuente:** modelo temporal, timeline, ripple, undo, almacenamiento atómico, keyframes y grafo Media3 de composición compartido. La comparación estática anterior registró paquete, versión, certificado documentado y 153 clases de producción coincidentes; no demuestra identidad binaria.

**Actual:** se copió el APK instalado en S25, se verificó SHA-256 y se instaló en un Pixel sin este paquete. Se creó un proyecto y abrió el editor con pistas V1/V2/A1/A2. Importar, editar y exportar no se han repetido en esta sesión. El nuevo nombre elegido por el autor se aplica a las fuentes y la presentación; el APK probado conserva su nombre anterior, Corte.

**Histórico:** ARCHITECTURE.md documenta 83 pruebas JVM y 20 instrumentadas, además de medidas de exportación. No se reejecutaron. Proxies, HDR, curvas de velocidad y algunos controles de procesamiento siguen pendientes. Una función no recibe PASS por aparecer en el timeline.

## ALEXIA

**Fuente:** Room, SAF, DocumentsProvider y recuperación de escrituras. **Actual:** apertura, proyecto y filtro de tipo en Pixel, sin alterar originales. Pixel tenía versionCode 63; S25, versionCode 68. No se presenta una prueba del Pixel como validación del APK del S25.

**Histórico:** informe de 63 pruebas unitarias y validación v68 de importación, hash, idempotencia, conservación del original y proveedor de documentos. Son evidencia previa, no resultados repetidos hoy. Importación y acceso entre aplicaciones actuales pendientes.

## NEXUS

**Actual Android:** catálogo guardado visible y aviso de recuperación de conexión. Esto prueba navegación del catálogo local, no disponibilidad de los modelos ni generación nueva.

**Revisión separada de escritorio:** captura real y verificaciones de navegación, conservación de prompt, importación local y rechazo de importaciones inválidas con datos de laboratorio. El informe de esa revisión registró 838 modelos, 85 trabajos y 84 resultados; son datos del estado revisado. No se hicieron llamadas de pago y el asistente figuró como no cargado durante esa comprobación.

## NutriShift

**Fuente:** menú contextual, turnos, despensa, lotes, caducidad y consumo reversible. **Actual:** APK copiado y verificado; flujo principal no repetido.

**Histórico:** XML con 42 pruebas JVM sin errores/fallos e informe de 28 pruebas Android en S25. La revisión visual completa de la 2.3 estaba pendiente en esos documentos. Las estimaciones nutricionales no son validación clínica.

## AudioTrim

**PASS actual limitado al WAV:** fixture sintético de 4 s, PCM mono de 16 bits y 48 kHz. Abrir → seleccionar → recortar → guardar por SAF → recuperar archivo. Exportación de 143.760 muestras, duración 2,995 s, PCM idéntico al tramo original.

- SHA-256 original: `45476dcdc32bf0aae2841292ee9b6d19b334ced9446d92544443716da600a28a`.
- SHA-256 exportación: `7cfb2c9095d1ed175cffc4de5e41ab3cad6d204d88bcc2513c1540dc0869d7fa`.

MP3, M4A y extracción de vídeo no validados en esta sesión. Recortar Audio es otra app y no hereda este PASS.

## Hallazgos en candidatas

- **AXEL Task:** la petición de un hueco de dos horas devolvió opciones de 30 minutos. Se reprodujo en el chat de la app. La instalación nueva contiene datos personales predefinidos, excluidos de capturas públicas.
- **AXEL Drobe:** tipo y color de una prenda fueron reconocidos, pero el nombre quedó en su primera letra. No se completó el flujo de conjuntos. Pixel API 37 mostró una advertencia de alineación de librerías de 16 KB.
- **ClipTree:** se creó y mostró un fragmento sintético en su carpeta. Copia al portapapeles y persistencia tras reiniciar pendientes. Su repositorio JSON no acredita un gestor seguro de contraseñas.
- **DisAster Web:** operaciones sobre registros de ejemplo, separadas de DisAster Android. No se atribuye gestión real del almacenamiento del teléfono a esa demo.
- **PhotoLayers:** ampliación por interpolación y enfoque en el código revisado; no superresolución neuronal.

## Alcance y límites

El Pixel quedó reservado después para otra compilación y pruebas de NEXUS; se respetó esa reserva y no se siguió operando su UI. Algunas funciones necesitan TV, robot, servicios autenticados o un entorno profesional que no se validaron aquí. Los tiempos de apertura y muestras aisladas de memoria no sirven para clasificar rendimiento sostenido.

La documentación conserva pendientes por app. Se mantienen privadas fuentes, credenciales, información profesional, datos personales, capturas y XML sin revisar. No se eliminó ningún original, se borraron datos de aplicaciones o se eludió Play Protect.
