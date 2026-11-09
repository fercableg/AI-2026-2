# Inteligencia Artificial — Tareas (2026-2)

Universidad Diego Portales, Facultad de Ingeniería y Ciencias, segundo semestre 2026.

## Integrantes

- Fernando Cabrera Legue (T1, T2 y T3)
- Magdalena Correa (T2 y T3)
- Martin Melo (T2 y T3)
- Nhayara Ramos (T1)

## Descripción

Repositorio con las tres tareas del curso **Inteligencia Artificial**. Cada tarea se desarrolla en una carpeta propia y se entrega en Jupyter Notebook.

| Tarea | Contenido | Entrega |
|---|---|---|
| 1 | Redes Bayesianas, cadenas de Markov / HMM y método de Monte Carlo | `Tarea_1/Fernando_Cabrera_Nhayara_Ramos_Tarea1.ipynb` |
| 2 | Aprendizaje supervisado, semisupervisado y no supervisado | `Tarea_2/Part1.ipynb`, `Tarea_2/Part2.ipynb`, `Tarea_2/Part3.ipynb` |
| 3 | Redes neuronales convolucionales (CNN) para clasificación de imágenes | Pendiente |

## Contenido del repositorio

```
IA/
├── Tarea_1/
│   ├── energydata_complete.csv
│   ├── Fernando_Cabrera_Nhayara_Ramos_Tarea1.ipynb
│   ├── Rúbrica_T1_IA_2026_2.pdf
│   └── T1_IA2026-2.pdf
├── Tarea_2/
│   ├── Datasets/
│   │   ├── default of credit card clients.xls
│   │   ├── letter-recognition.data
│   │   └── open-meteo-33.36S70.56W906m.csv
│   ├── Part1.ipynb
│   ├── Part2.ipynb
│   ├── Part3.ipynb
│   ├── Rúbrica_T2_IA_2026_2.pdf
│   └── T2_IA2026-2.pdf
├── Tarea_3/
│   └── T3_IA2026-2.pdf
├── .gitignore
├── requirements.txt
└── README.md
```

## Datasets utilizados

| Tarea | Pregunta | Dataset | Fuente |
|---|---|---|---|
| 1 | 1. Redes Bayesianas | Adult | https://archive.ics.uci.edu/dataset/2/adult |
| 1 | 2. Markov / HMM | Appliances Energy Prediction | https://archive.ics.uci.edu/dataset/374/appliances+energy+prediction |
| 1 | 3. Monte Carlo | — (datos simulados) | — |
| 2 | 1. Regresión lineal y logística | Default of Credit Card Clients | https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients |
| 2 | 2. Supervisado vs semisupervisado | Letter Recognition | https://archive.ics.uci.edu/dataset/59/letter+recognition |
| 2 | 3. Clustering no supervisado | Open-Meteo (Santiago) | https://open-meteo.com/ |
| 3 | Clasificación de imágenes | Peces submarinos (especies) | Enlace del enunciado |

Los datasets están incluidos en el repositorio, por lo que no hace falta descargarlos manualmente: están en la carpeta de cada tarea (la Tarea 2 en `Tarea_2/Datasets/`). La única excepción es el dataset `Adult` de la Tarea 1, que se descarga automáticamente desde el notebook con `ucimlrepo`.

## Requisitos

- Python 3.12+ (desarrollado con Python 3.14)
- Git
- VS Code con las extensiones de Python y Jupyter (o Jupyter Notebook)

Librerías principales por tarea:

- **Tarea 1:** `pandas`, `numpy`, `matplotlib`, `pgmpy`, `hmmlearn`, `ucimlrepo`
- **Tarea 2:** `pandas`, `numpy`, `matplotlib`, `scikit-learn`, `xlrd`
- **Tarea 3:** `tensorflow` (o `pytorch`), `pandas`, `numpy`, `matplotlib`

## Cómo preparar el entorno

### 1. Clonar el repositorio

```bash
git clone <URL_DEL_REPO>
cd IA
```

### 2. Crear el entorno virtual

Windows:

```powershell
py -3 -m venv venv_ia
```

Linux o macOS:

```bash
python3 -m venv venv_ia
```

### 3. Activar el entorno virtual

Windows (PowerShell):

```powershell
.\venv_ia\Scripts\Activate.ps1
```

Si PowerShell bloquea la activación, ejecutar una vez el siguiente comando y volver a activar:

```powershell
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

Windows (CMD):

```cmd
venv_ia\Scripts\activate.bat
```

Linux o macOS:

```bash
source venv_ia/bin/activate
```

Cuando el entorno está activo, aparece `(venv_ia)` al inicio de la línea de la terminal.

### 4. Instalar las dependencias

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

> Para la Tarea 3 se necesita además un framework de deep learning (`tensorflow` o `pytorch`), que no está incluido en `requirements.txt`. Instálalo según tu sistema.

### 5. Registrar el kernel de Jupyter

```bash
python -m ipykernel install --user --name venv_ia --display-name "Python (IA 2026-2)"
```

### 6. Abrir los notebooks

Abrir el notebook de la tarea en VS Code y seleccionar el kernel **Python (IA 2026-2)** en la esquina superior derecha. Ejecutar las celdas en orden de arriba hacia abajo.

Para desactivar el entorno al terminar:

```bash
deactivate
```
