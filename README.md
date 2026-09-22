# proyecto-grupo-4
# 🎮 Emily: Project E

📚 **Ficha:** ADSO 3312737  
👨‍🏫 **Instructor:** Jose Rodrigo  
🔗 **Repositorio:** https://github.com/ADSO-3312737/proyecto-grupo-4

> *«Una casa que finge ser un hogar.»*

---

# 👥 Integrantes

- Frank Rubio Ruiz Cerón — desarrollo completo (diseño, programación en Blueprints, arte, audio, documentación y producción)

> El proyecto es individual: el grupo 4 está formado por una sola persona, tal como recoge toda la documentación del proyecto («Equipo: una persona»).

---

# 🧾 Descripción

**Emily: Project E** es una demo de videojuego de **terror psicológico en primera persona**, hecha en **Unreal Engine 5** con Blueprints. Se centra en la exploración, la narrativa ambiental y los puzzles educativos. **No tiene combate, armas, barra de salud ni temporizador:** la tensión sale de la atmósfera, el ritmo y lo que el jugador va descubriendo.

Emily despierta en un cuarto cerrado por fuera y no recuerda cómo llegó allí. No sabe que la vivienda está construida dentro de un complejo experimental subterráneo ni que ella es sujeto de un programa de investigación. Solo conserva su capacidad para razonar, y con ella tiene que salir.

## ❓ Qué problema resuelve

Como proyecto formativo, busca **demostrar que el concepto funciona**: que la exploración, los puzzles educativos y la narrativa ambiental pueden sostener por sí solos entre 25 y 40 minutos de tensión, sin combate ni sustos encadenados. La demo sirve además como **prueba de concepto** de un juego completo más grande.

También busca que los puzzles **enseñen**: se resuelven con **matemáticas y lógica proposicional**, y funcionan como mecanismos del propio lugar, no como minijuegos aparte.

## ⚙️ Qué hace el sistema

| Sistema | En qué consiste |
| --- | --- |
| Exploración | Recorrer la vivienda de Emily y el complejo subterráneo (**diez zonas jugables**) sin indicaciones en pantalla |
| Puzzles educativos | Tres obstáculos integrados en la casa: **perímetros** en la pizarra del cuarto oculto (abre la cerradura de tres ruedas), un **código de tres cifras** en el botiquín del baño (la pista está en la cocina) y **lógica proposicional** en el panel de conmutación de la habitación |
| Sistema de fusibles | Tres fusibles (5 A, 10 A y 16 A) repartidos por la casa. El de 16 A en el circuito PUERTA es obligatorio y abre la puerta industrial al subsuelo. Si se instalan los tres a la vez, hay sobrecarga (carga máxima: 2 circuitos) |
| Interacción con objetos | Recoger, examinar y usar objetos y documentos como herramienta narrativa |
| Linterna | Se enciende y se apaga con un botón, sin pilas ni recarga. El jugador decide cuándo usarla |
| Narrativa ambiental | La historia se descubre observando el entorno, sin diálogos que la expliquen |
| Guardado | Automático y discreto, en **cinco puntos de guardado** gestionados por `BP_ProgressManager` |
| Interfaz | Menú principal, HUD mínimo, pausa y opciones: **11 pantallas** (WF-01 a WF-11) |
| Accesibilidad | Subtítulos, tamaño de texto, sensibilidad de cámara, inversión de controles y reducción de movimiento |
| Final | Cinemática de cierre con la aparición de Syairah tras una puerta con ventana |

**Objetivos de calidad:** 60 FPS estables en el hardware recomendado, plataforma PC, idioma base español (todos los textos pasan por tablas de localización) y una build empaquetada probada en un equipo distinto del de desarrollo.

## 🛠 Tecnologías utilizadas

| Herramienta | Uso en el proyecto |
| --- | --- |
| **Unreal Engine 5.8.1** | Motor del juego. Programación **solo con Blueprints, sin C++**. Nanite, Lumen, LOD, UMG (interfaz), plugin GameplayStateTree |
| **Blender** | Modelado 3D, UVs, esculpido, rigging con Rigify y horneado de mapas |
| **GIMP** | Edición de texturas, decals y texturas con texto |
| **Audacity** | Edición y limpieza de audio (47 sonidos documentados) |
| **Git + Git LFS + GitHub** | Control de versiones. Los archivos binarios grandes van con LFS |
| **Obsidian** | Vault de la documentación (`documentacion/00_Documentacion`) |
| **draw.io** | Diagramas de flujo, de estados y de clases |
| **ambientCG / Poly Haven / freesound.org** | Texturas y sonidos con licencia verificable (CC0 u otra documentada) |
| **OBS Studio / DaVinci Resolve** | Grabación y edición del vídeo de entrega |

