# **Predicción de Suscripción de Banco**
En un entorno altamente competitivo, las instituciones financieras enfrentan el desafío constante de diseñar estrategias de marketing más efectivas para captar y retener clientes. En este contexto, el presente trabajo aborda un problema planteado por un banco particular, que busca predecir cuáles de sus clientes es más probable que se suscriban a una campaña de marketing específica. La capacidad de identificar de manera precisa a estos clientes permitirá optimizar los recursos, reducir costos y aumentar la efectividad de las campañas, generando un impacto positivo tanto en los ingresos del banco como en la satisfacción de los clientes.

Para abordar este problema, se dispone de un conjunto de datos que comprende información de 45.211 clientes, descritos por 17 variables que reflejan características socioeconómicas, de comportamiento y de interacción con el banco.

# **Archivos del Proyecto**
- **clusterai_reporte_Ferreyra:** informe con los resultados principales del análisis
- **clusterai_Nicolas_Ferreyra_eda:** análisis EDA sobre el dataset
- **clusterai_Nicolas_Ferreyra_machine_learning:** implementación modelo de ML
- **clusterai_Nicolas_Ferreyra_completo:** compilado completo del proyecto
- **bank_subscription:** dataset empleado


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

Antes de ejecutar el proyecto, hay que tener instaladas las siguientes bibliotecas:

```
pip install pandas numpy scikit-learn matplotlib seaborn
```


# **Uso**
## **Cargar el notebook:**


El archivo principal del proyecto es un Jupyter Notebook.
Contiene secciones definidas con EDA y Machine Learning.

Guardar y cargar datos:
Los datos procesados se guardan en Google Drive para facilitar el uso entre notebooks:
```
from google.colab import drive
drive.mount('/content/drive')
clientes.to_csv('/content/drive/My Drive/clientes_new.csv', index=False)
```

## **Ejecución de los modelos:**

La sección de Machine Learning incluye la comparación de los modelos mencionados con los hiperparámetros óptimos.

# **Resultados**
## **EDA:**
-  Identificación de variables relevantes y posibles valores atípicos.
-  Relación entre Pdays y Previous, analizada mediante gráficos y matriz de correlación.
## **Modelos de Machine Learning:**
-  Random Forest mostró el mejor rendimiento sin PCA.
-  Igualmente todos los modelos tuvieron un rendimiento similar, pudiendo elegirse también otros modelos más sencillos
