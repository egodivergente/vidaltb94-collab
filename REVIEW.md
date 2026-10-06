# Evaluación de aplicaciones · 6 de octubre de 2026

La revisión comprende las **35 entradas Android identificadas**, incluidos complementos y prototipos, y **10 ediciones web o de servicios**. Se localizaron las 57 copias de fuente del inventario. Tener fuente, instalar un APK y completar su flujo principal son comprobaciones distintas.

**Cobertura funcional actual parcial:** se interactuó con ALEXIA, NEXUS, AXEL Editor de vídeo (APK identificado como Corte), AXELTask, AXELDrobe, AudioTrim y ClipTree en Pixel físico API 37. También se consultaron servicios AXEL del S25 sin operar su pantalla. Solo se atribuye PASS al flujo concreto verificado. Las pruebas históricas se mantienen identificadas como históricas. No se ha determinado una ganadora global de funcionamiento entre todas las apps.

## Cómo se valora

- **Dificultad técnica:** problemas propios resueltos, persistencia e integridad, concurrencia, formatos, permisos, integración entre componentes y recuperación ante errores. Cantidad de archivos, librerías empaquetadas y uso de un SDK no equivalen a ingeniería propia.
- **Utilidad y singularidad:** problema concreto, ahorro de pasos y relación con el resto del ecosistema. Un acompañante se valora dentro de su conjunto.
- **Funcionamiento:** entrada real, acción, resultado comprobable y fallos reproducidos. Una pantalla que abre, una capability declarada o un servicio health no acreditan todo el producto.
- **Experiencia y madurez:** claridad de flujos, estado de conexión, permisos, datos de ejemplo y límites de distribución. La opinión visual no sustituye exportaciones o integridad.

Las etiquetas de dificultad son cualitativas; no son medidas del esfuerzo histórico del autor. Las limitaciones de prueba no implican que la app falle. La evaluación funcional seguirá pendiente donde falten dispositivo objetivo, puente, permisos acotados o ejecución del flujo.

## Reconocimientos por lo observado

| Área | Proyecto | Motivo y alcance |
| --- | --- | --- |
| Integración de agentes | **AXEL** | Puentes Codex/Grok/AGY, trabajos y herramientas Android/archivos. Reconocimiento de arquitectura; el servicio activo necesita reconciliación y prueba completa. |
| Ingeniería multimedia | **AXEL Editor de vídeo** | Modelo temporal, edición no destructiva y grafo de composición compartido. Reconocimiento de implementación; la exportación actual sigue pendiente. |
| Integridad e interoperabilidad | **ALEXIA** | Room, SAF y DocumentsProvider con recuperación de escrituras. Apertura/filtro actuales e integridad histórica documentada. |
| Producto creativo | **NEXUS** | Catálogo, formularios, trabajos y biblioteca en Android/escritorio. Catálogo local observado; disponibilidad de proveedores por comprobar. |
| Utilidad cotidiana | **NutriShift** | Turnos, despensa, lotes, compra y consumo reversible. Lógica revisada y pruebas históricas; flujo actual pendiente. |
| Precisión en un flujo local | **AudioTrim** | Recorte WAV real con PCM idéntico al tramo original, recuperado y verificado. Reconocimiento limitado a ese formato/flujo. |

Estos reconocimientos orientan la presentación por especialidad. No son un orden de calidad global ni premios externos.

## Todas las entradas Android

