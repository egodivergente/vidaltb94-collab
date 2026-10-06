# Proyectos seleccionados

Cuatro productos encabezan este portafolio por la combinación de utilidad, diseño, profundidad y evidencia disponible. La revisión del **6 de octubre de 2026** compara documentación, fuentes accesibles, capturas reales e informes existentes; no es una nueva prueba completa de todas las aplicaciones.

[Volver al perfil](https://github.com/vidaltb94-collab)

## NEXUS

**01 · Creación con IA · Android y escritorio · Fuentes privadas**

Un estudio para elegir modelos, introducir parámetros, aportar referencias y gestionar resultados de imagen, vídeo y audio.

**Por qué encabeza la selección:** combina el mayor alcance de producto de las candidatas revisadas con una interfaz de escritorio coherente y una arquitectura que adapta los formularios a las capacidades de cada modelo.

- **Diseño:** creación, biblioteca y asistente separados en tres destinos; actividad y resultados cerca del flujo de creación.
- **Implementación:** catálogo de modelos, formularios dinámicos, seguimiento de trabajos y reproducción multimedia. Android usa Kotlin, Compose, WorkManager y Media3; el escritorio tiene su propia interfaz.
- **Evidencia revisada:** capturas reales de la revisión de escritorio del 6 de octubre, verificaciones de navegación, conservación del prompt, importación local y rechazo de importaciones inválidas. El informe de la instalación registró 838 modelos, 85 trabajos y 84 resultados, sin modificar el estado ni las credenciales.
- **Límite:** las comprobaciones de esa revisión no realizaron llamadas de pago. La captura de laboratorio utiliza material de prueba; no acredita una generación nueva ni el funcionamiento actual de cada proveedor. El informe también registró el asistente como no cargado durante esa comprobación.

## NutriShift

**02 · Organización cotidiana · Android · Fuentes privadas**

Conecta la planificación de comidas con turnos, recetas, raciones, despensa y compra. Su utilidad está en reducir decisiones y aprovechar lo que ya hay disponible.

**Por qué ocupa el segundo puesto:** tiene el lenguaje visual más definido de las capturas móviles comparadas y flujos cotidianos respaldados por pruebas de lógica y del dispositivo.

- **Diseño:** inicio con una acción principal, vista semanal y acceso directo a despensa y compra; identidad visual consistente.
- **Implementación:** lotes, caducidad, congelación, raciones, consumo reversible y recetas versionadas para conservar el historial.
- **Evidencia revisada:** captura real de la versión 2.2 y fuentes e informes de la 2.3. Los XML registran **42 pruebas JVM sin errores ni fallos**; el informe Android registra **28 pruebas superadas en el S25**.
- **Límite:** la revisión visual completa de la versión 2.3 seguía pendiente en la documentación consultada. El intercambio con ChatGPT es manual y revisable; no se presenta como una integración automática. Las estimaciones nutricionales no son una validación clínica.

## Corte

**03 · Edición de vídeo · Android nativo · Fuentes privadas**

Un editor multipista con proyectos locales, vídeo y audio vinculados, edición ripple, deshacer, autoguardado, keyframes, corrección de color, LUT y rótulos. Comparte la composición entre la previsualización y la exportación.

**Por qué entra en los destacados:** tiene una arquitectura de edición propia y un alcance multimedia considerable, con pruebas documentadas sobre las matemáticas del timeline y sobre los archivos exportados. Amplía la presentación más allá de las herramientas con IA.

- **Implementación revisada:** módulos de modelo, timeline y almacenamiento; Kotlin, Compose y Media3. Edición no destructiva, mezcla de audio, control de huecos entre pistas y exportación mediante un servicio con validación del archivo resultante.
- **Evidencia actual:** el 6 de octubre se comparó el proyecto recuperado con la app instalada: coinciden paquete, versión, certificado documentado y las 153 clases de producción declaradas. Es una reconciliación estática, sin afirmar identidad binaria.
- **Pruebas históricas:** ARCHITECTURE.md documenta 83 pruebas JVM y 20 pruebas instrumentadas sin fallos en el S25, además de exportaciones y medidas de imagen/audio. Esos resultados documentados no se han repetido en esta recuperación.
- **Límites:** varias interacciones de la interfaz de fase 2 siguen pendientes de revisión manual. Proxies, HDR, curvas de velocidad y el render de altas luces, sombras y nitidez no están completos. No se presenta como un editor terminado en todas sus funciones.

## ALEXIA

**04 · Biblioteca creativa · Android · Fuentes privadas**

Organiza material creativo por proyectos y conecta su índice local con los archivos y las herramientas de Android.

**Por qué forma parte de la selección:** aporta profundidad en almacenamiento e interoperabilidad, con evidencia concreta de conservación de originales e integridad de archivos.

- **Diseño de sistema:** separar el índice de la biblioteca del almacenamiento de los archivos.
- **Implementación:** Kotlin, Room, Storage Access Framework, DocumentsProvider e índice legible por agentes.
- **Evidencia revisada:** informe de **63 pruebas unitarias sin errores ni fallos** y comprobación histórica v68 en Pixel de imagen, vídeo, audio, SHA-256, idempotencia, conservación del original, DocumentsProvider y recuperación de escrituras interrumpidas.
- **Límite:** la fuente recuperada v69 y la versión instalada registrada v68 requieren reconciliación. Esta selección se apoya principalmente en arquitectura y pruebas; no atribuye a ALEXIA una superioridad visual que no se ha comprobado en esta revisión.

## Otros proyectos

### AXEL TV

**Experiencia entre dispositivos · Android TV y móvil**

Mando móvil, widget y puente de comunicación. Es una buena segunda línea por su interacción entre dispositivos. Existen entregas y pruebas históricas del mando; las variantes de TV aún necesitan reconciliación antes de presentarlas como un conjunto actual validado.

### AXEL Music

**Audio local · Android móvil y TV**

Biblioteca, cola, listas y recorte AAC/M4A. Las capturas muestran una interfaz propia y funciones locales concretas. Queda en segunda línea porque la documentación v0.2.1 vincula la reproducción a la actividad: la continuidad mediante servicio multimedia en segundo plano sigue pendiente. La conexión con YouTube Music es un relevo a su app oficial.

### AXELTask

**Agenda y tareas · Android · Fuentes privadas recuperadas**

Código para agenda, tareas, interpretación de texto, detección de conflictos e integración con el calendario del dispositivo. Tiene pantallas de preparación, movilidad y privacidad, además de la agenda.

La fuente recuperada declara package ai.axel.tasker, versión 1.0.0 y versionCode 1, coincidentes con la consulta de la instalación. Los informes existentes del 5 de septiembre registran **8 pruebas unitarias sin fallos ni errores** de interpretación y conflictos. No se han ejecutado de nuevo ni se ha revisado aquí su interfaz actual en el móvil. Es una candidata a la selección principal, pendiente de esa comparación.

### AXELDROBE

**Armario y conjuntos · Android · Fuentes privadas recuperadas**

Organiza prendas, propone conjuntos según disponibilidad, contexto e historial, y contempla planificación y lavandería. La lógica de sugerencias recuperada funciona mediante reglas locales.

La fuente declara package com.axel.axeldrobe.debug, versión 0.2.0-fixed y versionCode 2, coincidentes con la instalación consultada. Los informes existentes del 21 de septiembre registran **6 pruebas unitarias sin fallos ni errores** de interpretación de prendas y generación de conjuntos. No se ha validado aquí la experiencia actual del móvil. Es una candidata a la selección principal, pendiente de comparar diseño y flujos reales.

### DisAster

**Organización de archivos · Candidata pendiente de evaluación completa**

La edición Android instalada 3.7.3-permfix se ha recuperado completa desde su APK: recursos, interfaz web y código Smali. Se reconstruyó en el ASUS; las clases DEX coinciden y los assets mantienen sus bytes. Es una reconstrucción, con fuentes nativas originales pendientes. Su interfaz y sus flujos actuales todavía requieren evaluación funcional para decidir su lugar entre los destacados. La variante web se conserva por separado.

### Herramientas de apoyo

CineVault48, AXEL Control y el selector de compilaciones conservan su valor como herramientas especializadas e infraestructura. No encabezan esta presentación. [CineVault48 mantiene su código público](https://github.com/vidaltb94-collab/CineVault48).

---

La selección es editorial y provisional, basada en la evidencia accesible. No es una clasificación completa: Las fuentes de AXELTask y AXELDROBE ya se han recuperado; falta comparar su experiencia actual y revisar las demás apps pendientes. [Consultar el catálogo completo y sus pendientes](CATALOG.md). Los repositorios privados conservan su acceso restringido.
