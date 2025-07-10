# Análisis y Predicción del Diagnóstico de Cáncer de Mama

Este proyecto aplica técnicas de aprendizaje automático supervisado para predecir si un tumor es maligno o benigno, utilizando el reconocido conjunto de datos Breast Cancer Wisconsin (Diagnostic).  
El objetivo es comparar modelos de clasificación y seleccionar el más preciso y robusto para su posible aplicación en entornos clínicos.

## Dataset

- **Fuente:** [Kaggle - Breast Cancer Wisconsin (Diagnostic) Data Set](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data/data)  
- **Observaciones:** 569 registros  
- **Clases objetivo:**  
  - `M` = Maligno  
  - `B` = Benigno  
- **Variables:** 30 características numéricas (radio, textura, perímetro, etc.) derivadas de imágenes médicas.
- 
## Objetivos
- Realizar análisis exploratorio y visualización de datos (EDA).
- Aplicar técnicas de preprocesamiento y escalado con `ColumnTransformer`.
- Entrenar y evaluar múltiples modelos de clasificación binaria.
- Comparar rendimiento con métricas: `Accuracy`, `Precision`, `Recall`, `F1-Score`, `ROC-AUC`.
- Seleccionar el mejor modelo según rendimiento y robustez.
- Visualizar resultados con curvas ROC y matrices de confusión.
- 
## Modelos Evaluados
- **Regresión Logística**
- **KNN (con búsqueda de hiperparámetros)**
- **Random Forest (con búsqueda de hiperparámetros)**

Todos los modelos se integran en `Pipeline` y se validan con `cross-validation`.

## Visualizaciones Clave
- Distribución de clases (`diagnosis`)
- Boxplots por clase
- Matriz de correlación entre variables
- Matrices de confusión 1x3 (para comparar modelos)
- Curvas ROC superpuestas con valores de AUC

## Conclusiones
- **Random Forest** fue el mejor modelo: precisión perfecta (1.0) y AUC = 1.00.
- **Regresión Logística** también obtuvo excelentes resultados con AUC = 1.00.
- **KNN** tuvo desempeño ligeramente inferior en Recall (0.90), aunque competitivo.
- Todos los modelos muestran un alto nivel de discriminación entre tumores benignos y malignos.

Se recomienda usar Random Forest como modelo final por su balance óptimo entre precisión, robustez y capacidad predictiva sin errores críticos.

---

## 🧱 Estructura del Repositorio

