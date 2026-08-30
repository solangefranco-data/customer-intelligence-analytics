# Instalar lo mínimo

### Para empezar con el análisis de datos, instalaría solo:


```powershell
python -m pip install pandas jupyter openpyxl
```


| Librería   | Para qué la vamos a usar                 |
| ---------- | ---------------------------------------- |
| `pandas`   | cargar, limpiar y analizar datos         |
| `jupyter`  | crear y ejecutar notebooks               |
| `openpyxl` | trabajar con archivos Excel desde Python |


Después verificamos

Cuando termine:
```powershell
python -m pip list
```

Esto muestra todas las librerías instaladas en .venv.

### Y luego:
```powershell
python -c "import pandas; print(pandas.__version__)"
```

¿Para qué sirve este último comando?

Hace una prueba rápida:
importa pandas
muestra su versión
si no hay error, sabemos que la instalación funciona