| Aplicación | Aporte y dificultad | Resultado actual | Siguiente comprobación |
| --- | --- | --- | --- |
| **AKI** | Chat Android mediante WebView y puente local. **Baja–media**: Interfaz web, render de mensajes y puente Java/JavaScript; la mayor complejidad depende del servidor externo. | NO PROBADO: APK instalado en Pixel; conversación no ejecutada. | Comprobar puente, streaming y errores de conexión. |
| **Aki Chat** | Cliente Compose del puente de conversación. **Baja–media**: Cliente de chat y estado local; no equivale al motor de agentes. | NO PROBADO: APK histórico firmado disponible. | Verificar salud real del puente: la etiqueta de conexión no la acredita. |
| **ALEXIA** | Biblioteca multimedia por proyectos e interoperabilidad Android. **Alta**: Room, SAF, DocumentsProvider y recuperación de escrituras; integridad y compatibilidad entre aplicaciones. | PARCIAL: apertura, proyecto y filtro de tipo comprobados en Pixel; no se importaron nuevos originales. | Repetir importación sintética, hash, idempotencia y apertura desde otra app. |
| **Antigravity launcher (personal wrapper)** | Acceso personal a una sesión de Termux. **Baja**: Una actividad delega al RunCommand de Termux y al script; complejidad principal fuera del APK. | NO PROBADO: no se lanzó para evitar interrumpir el ejecutor de compilación. | Comprobar script y sesión cuando Termux esté libre; abre Termux en primer plano. |
| **AudioTrim** | Recorte local de audio y extracción de pistas. **Media–alta**: Parser RIFF/WAV propio, alineación de muestras, tratamiento MP3/AAC y rutas de remux/reencode. | PASS WAV: abrir, seleccionar, recortar y guardar; PCM exportado idéntico al tramo del original. | Validar MP3, M4A y audio de vídeo; este PASS no se extiende a esos formatos. |
| **AXEL AI** | Chat Android con agente persistente alojado en servidor. **Alta**: Cliente Android y servidor Python con trabajos persistentes, herramientas acotadas y proveedor Bedrock. | NO PROBADO: APK actual copiado al Pixel; no se efectuaron consultas al modelo. | Comprobar autenticación, estado de trabajos y recuperación; llamada al modelo con alcance autorizado. |
| **AXEL Android (ai.axel.app)** | Edición WebView del ecosistema local AXEL. **Alta en el conjunto; cliente por separar**: Interfaz, servicios y archivos recuperados de una evolución de agentes; no confundir con Native ni con AXEL AI. | NO PROBADO: APK firmado histórico 1.0.0 recuperado; no acredita la última edición descrita. | Reconciliar versión, puente actual y capacidades multimedia. |
| **AXEL Browse** | Navegación Android TV con control desde móvil. **Media–alta**: WebView para TV, cursor, protocolo de recepción y emparejamiento con token temporal. | NO PROBADO en TV: APK firmado instalado en Pixel para revisión, sin TV disponible en la sesión. | Probar navegación, emparejamiento, caducidad y transferencia con TV real. |
| **AXEL Console** | Terminal Android y cliente de ejecución local. **Media–alta inferida de reconstrucción**: Buffer y parser ANSI/CSI, redimensionado, streaming y peticiones autenticadas con HMAC; no es solo un lanzador. | NO PROBADO: reconstrucción y APK disponibles, sesión CLI no ejecutada. | Recuperar proyecto nativo y contrastar terminal, resize, desconexión y autenticación. |
| **AXEL Link** | Acompañante móvil de AXEL Browse. **Media**: Emparejamiento y envío de enlaces; aporta valor junto al receptor TV. | NO PROBADO: aplicación presente en Pixel, sin receptor TV probado. | Probar junto a Browse; evitar presentarlo como otro navegador completo. |
| **AXEL Media TV** | Reproducción multimedia para TV. **Media**: Cliente y controles de reproducción; compatibilidad del dispositivo es parte del producto. | BLOQUEADO en Pixel API 37: Play Protect rechazó este APK antiguo. | Validar en TV compatible; el rechazo en Pixel no demuestra fallo en TV. |
| **AXEL Native** | Agentes Codex, Grok y AGY conectados a herramientas y Android. **Alta**: Enrutamiento de proveedores, streaming, cancelación, trabajos y servicios MCP de archivos/ADB; dependencias entre componentes. | PARCIAL de servicios: health respondió, ruta de capacidades esperada dio 404 y consulta protegida dio 401 sin token. APK rechazado por Play Protect en Pixel. | Reconciliar servicio activo con fuente y probar conversación → herramienta → resultado con permisos adecuados. |
| **AXEL Stream** | Servicio HTTP para archivos y medios locales. **Media**: Servicio en primer plano y streaming de archivos; no es captura de pantalla. | NO PROBADO: APK instalado; servidor y acceso amplio a archivos no activados para la auditoría. | Servir solo un archivo sintético y comprobar autenticación, rangos y cierre. |
| **AXEL TV** | Experiencia Android TV con ambiente, biblioteca y recepción. **Media–alta**: Ciclo TV, transferencia, fondos y comunicación con acompañantes móviles. | NO PROBADO en el dispositivo objetivo. | Reconciliar variantes y probar funciones con TV real. |
| **AXELDROBE** | Armario, conjuntos, planificación y lavandería. **Media–alta**: Reglas locales de color/estilo, prendas disponibles, rotación e historial; generador de combinaciones propio. | FAIL de UX: frase reconoció camiseta y verde, pero el nombre quedó reducido a la primera letra. Advertencia 16 KB en Pixel API 37. | Corregir autocompletado; guardar prendas sintéticas y validar conjunto y lavandería. |
| **AxelMusic** | Biblioteca, cola y listas de audio local. **Media–alta**: MediaStore, cola, listas e importaciones; recorte AAC/M4A y operaciones de archivos. | NO PROBADO: APK firmado instalado; reproducción no ejecutada. | Reproducir fixture, cambiar cola y verificar continuidad; fuente vincula reproducción a actividad. |
| **AxelMusic TV** | Edición TV de la biblioteca musical. **Media**: Interfaz TV y reproducción; edición separada de la móvil. | BLOQUEADO en Pixel API 37 por Play Protect. | Probar en TV y comprobar relación real con móvil. |
| **AXELTask** | Agenda, tareas, calendario y conflictos de horario. **Alta**: Motores de planificación, texto natural, calendario, conflictos y servicio local; complejidad de dominio real. | FAIL: «Busca un hueco de dos horas para auditar apps» devolvió huecos de 30 min. La instalación nueva contiene datos personales predefinidos. | Unificar parser usado por UI; retirar datos personales de una distribución y repetir calendario/conflictos. |
| **AXELWORK** | Organización local de turnos y notas profesionales. **Media–alta**: Room, flujos offline, reglas de registros y protección de captura; transcripción depende de servicio local. | NO PROBADO: APK histórico firmado recuperado; no se utilizaron datos profesionales reales. | Validar CRUD sintético y disponibilidad de transcripción sin información real. |
| **AxShell** | Diseño de secuencias y generación de comandos. **Media**: Validación de parámetros/entorno, escaping y pasos delicados; el editor genera scripts. | NO PROBADO: instalación presente en Pixel, sin ejecución de secuencias. | Verificar salidas y escaping; no atribuir ejecución solo por generar un script. |
| **CineVault 48** | Galería temporal por proyectos. **Media–alta**: Política de retención, papelera, persistencia y mantenimiento programado. | NO PROBADO: APK instalado; no se concedió acceso a toda la galería para evitar políticas sobre archivos ajenos. | Probar retención y recuperación con proyecto sintético aislado. |
| **Cliptree** | Fragmentos jerárquicos y portapapeles. **Media**: Árbol de carpetas, repositorio JSON local, búsqueda, copia y acceso flotante. | PARCIAL: carpeta abierta y clip sintético creado y mostrado; copia/persistencia tras reinicio no comprobadas. | Comprobar copia y lectura persistente; JSON local no acredita bóveda de contraseñas. |
| **AXEL Editor de vídeo** | Editor de vídeo local multipista. **Alta**: Modelo temporal racional, ripple, undo, keyframes, almacenamiento atómico y composición Media3 compartida para preview/export. | PARCIAL: APK actual de S25 probado en Pixel; se creó proyecto y abrió editor V1/V2/A1/A2. Exportación actual no repetida. | Importar clips sintéticos, editar, exportar y medir duración, vídeo y audio. |
| **CreatorVault** | Biblioteca creativa por sesiones y proyectos. **Alta**: Room, copia atómica con hash, idempotencia, clustering y DocumentsProvider. | NO PROBADO: APK instalado sin modificar archivos de trabajo. | Importar fixture y comprobar nombres repetidos, hash, selector y recuperación. |
| **Despeja** | Captura de ideas y pendientes con clasificación y planificación. **Media–alta inferida de reconstrucción**: Classifier local, Room y puente que recibe planes y los aplica a identificadores existentes; evaluación desde Smali. | NO PROBADO: APK actual copiado al Pixel; no se ejecutó captura ni plan. | Probar captura, clasificación, completar y aplicar un plan; recuperar proyecto Kotlin original. |
| **DisAster / Clasificador de Fotos** | Organización de archivos en Android. **Media–alta inferida de reconstrucción**: WebView y puente Android de MediaStore/archivos; recursos y Smali de instalación recuperados. | NO PROBADO: APK instalado; no se movieron ni borraron archivos. | Clasificar un fixture y verificar ruta/hash; separar operación real de la simulación web. |
| **Dr. Axel** | Diagnóstico y mantenimiento del ecosistema local. **Media–alta**: Cliente Android y guardian con supervisión, retención y estados de proveedores. | NO PROBADO: APK firmado disponible; no se ejecutaron reparaciones ni reinicios. | Probar diagnóstico en entorno aislado; tests que reimplementan funciones no prueban producción. |
| **Keyframe Sorter** | Clasificación de imágenes y fotogramas en Android. **Media**: Categorías y operaciones sobre MediaStore; permisos y confirmación de movimientos. | NO PROBADO: APK instalado; archivos personales intactos. | Mover solo un fixture y verificar; limpiar nombres personales predefinidos. |
| **Mando AXEL** | Mando móvil y widget de Android TV. **Media–alta**: Cliente nativo, widget, protocolo de control y puente TV/ADB. | NO PROBADO en TV; controles físicos no ejecutados. | Probar conexión y UI sin confundir móvil y TV. |
| **NEXUS** | Estudio de creación con IA en Android y escritorio. **Alta**: Catálogo, formularios según capacidades, trabajos persistentes, referencias y biblioteca de resultados. | PARCIAL: Android mostró catálogo guardado y estado de recuperación de conexión. No se hizo generación de pago. | Verificar formularios y trabajo completo por proveedor; distinguir catálogo cacheado de disponibilidad. |
| **NutriShift** | Menús adaptados a turnos, despensa y preparación. **Alta**: Planificación contextual, lotes, caducidad, consumo reversible y conservación de elecciones manuales. | NO PROBADO de nuevo: APK actual copiado al Pixel; se conserva evidencia histórica separada. | Generar menú sintético y comprobar despensa, compra y consumo reversible. |
| **PhotoLayers Studio** | Edición de imágenes por capas y máscaras. **Media–alta**: Capas, composición, máscaras y segmentación de SDK; ampliación por interpolación y enfoque. | NO PROBADO: APK instalado; exportación no ejecutada. | Exportar composición sintética; la ampliación implementada no es superresolución neuronal. |
| **PromptClip** | Copia de prompts de respuestas visibles. **Media–alta**: Árbol de accesibilidad acotado, estabilización finita, selección y deduplicación por hash; evita leer campos de entrada. | NO PROBADO: APK actual copiado al Pixel; accesibilidad no habilitada durante la auditoría. | Probar con fixture visible, streaming, exclusión de entradas y copia. |
| **Recortar Audio** | Recorte, escucha y exportación de audio. **Media**: Compose y motor de recorte; ruta WAV presupone cabecera canónica de 44 bytes. | NO PROBADO: APK firmado instalado; recorte actual no ejecutado. | Probar WAV canónico y RIFF con chunks extra; límite inferido de código, no fallo reproducido. |
| **S25 Files** | Gestión de archivos y herramientas Android por MCP. **Alta**: MCP, SAF/archivos, duplicados, archivo/papelera, seguridad y protección de biblioteca ALEXIA. | NO PROBADO: APK instalado sin activar operaciones de gestión. | Consultar salud/listado acotado y autenticación antes de operaciones de escritura. |

