# PowerShell — Comandos útiles

Comandos de terminal utilizados durante el desarrollo del proyecto.

## Comandos básicos

| Comando | Acción | Descripción |
|---|---|---|
| `cd $HOME` | Ir a Home | Va a la carpeta personal del usuario |
| `cd carpeta` | Entrar en carpeta | Cambia la ubicación actual a la carpeta indicada |
| `pwd` | Ver ubicación | Muestra la ruta en la que estoy trabajando |
| `mkdir carpeta` | Crear carpeta | Crea una nueva carpeta |
| `New-Item archivo` | Crear archivo | Crea un nuevo archivo |
| `Remove-Item archivo` | Eliminar archivo | Elimina el archivo indicado |
| `Get-ChildItem` | Listar contenido | Muestra archivos y carpetas de la ubicación actual |
| `dir` | Listar contenido | Forma corta/alias para listar archivos y carpetas |
| `code .` | Abrir VS Code | Abre la carpeta actual como proyecto en VS Code |
| `Get-History` | Ver historial | Muestra comandos ejecutados durante la sesión |

---

## Ejemplos útiles

### Crear varias carpetas a la vez

```powershell
mkdir data, notebooks, src, images
```

### Crear un archivo

```powershell
New-Item README.md
```

### Crear un archivo dentro de una carpeta

```powershell
New-Item docs/notes/python.md
```

### Ver el contenido de una carpeta específica

```powershell
Get-ChildItem docs
```

También:

```powershell
dir docs
```

### Eliminar un archivo

```powershell
Remove-Item docs/learning_notes.md
```

---

## Conceptos importantes

### `cd`

Significa **Change Directory**.

Se utiliza para desplazarse entre carpetas.

```powershell
cd customer-intelligence-analytics
```

### `$HOME`

Representa la carpeta personal del usuario.

```powershell
cd $HOME
```

Ejemplo:

```text
C:\Users\solan
```

### `.`

El punto representa la **ubicación actual**.

Por eso:

```powershell
code .
```

significa:

> Abrir la carpeta actual en Visual Studio Code.

### Recuperar comandos anteriores

Usar:

```text
↑
```

permite recuperar los comandos ejecutados anteriormente sin tener que volver a escribirlos.