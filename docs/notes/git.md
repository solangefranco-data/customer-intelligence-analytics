# Git y GitHub — Guía rápida

Comandos y conceptos de Git utilizados durante el desarrollo del proyecto.

## Comandos básicos

| Comando | Acción | Descripción |
|---|---|---|
| `git init` | Inicializar Git | Convierte la carpeta actual en un repositorio Git |
| `git status` | Ver estado | Muestra archivos nuevos, modificados y preparados |
| `git status --untracked-files=all` | Ver Untracked | Muestra individualmente todos los archivos todavía no rastreados |
| `git branch -M main` | Rama principal | Establece `main` como rama principal |
| `git add archivo` | Preparar archivo | Añade un archivo al área de staging |
| `git add .` | Preparar cambios | Añade todos los cambios actuales al área de staging |
| `git commit -m "mensaje"` | Crear commit | Guarda una versión de los cambios preparados |
| `git push` | Subir cambios | Envía los commits locales a GitHub |
| `git pull` | Descargar cambios | Trae cambios existentes en GitHub al repositorio local |
| `git log` | Ver historial | Muestra el historial de commits |

> `git add`, `commit`, `push` y `pull` los iremos utilizando y aprendiendo durante el proyecto.

---

# Conceptos básicos

## ¿Qué es Git?

**Git** es un sistema de control de versiones.

Permite registrar los cambios realizados en un proyecto y mantener un historial de sus diferentes versiones.

Git funciona principalmente sobre nuestro repositorio local.

## ¿Qué es GitHub?

**GitHub** permite almacenar y publicar online repositorios gestionados con Git.

Git y GitHub no son lo mismo.

```text
PROYECTO LOCAL
      │
      ▼
     GIT
      │
      ▼
COMMITS / HISTORIAL
      │
      ▼
    GITHUB
```

---

# Flujo habitual

El flujo que utilizaremos durante el proyecto será:

```text
MODIFICO ARCHIVOS
       │
       ▼
   git status
       │
       ▼
    git add
       │
       ▼
   git commit
       │
       ▼
    git push
       │
       ▼
     GitHub
```

## 1. Revisar qué cambió

```powershell
git status
```

Permite comprobar el estado actual antes de guardar cambios.

## 2. Preparar los cambios

Para seleccionar un archivo:

```powershell
git add README.md
```

Para seleccionar todos los cambios:

```powershell
git add .
```

Los archivos pasan al área denominada **staging**.

## 3. Crear una versión

```powershell
git commit -m "mensaje descriptivo"
```

Crea un punto en el historial con los cambios que estaban preparados.

Ejemplo:

```powershell
git commit -m "Initialize project structure"
```

## 4. Enviar a GitHub

```powershell
git push
```

Envía a GitHub los commits que existen localmente.

---

# Estados de los archivos

## Untracked

Un archivo **Untracked** existe dentro del proyecto, pero Git todavía no está realizando seguimiento sobre él.

VS Code lo identifica con:

```text
U
```

Ejemplo:

```text
U README.md
```

Significa que `README.md` es un archivo nuevo que todavía no fue agregado a Git.

## Modified

Un archivo **Modified** ya era conocido por Git pero posteriormente fue modificado.

VS Code puede mostrar:

```text
M
```

## Staged

Un archivo **Staged** fue seleccionado mediante `git add` y está preparado para formar parte del próximo commit.

Conceptualmente:

```text
UNTRACKED / MODIFIED
        │
        │ git add
        ▼
      STAGED
        │
        │ git commit
        ▼
   COMMITTED
```

---

# Ramas (Branches)

Una rama permite trabajar sobre una línea de desarrollo del proyecto.

Nuestra rama principal se llama:

```text
main
```

La establecimos mediante:

```powershell
git branch -M main
```

Más adelante aprenderemos a crear otras ramas cuando realmente las necesitemos.

---

# Comandos utilizados al iniciar este proyecto

## Inicializar Git

```powershell
git init
```

Convierte la carpeta actual en un repositorio Git.

## Establecer `main`

```powershell
git branch -M main
```

Define `main` como rama principal.

## Consultar estado

```powershell
git status
```

Muestra el estado del repositorio.

## Mostrar todos los archivos Untracked

```powershell
git status --untracked-files=all
```

Muestra individualmente todos los archivos nuevos, incluso los que se encuentran dentro de carpetas.

---

# Git y nuestro proyecto

Repositorio:

```text
customer-intelligence-analytics
```

Estructura inicial:

```text
customer-intelligence-analytics/
│
├── data/
├── docs/
│   ├── README.md
│   └── notes/
│       ├── vscode.md
│       ├── powershell.md
│       ├── git.md
│       ├── python.md
│       ├── pandas.md
│       └── visualization.md
├── images/
├── notebooks/
├── src/
├── .gitignore
├── README.md
└── requirements.txt
```

## Archivos importantes para GitHub

### README.md

Es la presentación principal del proyecto.

Incluirá progresivamente:

- objetivo
- problema de negocio
- dataset
- metodología
- tecnologías
- análisis
- resultados
- visualizaciones
- conclusiones

### .gitignore

Indica qué archivos o carpetas **no queremos incorporar al repositorio**.

Por ejemplo:

```text
.venv/
```

Nuestro entorno virtual de Python debe permanecer en nuestro ordenador y no subirse al repositorio.

### requirements.txt

Contendrá las librerías de Python necesarias para ejecutar el proyecto.

Ejemplo:

```text
pandas
matplotlib
jupyter
```

Esto permite que otra persona pueda conocer las dependencias necesarias para ejecutar el proyecto.