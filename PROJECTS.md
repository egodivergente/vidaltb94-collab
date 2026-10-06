# Productos y decisiones de diseño

Esta selección presenta agentes conectados al teléfono, creación con IA, edición multimedia, almacenamiento Android y organización cotidiana. Los productos siguen en desarrollo. [Pruebas, fechas y límites](VALIDATION.md) · [Catálogo completo](CATALOG.md).

## AXEL

**01 · Agentes con acceso al entorno Android · Termux y app Android · Fuentes privadas**

AXEL conecta la conversación con el entorno del teléfono: agentes locales, archivos, herramientas multimedia y acciones sobre otras aplicaciones. Su propuesta es resolver una tarea que necesita contexto y ejecución, desde una misma interfaz.

Las fuentes conservan un puente que enruta **Codex CLI, Grok y Antigravity/AGY**, respuestas en streaming, cancelación y trabajos. Los servicios locales incluyen búsqueda e inspección de archivos, OCR, transcripción y acceso a Android mediante ADB. La app aporta conversaciones, adjuntos y flujos entre aplicaciones.

En multimedia, incorpora rutas para usar imágenes de referencia, generar mediante proveedores configurados y presentar o guardar los resultados. La disponibilidad depende del proveedor, los permisos y los puentes de cada entorno; una entrada de catálogo no prueba que toda la cadena esté operativa.

**Por qué encabeza la selección:** la integración entre agentes, sistema Android, archivos y herramientas propias es uno de los trabajos más singulares del ecosistema. Su valor está en coordinar esas capas para actuar sobre un contexto real. El repositorio Native conserva una evolución de la app; las ediciones WebView y Native se documentan por separado. [Evidencia y alcance](VALIDATION.md#axel).


## NEXUS

**02 · Estudio creativo · Android y escritorio · Fuente privada**

Crear con distintos modelos suele exigir cambiar de interfaz, reconstruir parámetros y buscar después los resultados. NEXUS reúne la elección del modelo, sus opciones, las referencias y la biblioteca en un mismo flujo.

El escritorio separa **Crear**, **Biblioteca** y **Asistente**. El catálogo adapta los formularios a las capacidades del modelo y conserva el seguimiento de trabajos. La aplicación Android usa Kotlin, Compose, WorkManager y Media3.

![NEXUS: interfaz de creación del escritorio con datos de laboratorio](assets/nexus-create-lab.png)

*Captura real de la interfaz del escritorio con datos de laboratorio, sin conexión ni generación de pago. El resultado mostrado es material de prueba.*

**Por qué está entre los destacados:** combina un producto amplio con una interfaz de escritorio revisada y un problema concreto de creación y gestión de resultados. La revisión disponible acredita navegación y flujos locales; la disponibilidad actual de cada proveedor necesita su propia comprobación. [Evidencia](VALIDATION.md#nexus).


## Corte

**03 · Editor de vídeo multipista · Android · Fuente privada**

Corte permite construir proyectos locales con vídeo y audio vinculados, editar un timeline y exportar la composición. Su arquitectura separa el modelo, las operaciones de edición y el almacenamiento de la interfaz.

La implementación incluye edición ripple, deshacer, autoguardado, keyframes, color, LUT y rótulos. Comparte el grafo de composición entre previsualización y exportación mediante Media3.

**Por qué está entre los destacados:** muestra profundidad técnica en edición y exportación multimedia. La fuente se contrastó estáticamente con la instalación y existen pruebas históricas documentadas. Varias interacciones de fase 2 y funciones de procesamiento aún requieren completar su validación o implementación. [Evidencia](VALIDATION.md#corte).


## ALEXIA

**04 · Biblioteca creativa por proyectos · Android · Fuente privada**

ALEXIA organiza imágenes, vídeos y audio por proyectos y conecta su índice con el almacenamiento de Android. Su trabajo central es conservar referencias utilizables a los archivos y hacerlos accesibles desde otras herramientas.

Usa Kotlin, Room, Storage Access Framework y DocumentsProvider. La arquitectura distingue el índice de la biblioteca del almacenamiento de los originales y contempla la recuperación de escrituras interrumpidas.

**Por qué está entre los destacados:** aporta profundidad en integridad e interoperabilidad Android. La evidencia disponible incluye pruebas históricas con archivos y hashes; las variantes recuperadas e instaladas necesitan su reconciliación correspondiente. [Evidencia](VALIDATION.md#alexia).


## NutriShift

**05 · Comidas adaptadas a turnos · Android · Fuente privada**

Planificar comidas resulta difícil cuando cambian los horarios y la despensa. NutriShift conecta el menú con los turnos, las recetas, las raciones preparadas, las existencias y la lista de compra.

La lógica conserva recetas versionadas y registra el consumo de forma reversible. Contempla lotes, caducidad, congelación y preparación de varias raciones. Las consultas a ChatGPT se copian y revisan manualmente antes de incorporar propuestas.

**Por qué está entre los destacados:** ofrece utilidad cotidiana y flujos respaldados por informes de lógica y dispositivo. Se han revisado capturas e informes existentes; la revisión visual completa de la versión 2.3 seguía pendiente en esa documentación. [Evidencia](VALIDATION.md#nutrishift).


## Otros proyectos

| Producto | Qué aporta | Estado de la evaluación |
| :--- | :--- | :--- |
| **AXEL Task** | Agenda, tareas, interpretación de texto y conflictos de horario. | Fuentes recuperadas; pruebas históricas de lógica. Experiencia actual por comparar. |
| **AXEL Drobe** | Prendas, conjuntos, planificación y lavandería con reglas locales. | Fuentes recuperadas; pruebas históricas de sugerencias. Experiencia actual por comparar. |
| **ClipTree** | Fragmentos de texto en carpetas, portapapeles y burbuja flotante. | Fuentes recuperadas; validación actual pendiente. |
| **AXEL TV** | Mando móvil, widget y comunicación con Android TV. | Evidencia histórica del mando; variantes TV por reconciliar. |
| **AXEL Music** | Audio local, cola y listas en móvil y TV. | Interfaz y código revisados; reproducción persistente en segundo plano pendiente. |
| **DisAster** | Organización de archivos en Android y variantes web. | Android 3.7.3 reconstruido y recompilado desde APK; fuente nativa original y evaluación funcional pendientes. |

Los repositorios de fuentes privadas conservan su acceso restringido. Las herramientas internas y los archivos históricos están en el [catálogo](CATALOG.md); la selección editorial no convierte una recuperación de código en una entrega validada.
