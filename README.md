# Detección de Fraudes en Tarjetas de Crédito

Este proyecto utiliza varios algoritmos de aprendizaje automático para abordar el problema de detección de fraudes en transacciones de tarjetas de crédito. A través de técnicas avanzadas como el balanceo de clases y la combinación de modelos, se busca maximizar la precisión y la capacidad de generalización, mientras se minimizan los falsos negativos.

## Tabla de Contenidos

- [Introducción](#introducción)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Resultados Clave](#resultados-clave)
- [Guía de Uso](#guía-de-uso)
- [Contribuciones](#contribuciones)
- [Licencia](#licencia)

## Introducción

La detección de fraudes en tarjetas de crédito es un problema crítico en la industria financiera. Este proyecto implementa y compara múltiples modelos de aprendizaje automático, desde métodos individuales como KNN y SVM hasta modelos híbridos basados en Voting Classifiers. Además, se aplican técnicas de sobremuestreo (SMOTE y ADASYN) para abordar el desequilibrio de clases.

## Tecnologías Utilizadas

- Python 3.8+
- Bibliotecas principales:
  - `scikit-learn` (implementación de modelos y validación)
  - `imbalanced-learn` (balanceo de clases)
  - `pandas` y `numpy` (procesamiento de datos)
  - `matplotlib` y `seaborn` (visualización de resultados)

## Estructura del Proyecto

```
├── data
│   ├── creditcard.csv       # Dataset de transacciones de tarjetas de crédito
├── notebooks
│   ├── analysis.ipynb       # Análisis exploratorio de datos (EDA)
│   ├── modeling.ipynb       # Entrenamiento y evaluación de modelos
├── src
│   ├── preprocessing.py     # Funciones de limpieza y preprocesamiento
│   ├── modeling.py          # Implementación de modelos
│   ├── evaluation.py        # Métricas y visualización de resultados
├── results
│   ├── metrics.csv          # Tabla resumen con las métricas de los modelos
├── README.md                # Documentación del proyecto
```

## Resultados Clave

Los resultados obtenidos destacan las fortalezas y debilidades de cada modelo. A continuación, se muestra una tabla resumen:

| Modelo                   | Precisión (%) | Recall | F1-Score | AUC-ROC | Tiempo de Ejecución  |
|--------------------------|---------------|--------|----------|---------|-----------------------|
| KNN                      | 99.94         | 0.9912 | 0.9928   | 0.9961  | 1 segundo            |
| SVM                      | 99.92         | 0.9934 | 0.9929   | 0.9967  | 5 segundos           |
| Redes Neuronales (NN)    | 99.89         | 0.9901 | 0.9895   | 0.9955  | 4 minutos            |
| Logistic Regression (LR) | 99.93         | 0.61   | 0.71     | 0.92    | 20 segundos          |
| Random Forest (RF)       | 99.90         | 0.89   | 0.88     | 0.94    | 4 minutos            |
| Gradient Boosting (GB)   | 99.85         | 0.16   | 0.27     | 0.34    | 2 minutos            |
| Híbrido (RF-LR-GB)       | 99.95         | 0.64   | 0.75     | 0.93    | 1 minuto             |
| Híbrido (RF-LR-SVC)      | 99.94         | 0.00   | 0.00     | 0.81    | 2 horas              |

## Guía de Uso

1. **Instalación de Dependencias:**
   ```bash
   pip install -r requirements.txt
   ```

2. **Ejecutar el Análisis:**
   Abra y ejecute los notebooks en la carpeta `notebooks` para realizar el preprocesamiento, el entrenamiento y la evaluación de modelos.

3. **Visualizar Resultados:**
   Consulte los gráficos y las tablas generados en la carpeta `results` para analizar el desempeño de los modelos.

## Contribuciones

Las contribuciones son bienvenidas. Si desea contribuir:

1. Haga un fork del repositorio.
2. Cree una rama con la nueva funcionalidad: `git checkout -b feature/nueva-funcionalidad`.
3. Realice un pull request con una descripción detallada.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulte el archivo `LICENSE` para más información.