> ⚠ Todo asset externo, sea gratuito o no, necesita tener su **procedencia y licencia verificadas y documentadas** antes de entrar al proyecto.

---

# 📂 Estructura del repositorio

```
proyecto-grupo-4/
│
├── codigo/
│   └── EmilyProyectE/            → proyecto de Unreal Engine 5.8
│       ├── EmilyProyectE.uproject
│       ├── Config/               → configuración del motor, input y juego
│       └── Content/
│           ├── 01_Blueprints/    → Characters, Doors, Interaction, Items,
│           │                       Narrative, Systems, Utilities
│           ├── 02_Environment/   ├── 03_Props/      ├── 04_Materials/
│           ├── 05_Textures/      ├── 06_Animations/ ├── 07_Audio/
│           ├── 08_VFX/           ├── 09_Puzzles/    ├── 10_Level/
│           ├── 11_Cinematics/    ├── 12_Data/       └── 13_Saved/
│
├── documentacion/
│   └── 00_Documentacion/         → los 22 documentos de diseño (vault de Obsidian)
│       ├── 01_GDD/               → GDD v3.0 y Documento de Concepto
│       ├── 02_Historia/          → Historia y Lore
│       ├── 03_Gameplay/          → Gameplay y Campo de Punto Cero
│       ├── 04_Niveles/           → Diseño del Nivel v2.0
│       ├── 05_Enemigos/          → fichas de Syairah y Wilton
│       ├── 06_Puzzles/           → Mecánicas, Puzzles y Fusibles
│       ├── 07_Arte/              → Blockout, Catálogo, Conceptos, Mockups, Wireframes
│       ├── 08_Audio/             → Diseño Sonoro
│       ├── 09_Tecnico/           → Flujo v3.0, Clases v2.1, Almacenamiento, diagramas .drawio
│       ├── 10_Produccion/        → Plan de Producción v1.3, Control de Versiones, Formación
│       └── 11_Testing/           → Plan de Testing
│
└── diagramas/                    → diagramas de flujo, de estados (STATE_02/04, 05, 08)
    └── clases/                     y de clases (núcleo del jugador e interacción)
```

## 📑 Documentos principales

| Documento | Para qué sirve |
| --- | --- |
| Documento de Concepto | Resumen del proyecto en dos minutos: género, público, mecánicas y requisitos |
| GDD v3.0 | El documento base; los demás derivan de él |
| Diagrama de Flujo v3.0 | El recorrido completo en 12 estados (STATE_01 a STATE_12) |
| Diagrama de Clases v2.1 | Arquitectura de Blueprints (**21 clases**). Es la única fuente válida para los nombres `BP_` |
| Plan de Producción v1.3 | Fases, horas, hitos y plan de recorte |
| Plan de Testing | Cómo se verifica cada criterio de finalización |

---

# 🗓 Plan de trabajo

**750 horas** en **30 semanas**, más 6 semanas de colchón. El calendario empieza la semana del 7 de septiembre de 2026.

| Fase | Contenido | Hito | Fecha |
| --- | --- | --- | --- |
| F0 | Preparación: motor, carpetas, control de versiones, curso de Blueprints | — | S01 |
| F1 | Prototipo en cajas grises: personaje, linterna, zonas, puertas, puzzles, fusibles | H1 · Se juega entera | 02 nov 2026 |
| F2 | Contenido y arte: textos, arquitectura, mobiliario, props, materiales | H2 · Está vestida | 11 ene 2027 |
| F3 | Syairah y el final: modelo, animación, encuadre | H3 · Tiene final | 08 feb 2027 |
| F4 | Luz, sonido y atmósfera | H4 · Da miedo | 08 mar 2027 |
| F5 | Pulido, testeo, build y entrega | H5 · Entregable | 05 abr 2027 |
| — | Colchón | — | 17 may 2027 |

