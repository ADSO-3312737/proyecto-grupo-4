# 📘 Manual básico de GitHub para aprendices (con plastilina)
## 📚 Ficha ADSO 3312737  
👨‍🏫 Instructor: Jose Rodrigo  

---

# 🎯 Objetivo del manual

Este manual te enseña a usar GitHub para:

- 👥 Trabajar en equipo
- 💾 Guardar avances (commits)
- 🚀 Subir avances a internet (push)
- 🧾 Llevar historial de cambios

Cada grupo trabajará dentro de **un repositorio del proyecto**.

---

# 🧠 Conceptos básicos (explicado con plastilina)

## 📦 Repositorio

Un repositorio es como **una carpeta del proyecto pero en internet**.

Dentro se guardan:

- código
- documentos
- diagramas
- historial de cambios

Ejemplo de estructura:

```
proyecto-grupo-1
│
├── codigo/
├── documentacion/
└── diagramas/
```

---

## 💾 Commit

Un **commit** es guardar un cambio en el proyecto.

Es como presionar **guardar**, pero dejando registro de:

- qué cambió
- quién lo cambió
- cuándo lo cambió

Ejemplos de commits:

- "Estructura inicial del proyecto"
- "Se agregó el algoritmo principal"
- "Corrección de errores"

---

## 🚀 Push

Push significa **subir los cambios a GitHub**.

---

## 📥 Clone

Clone significa **copiar el repositorio de GitHub a tu computador**.

---

## 🔁 Pull

Pull significa **descargar los cambios que hicieron tus compañeros**.

---

# 🛠 Requisitos

Antes de empezar necesitas:

1️⃣ Crear cuenta en GitHub  
https://github.com  

2️⃣ Instalar Git  
https://git-scm.com  

La instalación incluye **Git Bash**, que será la terminal que usaremos.

---

# 🧭 Paso a paso (cogidos de la manito)

---

# 📥 Paso 1 — Clonar el repositorio

El instructor te dará la dirección del repositorio del grupo.

Ejemplo:

```
https://github.com/ADSO-3312737/proyecto-grupo-1
```

Abrir **Git Bash**.

Escribir:

```bash
git clone URL_DEL_REPOSITORIO
```

Ejemplo real:

```bash
git clone https://github.com/ADSO-3312737/proyecto-grupo-1.git
```

Entrar a la carpeta del proyecto:

```bash
cd proyecto-grupo-1
```

---

# 📂 Paso 2 — Revisar la estructura

El proyecto debe tener estas carpetas:

```
codigo/
documentacion/
diagramas/
```

---

# ✏️ Paso 3 — Crear o modificar archivos

Ejemplos de archivos:

```
codigo/algoritmo.py
documentacion/manual.md
diagramas/flujo.png
```

Puedes usar editores como:

- VS Code
- Notepad++
- IntelliJ

---

# 🔁 Paso 4 — Actualizar antes de trabajar

Antes de empezar a trabajar ejecuta:

```bash
git pull
```

Esto descarga los cambios que hayan subido tus compañeros.

---

# ➕ Paso 5 — Preparar los archivos

Cuando hayas hecho cambios ejecuta:

```bash
git add .
```

Esto prepara los archivos para guardarse.

---

# 💾 Paso 6 — Crear un commit

Guardar los cambios con un mensaje:

```bash
git commit -m "Descripción del cambio"
```

Ejemplos:

```bash
git commit -m "Se agregó el algoritmo de cálculo"
git commit -m "Se creó el diagrama de flujo"
```

---

# 🚀 Paso 7 — Subir cambios a GitHub

Subir los cambios:

```bash
git push
```

Ahora tus cambios aparecerán en GitHub.

---

# 🔁 Flujo normal de trabajo

Cada vez que trabajes debes hacer:

```bash
git pull
git add .
git commit -m "mensaje del cambio"
git push
```

---

# 👨‍👩‍👧‍👦 Trabajo en equipo

Cada integrante debe subir su propio trabajo.

No es correcto que solo una persona haga todos los commits.

---

# 📊 Evaluación del instructor

El instructor revisará el trabajo en:

```
Repositorio → Insights → Contributors
```

Allí se puede ver:

- quién subió código
- cuántos commits realizó
- cuándo trabajó

---

# 📌 Reglas del proyecto

Cada integrante debe:

✔ realizar commits  
✔ subir avances  
✔ documentar su trabajo  

Ejemplos de commits correctos:

```
Estructura inicial del proyecto
Se agregó algoritmo de inventario
Corrección de errores
Actualización del diagrama de flujo
Documentación del sistema
```

---

# ⚠️ Errores comunes

## ❌ No hacer commits

Si no haces commits **no aparecerá tu trabajo**.

---

## ❌ Una sola persona sube todo

Cada integrante debe subir su propio trabajo.

---

## ❌ No hacer pull antes de trabajar

Puede causar conflictos en el proyecto.

---

# 🎓 Resultado esperado

Al final el repositorio debe contener:

```
proyecto-grupo-X
│
├── codigo
├── documentacion
└── diagramas
```

y un historial de commits que demuestre el trabajo del grupo.

---

🚀 Ahora ya sabes usar GitHub para trabajar en tu proyecto.