## Ediciones web y servicios

| Proyecto | Implementación revisada | Funcionamiento actual |
| --- | --- | --- |
| **amazon-medical-portal** · Portal documental profesional | Flask, sesiones, registro de operaciones, formularios y persistencia. | Fuente revisada; no se usaron registros profesionales reales ni servidor de trabajo. |
| **axel-osint** · Investigación local de fuentes abiertas | Scope, redacción, almacenamiento, colectores y pipeline de casos; la UI no acredita todos los adaptadores. | Fuente revisada; investigación nueva y colectores no ejecutados. |
| **axel-portable** · Archivo del entorno AXEL/Codex UI | Runtime Codex/Grok, streaming, archivos y rutas multimedia locales; gran archivo con dependencias incluidas. | Fuente revisada; servicio actual completo no probado. No premiar tamaño de dependencias. |
| **derivacion-sns** · Formulario y registro de derivaciones | Cache/outbox y llamadas de registro; depende del backend compartido. | Fuente revisada; integración con portal actual no probada. |
| **derivamad4** · Formularios y sincronización documental | Registro, archivos, sincronización y PeerJS; separar UI y backend. | Fuente revisada; flujo profesional real no ejecutado. |
| **disaster-web** · Prototipo web de organización de medios | Estado React con archivos de ejemplo; clasificar y borrar cambia registros de ejemplo. Backend contempla respuesta mock. | PROTOTIPO: no acredita mover archivos Android ni descarga real de Drive. |
| **dreame** · Integración de robot mediante MCP y aplicación de escritorio | Cliente cloud, mapas, herramientas MCP y frontend Tauri; requiere cuenta y dispositivo compatibles. | Fuente revisada; no se controló ningún robot ni se validó sesión actual. |
| **farmatools-ronda** · Extensión que prepara una hoja de turno | Extracción del DOM de un portal concreto y consolidación; depende del entorno real. | Fuente revisada; integración con portal laboral no probada en esta auditoría. |
| **noelia-vidal-pwa** · PWA personal de recuerdos y medios | Carga local, IndexedDB y service worker; código y contenido personal deben distinguirse. | Fuente revisada; no se publicó material personal ni se probó despliegue actual. |
| **noelia-vidal-claude** · Otra edición del proyecto personal de recuerdos | UI React/Next y persistencia según edición; relación con la PWA por conservar. | Fuente revisada; no se probó despliegue actual ni se fusionaron variantes. |

