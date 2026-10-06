# Proyectos seleccionados

Una selección del ecosistema, agrupada por el problema que resuelve cada producto. Las descripciones se apoyan en sus fuentes y documentación. Esta publicación presenta los proyectos; no certifica una nueva compilación ni una prueba completa de todas sus funciones.

[Volver al perfil](https://github.com/vidaltb94-collab)

## ALEXIA

**Biblioteca creativa · Android · Código privado**

Reúne el material creativo por proyectos, con un índice local y archivos accesibles a través de las herramientas del sistema.

- **Decisión de diseño:** separar el índice de la biblioteca del almacenamiento de los archivos.
- **Implementación documentada:** Room, Storage Access Framework, DocumentsProvider e índice legible por agentes.
- **Tecnologías:** Kotlin, Android y Room.
- **Estado:** fuentes versionadas y documentación de arquitectura. La recuperación del repositorio conserva evidencia de versiones y continuidad; no equivale a validar de nuevo la aplicación instalada.

## NEXUS

**Creación con IA · Android · Código privado**

Unifica la selección de modelos, la introducción de parámetros y la consulta de generaciones de imagen, vídeo y audio.

- **Decisión de diseño:** adaptar los formularios a las capacidades del modelo y separar los proveedores de la interfaz.
- **Implementación documentada:** catálogo de modelos, biblioteca de resultados, seguimiento de trabajos y reproducción multimedia.
- **Tecnologías:** Kotlin, Jetpack Compose, Material 3, WorkManager, Media3 y APIs de proveedores.
- **Estado:** proyecto en desarrollo con fuentes versionadas. La disponibilidad y el coste de cada modelo dependen del proveedor y de la configuración del usuario.

## AXEL TV

**Experiencia multidispositivo · Android TV y móvil · Código privado**

Conecta la experiencia de televisión con un mando móvil y un puente de red para consultar el estado y enviar acciones autorizadas.

- **Decisión de diseño:** mantener separados la aplicación de TV, el mando y el puente de comunicación.
- **Implementación documentada:** servidor LAN, mando Android, widget y recuperación de conectividad.
- **Tecnologías:** Android, Kotlin, Java y Python.
- **Estado:** existen pruebas y entregas documentadas del mando. La base de TV recuperada tiene pendiente la reconciliación con la versión instalada; no se presenta como una entrega actual validada en su conjunto.

## AXEL Control

**Panel del ecosistema · Windows · Código privado**

Agrupa el acceso a AXEL, las consultas de salud del conector y la recuperación de su proceso local en una interfaz de escritorio.

- **Decisión de diseño:** reutilizar la infraestructura existente y verificar el estado antes de actuar.
- **Implementación documentada:** panel, bandeja del sistema, consultas autenticadas y comprobación de integridad de artefactos.
- **Tecnologías:** C# / .NET Framework y PowerShell, con herramientas de compilación para Linux.
- **Estado:** fuentes de entrega y controles de diagnóstico documentados. El ejecutable descrito en el repositorio no dispone de firma Authenticode.

## CineVault48

**Organización visual · Android · [Código público](https://github.com/vidaltb94-collab/CineVault48)**

Organiza imágenes cinematográficas generadas con IA por proyecto, fecha y tipo de material, diferenciando las imágenes temporales de las permanentes.

- **Decisión de diseño:** importar únicamente lo seleccionado por el usuario mediante Photo Picker.
- **Implementación documentada:** retención de 48 horas, papelera con periodo de gracia, selección múltiple y modo de simulación.
- **Tecnologías:** Kotlin, SQLite y WorkManager.
- **Estado:** código y documentación públicos, con pruebas y workflow definidos. La existencia de esos archivos no acredita una ejecución reciente del workflow ni todas las integraciones externas.
- **Para revisar:** [arquitectura](https://github.com/vidaltb94-collab/CineVault48/blob/main/docs/ARCHITECTURE.md), [esquema de datos](https://github.com/vidaltb94-collab/CineVault48/blob/main/docs/DATABASE.sql) e [instalación](https://github.com/vidaltb94-collab/CineVault48/blob/main/docs/DEPLOYMENT.md).

## Selector de compilaciones

**Automatización de desarrollo · Linux, Windows y Android**

Evalúa el ecosistema antes de compilar y remite cada trabajo a un ejecutor compatible según disponibilidad, memoria, carga y temperatura.

- **Decisión de diseño:** utilizar los equipos dedicados cuando conviene y limitar la carga en los dispositivos de uso interactivo.
- **Implementación:** copias aisladas de las fuentes con manifiestos SHA-256, una compilación por nodo, recuperación de logs y verificación de artefactos.
- **Tecnologías:** Python, PowerShell, SSH, Tailscale y ADB.
- **Estado:** 39 pruebas automatizadas superadas en la revisión del 6 de octubre de 2026 y control de pausa, reanudación y terminación comprobado en un ejecutor Linux. La prueba completa de protección bajo carga en Windows y la telemetría física del móvil siguen pendientes. El resultado de una prueba local no se extiende a todos los dispositivos.

---

## Lectura del portafolio

**Código público** permite revisar el repositorio sin acceso adicional. **Código privado** indica que esta ficha describe el proyecto sin exponer sus fuentes. **En desarrollo** no equivale a una aplicación publicada ni a una versión certificada para producción.

Última revisión de estas fichas: **6 de octubre de 2026**.
