# Catálogo del ecosistema

La portada muestra cuatro proyectos seleccionados. Este catálogo conserva el resto del ecosistema, incluidas las aplicaciones cuyas fuentes todavía están pendientes de localizar o consolidar.

**La selección del portafolio es provisional mientras se completa la evaluación de las apps pendientes.** Ausencia de una app en la portada no significa ausencia de código ni menor calidad.

## Proyectos seleccionados

[NEXUS, NutriShift, Corte y ALEXIA: alcance, evidencia y límites](PROJECTS.md).

## Fuentes registradas en repositorios

El índice interno documenta las ramas y la procedencia de las fuentes privadas. Recuperar una copia no acredita que sea la última versión ni que todas sus funciones estén validadas.

| Área | Proyectos |
| :--- | :--- |
| Creación y multimedia | ALEXIA · NEXUS · CineVault · CineVault48 · CreatorVault · Clasificador de fotos / variantes Android de DisAster · Corte · AudioTrim · Recortar Audio · PhotoLayers Studio · PromptClip · Keyframe Sorter · Despeja |
| Familia AXEL | AXEL AI · AXEL Browse · AXEL Music · AXEL Native · AXEL OSINT · AXEL Portable · AXEL TV · AXELTask · AXELDROBE · AXEL Stream · AXEL Media TV · AxShell · AXEL Control · AXEL Link · Mando AXEL · AxelMusic TV |
| Herramientas especializadas | Amazon Medical Portal · Derivación SNS · DerivaMAD4 · FarmaTools Ronda · AXELWORK |
| Planificación y organización | NutriShift · Cliptree |
| Web y variantes | DisAster web · DisAster (repositorio anterior) · Noelia y Vidal, variantes Claude y PWA |
| Dispositivos y asistentes locales | Dreame · S25 Manager · Dr. Axel · Aki Chat · AKI · AXEL Console · Lanzador Antigravity personal |

Las variantes de un producto y sus repositorios históricos no se cuentan como apps distintas. DisAster Android conserva las ramas históricas y una reconstrucción completa del APK instalado 3.7.3. Esa reconstrucción no sustituye las fuentes nativas originales que siguen pendientes de localizar.

## Apps pendientes de consolidar

Las fuentes de AXELTask, AXELDROBE y Cliptree se localizaron en las carpetas de trabajo de Antigravity y ya están publicadas en repositorios privados. Sus fichas están [aquí](PROJECTS.md#axeltask). La recuperación añadió también PhotoLayers Studio, Recortar Audio, AXEL Stream y AXEL Media TV. Las variantes de proyectos existentes se conservan en ramas separadas. No se han recompilado durante esta recuperación.

Estos proyectos requieren completar su recuperación:

| App | Pendiente |
| :--- | :--- |
| **Despeja** | Localizar el proyecto original; se conserva una reconstrucción de su APK. |
| **AXEL Console** | Localizar el proyecto original; su reconstrucción desde APK compila. |
| **DisAster Android** | Localizar las fuentes nativas originales; la edición instalada 3.7.3 se conserva reconstruida y compilable. |
| **AXEL Android (`ai.axel.app`)** | Código Java recuperado dentro de un árbol mezclado con ALEXIA; separar y reconciliar su configuración de compilación. |

## Inventario Android ampliado

La revisión de APK del 6 de octubre identifica **35 entradas de apps Android propias**, incluidas apps complementarias y prototipos. Las variantes de pruebas se agrupan con su app principal. Este recuento describe el archivo Android; los proyectos web y herramientas del catálogo tienen otro alcance.

Además de las apps anteriores, se localizaron **AXEL Console, AXELWORK, Dr. Axel, Aki Chat y un lanzador Antigravity personal**. Sus APK confirman su existencia, pero su funcionamiento actual y su inclusión en la selección principal están pendientes de evaluar. Las fuentes de AXELWORK, Dr. Axel, Aki Chat, AKI y el lanzador ya están publicadas en repositorios privados. Las 8 clases de AKI aparecen en su APK instalado; su carpeta original no incluye un proyecto Gradle completo. AXEL Android `ai.axel.app` conserva sus fuentes Java dentro de un árbol con configuración ALEXIA, archivado sin mezclarlo con la fuente principal. AXEL Console conserva una reconstrucción de su APK que compila; su proyecto original sigue pendiente. Ninguna de estas recuperaciones acredita por sí sola una prueba funcional actual.

**Keyframe Sorter y DisAster son apps distintas.** Keyframe Sorter figura en la recuperación base del repositorio `clasificador-fotos`; DisAster conserva otras ramas de recuperación. AXEL Link, Mando AXEL y AxelMusic TV tienen APK propios como apps complementarias.

El registro completo de identidades, versiones y pendientes está en el [índice privado](https://github.com/vidaltb94-collab/apps-index/blob/codex/migration-20261006/APK-INVENTORY.md). La búsqueda incluye archivos antiguos y copias; no demuestra que todas las fuentes sean la última edición.

## Repositorios y componentes por reconciliar

- **AppOrganizer:** repositorio sin fuentes en la revisión anterior.
- **NEXUS-Studio:** repositorio separado sin fuentes en la revisión anterior; el escritorio de NEXUS sí figura en el proyecto NEXUS.
- **Or:** archivo ZIP de CreatorVault, pendiente de organizar como fuente navegable.
- **salon:** repositorio añadido después del inventario inicial, pendiente de revisión.
- **AXEL Stream y AXEL Media TV:** fuentes recuperadas; funcionamiento actual pendiente de comprobar.
- **Selector de compilaciones:** infraestructura de desarrollo, fuera de la selección principal de aplicaciones.
- **apps-index:** índice interno de fuentes, variantes y pendientes.
- **Repositorio del perfil:** presentación pública del ecosistema.

Última revisión: **6 de octubre de 2026**. El catálogo sigue abierto a fuentes que aparezcan en otros dispositivos o respaldos.