## Resultados que cambian la presentación

AXELTask no recibe una posición principal por ambición solamente: el flujo de chat devuelve 30 minutos cuando se piden dos horas. Su versión de prueba también contiene datos personales predefinidos; esos valores no se reproducen aquí. AXELDrobe reconoce tipo y color, pero su autocompletado deja el nombre en una letra. Ambos fallos deben resolverse antes de presentarlos como flujos maduros.

DisAster Android y DisAster Web son ediciones distintas. La web cambia registros de demostración; no acredita operaciones sobre archivos reales. PhotoLayers implementa ampliación por interpolación y enfoque, no superresolución neuronal. AXEL Stream sirve medios/archivos; no se ha encontrado una implementación de captura de pantalla en la edición revisada.

AXEL Console conserva parser ANSI, terminal y cliente autenticado: merece evaluarse por esa ingeniería y no relegarse por llamarse Console. Despeja conserva clasificación de ideas/pendientes y planes; no es un limpiador de archivos. ClipTree es un organizador local de fragmentos; su JSON no acredita una bóveda segura de contraseñas.

El rechazo de algunos APKs antiguos por Play Protect en Pixel API 37 es un límite de esta sesión, no una prueba de fallo en su Android TV objetivo. El rendimiento no se clasifica con una sola apertura ni una captura aislada de memoria.

