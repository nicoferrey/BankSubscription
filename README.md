# **Estructura del Proyecto**

## **1. Exploración y Limpieza de Datos**
- **Inspección inicial:** Se analiza la estructura de los datos para identificar tipos de variables y valores faltantes.
- **Tratamiento de valores nulos:**
  - Variables categóricas: Rellenadas con la moda o agrupadas en categorías como "Otros" o "Desconocido".
  - Variables numéricas: Imputadas con la mediana o media.
- **Codificación de variables categóricas:** Conversión a variables dummy para su uso en modelos.
- **Estandarización de datos:** Se escala el dataset para técnicas que lo requieran, como PCA o SVM.

## **2. Análisis Exploratorio (EDA)**
- Gráficos de distribución para variables numéricas.
- Relación entre variables categóricas y la variable objetivo (`Subscription`).
- Matriz de correlación para identificar relaciones entre variables numéricas.
- Visualización de relaciones clave con gráficos como scatterplots, heatmaps y pairplots.

## **3. Reducción de Dimensionalidad**
- **PCA (Análisis de Componentes Principales):**
  - Identificación del número óptimo de componentes mediante varianza explicada acumulada y Scree Plot.
  - Comparación del rendimiento de modelos con y sin PCA.

## **4. Modelos de Machine Learning**
Se implementaron y compararon los siguientes modelos:
- **Random Forest**
- **Logistic Regression**
- **Red Neuronal (MLPClassifier)**

### **Optimización:**
- Uso de **Grid Search** y validación cruzada para seleccionar los mejores hiperparámetros para cada modelo.

### **Evaluación:**
- **Métricas utilizadas:**
  - Accuracy
  - Precision
  - Recall
  - F1-Score
- Comparativa final entre modelos, con y sin reducción de dimensionalidad.

---

# **Requisitos**

Antes de ejecutar el proyecto, asegúrate de tener instaladas las siguientes bibliotecas:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn

Accuracy
Precision
Recall
F1-Score
Comparativa final entre modelos, con y sin reducción de dimensionalidad.
Requisitos
Antes de ejecutar el proyecto, asegúrate de tener instaladas las siguientes bibliotecas:

bash
Copiar código
pip install pandas numpy scikit-learn matplotlib seaborn
Uso
Cargar el notebook:

El archivo principal del proyecto es un Jupyter Notebook.
Contiene secciones bien definidas con EDA, PCA, y evaluación de modelos.
Guardar y cargar datos:

Los datos procesados se guardan en Google Drive para facilitar el uso entre notebooks:
python
Copiar código
from google.colab import drive
drive.mount('/content/drive')
clientes_new.to_csv('/content/drive/My Drive/clientes_new.csv', index=False)
Ejecución de los modelos:

La sección de Machine Learning incluye la comparación de los modelos mencionados con los hiperparámetros óptimos.
Resultados
EDA:
Identificación de variables relevantes y posibles valores atípicos.
Relación clara entre Pdays y Previous, analizada mediante gráficos y matriz de correlación.
Modelos de Machine Learning:
Random Forest mostró el mejor rendimiento sin PCA.
SVM tuvo mejoras significativas tras la reducción de dimensionalidad.