> **Regla de producción:** no entra ningún material, malla definitiva ni sonido hasta que la demo se pueda jugar entera en cajas grises, de principio a fin, con los tres puzzles funcionando.

---

# ⚙️ Instrucciones para trabajar con Git

Todos los avances se suben al repositorio con **Git**. El procedimiento completo está en `documentacion/00_Documentacion/10_Produccion/Emily_Project_E_Control_de_Versiones.docx`.

> ⚠ **El repositorio no va dentro de Google Drive.** Drive sincroniza en segundo plano la carpeta oculta `.git` y puede corromper el historial. Drive se usa como copia de trabajo de la documentación y como copia de seguridad; el repositorio vive en una carpeta local.

---

# 🔧 0. Instalación (solo una vez por ordenador)

Instalar Git desde https://git-scm.com (ya incluye **Git Bash** y **Git LFS**). Después, en Git Bash:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu-correo-de-github@ejemplo.com"
git lfs install
```

**Git LFS es obligatorio** en este proyecto: los `.uasset`, `.umap`, `.fbx`, `.blend`, `.wav`, `.psd` y `.mp4` son binarios grandes y se guardan con LFS (ver `.gitattributes`).

---

# 📥 1. Clonar el repositorio (solo la primera vez)

```bash
git clone https://github.com/ADSO-3312737/proyecto-grupo-4.git
cd proyecto-grupo-4
```

Para abrir el juego: doble clic en `codigo/EmilyProyectE/EmilyProyectE.uproject` con **Unreal Engine 5.8** instalado desde el Epic Games Launcher.

---

# 🔁 2. Actualizar antes de trabajar

```bash
git pull
```

---

# ➕ 3. Revisar y agregar archivos

```bash
git status
git add .
```

`git status` muestra qué archivos cambiaron. `git add .` los prepara todos para el commit.

---

# 💾 4. Crear un commit

El mensaje dice **qué cambió**, empezando por la fase en la que se trabaja:

```bash
git commit -m "F1: la cerradura de tres ruedas abre con el codigo 148"
```

---

# 🚀 5. Subir los cambios al repositorio

```bash
git push
```

Si GitHub rechaza el push, primero `git pull` y después `git push` otra vez.

---

# 🚫 Qué no se sube

El `.gitignore` deja fuera las carpetas que Unreal regenera solo y que ocupan gigabytes:

```
Binaries/   Intermediate/   DerivedDataCache/   Saved/   Build/
```

También quedan fuera los archivos de respaldo de Blender (`*.blend1`), los archivos temporales del sistema y la configuración personal de Obsidian (`workspace.json`).

Los `.docx` de la documentación se copian al repositorio **cuando un documento sube de versión o cambia su contenido**, no cada vez que se corrige una coma. Así, el historial muestra cómo evolucionó el diseño.

---

# 📊 Buenas prácticas

Un commit por avance real, al final de cada sesión de trabajo. Ejemplos de mensajes válidos:

```
F0: estructura de carpetas del proyecto de Unreal
F1: BP_Emily con movimiento y linterna
F1: los tres puzzles se resuelven seguidos
F2: materiales maestros del subsuelo
Docs: Plan de Produccion v1.3
Docs: correcciones de coherencia entre documentos
```

Mensajes como «cambios» o «avance» no sirven: no dicen qué cambió.

## 🆘 Cuando algo sale mal

| Situación | Comando |
| --- | --- |
| No sé en qué estado estoy | `git status` |
| Quiero ver el historial | `git log --oneline` |
| Quiero descartar cambios que aún no guardé | `git restore archivo` ⚠ no se puede deshacer |
| Subí algo que estaba mal | `git revert codigo-del-commit` |

> ⚠ **Nunca borres la carpeta `.git`**: contiene todo el historial del proyecto.  
> ⚠ **Git no es una copia de seguridad**: la copia semanal del proyecto completo (disco externo o nube) sigue siendo obligatoria.

---

# 📌 Regla del proyecto

Los commits se hacen **durante todo el desarrollo**, no solo al final. Así el historial demuestra el trabajo realizado y sirve como diario del proyecto para la sustentación.

El instructor revisará la participación en:

```
GitHub → Insights → Contributors
```
