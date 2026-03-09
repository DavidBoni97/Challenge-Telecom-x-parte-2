# Challenge Telecom X parte 2
Este proyecto tiene como objetivo analizar y predecir la **cancelación de clientes (Churn)** en la empresa ficticia **Telecom X**, utilizando técnicas de análisis de datos y machine learning.

La cancelación de clientes representa uno de los principales desafíos en empresas de telecomunicaciones, ya que implica pérdida de ingresos y mayores costos asociados a la adquisición de nuevos clientes. Por esta razón, identificar **qué factores influyen en la cancelación** y **predecir qué clientes tienen mayor riesgo de abandonar el servicio** es fundamental para diseñar estrategias de retención.

En este proyecto se desarrolló un pipeline completo de análisis de datos que incluye **limpieza de datos, análisis exploratorio, preparación para machine learning, entrenamiento de modelos predictivos y análisis de variables relevantes**.

#  Objetivos del análisis

- Analizar los factores que influyen en la cancelación de clientes.
- Preparar los datos para su utilización en modelos de machine learning.
- Construir modelos predictivos capaces de identificar clientes con riesgo de churn.
- Evaluar el desempeño de diferentes algoritmos de clasificación.
- Identificar las variables más importantes que explican la cancelación.
- Proponer estrategias de retención basadas en los resultados obtenidos.

# Dataset

El dataset utilizado contiene información sobre clientes de Telecom X, incluyendo:

- Datos demográficos
- Tipo de contrato
- Servicios contratados
- Información de facturación
- Tiempo de permanencia del cliente
- Estado de cancelación del servicio (Churn)

Cada registro representa un cliente y su comportamiento dentro de la empresa.

#  Proceso de análisis

El proyecto se desarrolló siguiendo las etapas típicas de un flujo de trabajo en Data Science:

### 1) Extracción y limpieza de datos

- Importación de datos desde una API en formato JSON.
- Normalización de estructuras anidadas del dataset.
- Conversión de variables categóricas a formato numérico.
- Tratamiento de valores faltantes.

### 2) Preparación de datos

- Eliminación de variables irrelevantes (por ejemplo, identificadores de clientes).
- Codificación de variables categóricas mediante **One-Hot Encoding**.
- Balanceo de clases utilizando **SMOTE**, debido al desbalance entre clientes activos y cancelados.

### 3) Análisis exploratorio de datos (EDA)

Se analizaron las relaciones entre variables y la cancelación de clientes mediante:

- Boxplots
- Scatter plots
- Matriz de correlación
- Comparación de variables numéricas con churn

Este análisis permitió identificar patrones importantes relacionados con la cancelación.

### 4) Entrenamiento de modelos predictivos

Se entrenaron dos modelos de clasificación:

- **Regresión Logística**
- **Random Forest**

Se eligieron estos modelos porque permiten comparar enfoques distintos:

- Modelos lineales sensibles a la escala de los datos.
- Modelos basados en árboles que capturan relaciones no lineales.

### 5) Evaluación de modelos

Los modelos fueron evaluados utilizando las siguientes métricas:

- Accuracy
- Precision
- Recall
- F1-score
- Matriz de confusión

Esto permitió comparar su desempeño en la predicción de cancelación.

### 6) Interpretación de variables

Se analizaron las variables más relevantes en la predicción del churn utilizando:

- Coeficientes del modelo de **Regresión Logística**
- Importancia de variables del modelo **Random Forest**

# Principales insights

El análisis permitió identificar varios factores asociados a la cancelación de clientes:

- **Tiempo de contrato (tenure):** los clientes con menor antigüedad presentan mayor probabilidad de cancelar.
- **Tipo de contrato:** los contratos mensuales presentan mayor churn que los contratos anuales o bianuales.
- **Gasto total del cliente:** los clientes que cancelan tienden a tener menor gasto acumulado.
- **Servicios adicionales:** clientes que no utilizan servicios como soporte técnico o seguridad en línea muestran mayor probabilidad de cancelar.

Estos factores permiten comprender mejor el comportamiento de los clientes y anticipar posibles cancelaciones.

# Recomendaciones estratégicas

A partir de los resultados obtenidos, se proponen algunas estrategias para reducir la cancelación de clientes:

- Implementar programas de **retención temprana** para clientes nuevos.
- Incentivar contratos de **mayor duración** mediante descuentos o beneficios.
- Promover el uso de **servicios adicionales**, aumentando la integración del cliente con el servicio.
- Utilizar modelos predictivos para identificar **clientes con alto riesgo de churn** y aplicar campañas de retención personalizadas.

# Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)