## Recorte WAV verificado

Fixture sintético de 4 segundos, 48 kHz, mono PCM de 16 bits. Se abrió en AudioTrim, se desplazó el inicio, se guardó por el selector Android y se recuperó el archivo exportado. El resultado tiene 143.760 muestras y dura 2,995 segundos; sus bytes PCM coinciden exactamente con la selección del original.

- SHA-256 del WAV original: `45476dcdc32bf0aae2841292ee9b6d19b334ced9446d92544443716da600a28a`.
- SHA-256 del WAV exportado: `7cfb2c9095d1ed175cffc4de5e41ab3cad6d204d88bcc2513c1540dc0869d7fa`.

No se repitieron MP3, M4A ni extracción de vídeo. Las capturas y registros con información privada no forman parte de esta página.

## Nombres y coherencia

AXEL es el producto de agentes y sus ediciones se identifican por separado: Android/WebView, Native, archivo Portable y AXEL AI con servidor. AXEL Task y AXEL Drobe se escriben de forma consistente en la presentación. AudioTrim y Recortar Audio siguen siendo apps distintas. El autor eligió **AXEL Editor de vídeo** para el editor antes llamado Corte. El nombre del lanzador y el encabezado usan un recurso único en las fuentes; el paquete y el repositorio Corte conservan su identidad. La actualización del APK instalado todavía no se ha realizado.

AXEL Control, el selector de compilaciones, Salón y las reservas históricas son infraestructura o inventario sin suficiente fuente funcional en este lote; no compiten como apps terminadas. No se eliminaron repositorios ni se publicaron fuentes privadas.
