# Demanda de Potencia Mensual - Análisis y Predicción

Este proyecto tiene como objetivo analizar y predecir la demanda de potencia mensual para la Administración Nacional de Electricidad (ANDE). El análisis se basa en datos históricos y otros factores relevantes relacionados con la demanda de energía eléctrica.

## Estructura del Proyecto

```
gillopy-demanda_de_potencia_max_ande_deployment/
├── data/                     # Input data folder (ignored by Git)
│   └── demanda2.xlsx         # Archivo de datos de entrada
├── src/                      # Source code
│   ├── data_analyzer.py      # Módulo para el análisis de datos
│   ├── data_loader.py        # Carga de datos
│   ├── data_visualizer.py    # Visualización de datos
│   ├── main.py               # Orquesta todo el flujo de análisis
│   └── __pycache__/          # Archivos compilados de Python
├── LICENSE                   # Licencia del proyecto
├── pyproject.toml            # Configuración de Poetry
├── README.md                 # Documentación del proyecto (este archivo)
```

## Requisitos

- **Python 3.10 o superior**: Este proyecto está desarrollado para versiones recientes de Python.
- **Poetry**: Herramienta para la gestión de dependencias y creación de entornos virtuales.

## Dependencias

Todas las dependencias están listadas en el archivo `pyproject.toml`. Algunas de las bibliotecas clave incluyen:

- **pandas**: Manipulación y análisis de datos
- **scikit-learn**: Preprocesamiento de datos y entrenamiento de modelos
- **matplotlib / seaborn**: Visualización de datos
- **numpy**: Cálculos numéricos

## Configuración

### 1. Clonar el Repositorio

Primero, clona este repositorio en tu máquina local:

```bash
git clone https://github.com/gillopy/Ande_Demanda_de_Potencia_Mensual.git
cd Ande_Demanda_de_Potencia_Mensual
```

### 2. Instalar Dependencias

Usa Poetry para instalar todas las dependencias necesarias:

```bash
poetry install
```

Este comando:
- Crea un entorno virtual.
- Instala todas las dependencias definidas en el archivo `pyproject.toml`.

### 3. Preparar el Entorno

Asegúrate de que el archivo de datos `demanda2.xlsx` esté ubicado en la carpeta `data/`.

## Uso

Para ejecutar el análisis y la predicción de la demanda de potencia, utiliza el siguiente comando:

```bash
poetry run python src/main.py
```

## Output

- El script ejecutará todo el flujo de trabajo, desde la carga de datos hasta la visualización de los resultados.
- Los gráficos generados se mostrarán en pantalla y pueden ser exportados para su posterior análisis.

## Detalles

### Datos

**Datos de Entrada**:
- Los datos se encuentran en el archivo `data/demanda2.xlsx`.
- El archivo contiene información histórica sobre la demanda de energía eléctrica, con columnas relevantes que son procesadas para análisis y predicción.

**Preprocesamiento**:
- Los valores faltantes se manejan adecuadamente.
- Se realizan transformaciones en las columnas numéricas y categóricas para prepararlas para el modelo de predicción.

### Análisis

**Análisis de Datos**:
- El módulo `data_analyzer.py` realiza un análisis exploratorio de los datos, mostrando estadísticas descriptivas y visualizaciones clave.

**Visualización de Datos**:
- El módulo `data_visualizer.py` genera gráficos que permiten visualizar las tendencias y patrones en los datos.

### Predicción

**Modelo**:
- Actualmente, el flujo de trabajo no incluye un modelo predictivo entrenado, pero está preparado para ser extendido con métodos de predicción basados en scikit-learn o cualquier otro modelo de machine learning según sea necesario.

**Evaluación**:
- El rendimiento del modelo debe ser evaluado en un conjunto de datos de prueba (si se implementa un modelo predictivo).

**Guardado**:
- Los resultados del análisis y las visualizaciones pueden ser exportados como archivos de imagen o CSV según se requiera.

## Contribuciones

Si deseas contribuir a este proyecto, sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una nueva rama para tu contribución.
3. Realiza los cambios y haz un commit con un mensaje claro.
4. Abre un Pull Request describiendo tus cambios.

## Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo LICENSE para más detalles.
