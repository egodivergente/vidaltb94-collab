# Proyectos que desarrollo

Trabajo en aplicaciones para crear, organizar y conectar herramientas con el entorno local. Aquí reúno seis proyectos por su aportación técnica y utilidad. [Catálogo](CATALOG.md) · [Estado y pruebas](VALIDATION.md) · [Evaluación individual](REVIEW.md).

## AXEL

**Agentes y herramientas locales · Android y Termux**

Diseñé AXEL para conversar con agentes y darles contexto útil de mi teléfono: archivos, herramientas Android y flujos multimedia. Integra puentes a Codex CLI, Grok y Antigravity/AGY, con streaming, cancelación y gestión de trabajos.

La aportación está en conectar conversación y acciones sobre el entorno local. Las rutas multimedia contemplan adjuntos, OCR, transcripción y referencias con proveedores configurados. Mantengo identificadas sus distintas ediciones: Native, Android/WebView, Portable y AXEL AI con servidor.

He revisado las fuentes y consultado los servicios activos. Hay diferencias entre rutas que debo reconciliar antes de dar por verificado todo el recorrido conversación → herramienta → resultado. [Pruebas y pendientes](VALIDATION.md#axel).

## AXEL Editor de vídeo

**Edición no destructiva · Android nativo · Multimedia**

Desarrollé un editor multipista con vídeo y audio vinculados, timeline, ripple, deshacer, autoguardado, keyframes, color, LUT y rótulos. Separé el modelo temporal, las operaciones de edición, el almacenamiento y la interfaz, y compartí el grafo Media3 entre previsualización y exportación.

Es uno de mis proyectos más exigentes por la coordinación de tiempo, pistas, estados y formatos. He comprobado en el Pixel la importación de un clip con audio, su exportación H.264 a 720p y la duplicación con deshacer de clips vinculados. Recuperé y decodifiqué el archivo exportado para verificar el resultado.

Elegí este nombre para el proyecto antes llamado Corte. Ya lo cambié en las fuentes del lanzador y del encabezado; la actualización instalada está pendiente de compilación y firma compatible. Algunas funciones avanzadas siguen en desarrollo. [Pruebas y límites](VALIDATION.md#axel-editor-de-vídeo).

## ALEXIA

**Biblioteca multimedia · Integridad · Interoperabilidad Android**

Creé ALEXIA para organizar imágenes, vídeos y audio por proyectos y mantenerlos accesibles desde otras aplicaciones. Uso Room, Storage Access Framework y DocumentsProvider, con el índice separado de los archivos originales.

La parte más delicada es conservar referencias válidas y recuperar escrituras interrumpidas. He comprobado apertura, navegación y filtrado en la revisión actual; conservo las pruebas anteriores de importación e integridad identificadas por versión. [Estado de validación](VALIDATION.md#alexia).

## NEXUS

**Creación con IA · Android y escritorio**

Desarrollo NEXUS para reunir modelos, opciones, referencias, trabajos y resultados de imagen, vídeo y audio. Los formularios se adaptan a las capacidades de cada modelo; en escritorio organizo el flujo en Crear, Biblioteca y Asistente.

![NEXUS: interfaz real de creación con datos de laboratorio](assets/nexus-create-lab.png)

*Interfaz de escritorio con datos de laboratorio. El resultado mostrado es material de prueba.*

Me interesa que elegir un modelo, preparar una creación y recuperar sus resultados formen un flujo continuo. La comprobación Android mostró el catálogo local mientras recuperaba conexión; las pruebas de escritorio están documentadas por separado. [Pruebas y pendientes](VALIDATION.md#nexus).

## NutriShift

**Planificación cotidiana · Menús y turnos · Android**

Desarrollé NutriShift para conectar mis horarios con menús, recetas, raciones preparadas, despensa, caducidad y compra. La lógica contempla consumo reversible, lotes y conservación de elecciones manuales.

He comprobado el menú semanal, el avance a la siguiente comida al marcarla como consumida, el alta de un producto y la presentación de un objetivo manual de 2100 kcal. Mantengo pendientes la comprobación actual de turnos con calendario y la reversión de existencias. [Estado de validación](VALIDATION.md#nutrishift).

## AudioTrim

**Recorte local de audio · Tratamiento de formatos**

Implementé rutas de recorte específicas para RIFF/WAV, MP3 y AAC. En WAV he comprobado el recorrido completo: abrir, seleccionar, recortar, guardar mediante el selector de Android y recuperar el archivo.

Los recortes conservan exactamente las muestras del tramo original, tanto en un WAV convencional como en otro con un chunk adicional. Los demás formatos mantienen sus pruebas actuales pendientes. [Resultados y hashes](VALIDATION.md#audiotrim).

## Más proyectos

También desarrollo AXEL Task, AXEL Drobe, CreatorVault, Despeja, PhotoLayers, PromptClip, ClipTree, AXEL Console y herramientas para TV. Documenté sus aportaciones, fallos reproducidos y siguientes pruebas en la [evaluación individual](REVIEW.md).

Las fuentes de estos productos se mantienen privadas; aquí explico sus decisiones de diseño, resultados y estado de desarrollo.
