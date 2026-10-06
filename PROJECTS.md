# Productos y decisiones de diseño

Seis casos muestran aportaciones distintas del ecosistema. La selección considera implementación propia, utilidad, singularidad y evidencia. [Evaluación de 35 entradas Android y 10 ediciones web/servicios](REVIEW.md) · [Pruebas y límites](VALIDATION.md).

## AXEL

**Integración de agentes · Android y Termux · Fuentes privadas**

AXEL conecta conversación, contexto del teléfono y herramientas: agentes, archivos, acciones Android y flujos multimedia desde una interfaz propia. El trabajo de integración incluye enrutamiento a Codex CLI, Grok y Antigravity/AGY, streaming, cancelación y trabajos; los servicios incluyen archivos y consultas ADB.

Las rutas multimedia permiten adjuntos, OCR, transcripción y uso de referencias con proveedores configurados. La edición Native, la antigua WebView, el archivo Portable y AXEL AI con servidor tienen identidades y dependencias distintas.

**Aportación destacada:** coordinar agentes y herramientas para actuar sobre contexto local. La revisión actual encontró diferencias entre el servicio activo y las rutas del código recuperado; completar conversación → herramienta → resultado sigue pendiente. [Evidencia](VALIDATION.md#axel).

## AXEL Editor de vídeo

**Ingeniería multimedia · Android nativo · Fuentes privadas**

Editor local multipista con vídeo y audio vinculados, timeline, ripple, deshacer, autoguardado, keyframes, color, LUT y rótulos. La arquitectura separa modelo, operaciones temporales, almacenamiento e interfaz y comparte el grafo Media3 entre previsualización y exportación.

**Aportación destacada:** modelo temporal propio, edición no destructiva y composición coherente entre reproducción y archivo exportado. Su dificultad procede de coordinar tiempo, pistas, estados y formatos. En la revisión actual se creó un proyecto y se abrió el editor; existen pruebas históricas de lógica y exportaciones, sin atribuirlas a una nueva validación completa.

El autor eligió este nombre el 6 de octubre. El proyecto antes se presentaba como Corte; conserva paquete y repositorio. El recurso del lanzador y el encabezado ya se han cambiado en las fuentes. La actualización instalada está pendiente. Varias funciones de fase 2 siguen pendientes de completar o validar. [Evidencia](VALIDATION.md#axel-editor-de-vídeo).

## ALEXIA

**Integridad e interoperabilidad · Android · Fuentes privadas**

ALEXIA organiza imágenes, vídeos y audio por proyectos y conecta su índice con el almacenamiento de Android. Usa Room, Storage Access Framework y DocumentsProvider, separando el índice de los archivos originales.

**Aportación destacada:** conservar referencias útiles entre aplicaciones y recuperar escrituras interrumpidas. La revisión actual comprobó apertura, navegación y filtrado; la integridad completa se apoya en pruebas históricas identificadas. Las versiones de Pixel y S25 son diferentes. [Evidencia](VALIDATION.md#alexia).

## NEXUS

**Producto creativo · Android y escritorio · Fuentes privadas**

NEXUS reúne modelos, opciones, referencias, trabajos y resultados de imagen, vídeo y audio. Los formularios se adaptan a las capacidades del modelo; el escritorio organiza Crear, Biblioteca y Asistente.

![NEXUS: interfaz real de creación con datos de laboratorio](assets/nexus-create-lab.png)

*Captura real de escritorio con datos de laboratorio, sin conexión ni generación de pago. El resultado mostrado es material de prueba.*

**Aportación destacada:** continuidad del flujo desde elegir un modelo hasta gestionar sus resultados. Android mostró el catálogo guardado mientras recuperaba conexión; este estado no acredita la disponibilidad de todos los proveedores. [Evidencia](VALIDATION.md#nexus).

## NutriShift

**Utilidad cotidiana · Android · Fuentes privadas**

NutriShift conecta menús y turnos con recetas, raciones preparadas, despensa, caducidad y compra. La lógica contempla consumo reversible, lotes y conservación de elecciones manuales.

**Aportación destacada:** adaptar planificación y existencias a horarios que cambian. Se ha revisado la lógica y la evidencia histórica; el flujo principal de la instalación actual todavía no se ha repetido. Las consultas a ChatGPT siguen siendo manuales y revisables. [Evidencia](VALIDATION.md#nutrishift).

## AudioTrim

**Precisión de una herramienta local · Android · Fuentes privadas**

AudioTrim abre medios y recorta audio mediante rutas específicas para formatos. La implementación incluye tratamiento propio de RIFF/WAV y otras estrategias para MP3/AAC.

**Aportación destacada en esta sesión:** abrió un WAV sintético, recortó la selección y guardó el resultado por el selector Android. El archivo recuperado tiene PCM idéntico al tramo original. Es un resultado comprobado de principio a fin; los otros formatos conservan su validación pendiente. [Evidencia y hashes](VALIDATION.md#audiotrim).

## Candidatas y herramientas

AXEL Task y AXEL Drobe muestran lógica de dominio considerable, con fallos actuales documentados antes de promoverlas. CreatorVault, Despeja, PhotoLayers, PromptClip, ClipTree y AXEL Console merecen evaluación de sus flujos completos. Las herramientas TV necesitan su dispositivo objetivo.

[Catálogo](CATALOG.md) · [Resultados individuales y pendientes](REVIEW.md). Las fuentes privadas mantienen su acceso restringido.
