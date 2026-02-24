# 📊 Telecom X -- Parte 2: Predicción de Cancelación (Churn)

Proyecto Final -- **Alura Latam \| Cursos Online de Tecnología**\
Programa: **Oracle ONE - México 9**

------------------------------------------------------------------------

## 🎯 Propósito del Proyecto

El objetivo principal de este proyecto es desarrollar modelos
predictivos capaces de **predecir la cancelación (churn) de clientes**
en la empresa Telecom X, utilizando variables demográficas,
contractuales y de consumo.

La finalidad estratégica es anticipar la pérdida de clientes para
permitir a la empresa implementar acciones de retención basadas en
datos.

------------------------------------------------------------------------

## 🧠 Objetivo Analítico

-   Identificar los factores más influyentes en la cancelación.
-   Construir al menos dos modelos de clasificación.
-   Comparar el desempeño de los modelos.
-   Generar insights estratégicos para la toma de decisiones.

------------------------------------------------------------------------

## 📁 Estructura del Proyecto

    Telecom-Churn/
    │
    ├── Telecom_X_Parte_2.ipynb        # Cuaderno principal con todo el análisis
    ├── datos_tratados_ingles.csv             # Dataset limpio y preparado
    ├── visualizaciones/               # Carpeta opcional con gráficos exportados
    └── README.md                      # Documentación del proyecto

------------------------------------------------------------------------

## 🛠 Preparación de los Datos

### 1️⃣ Clasificación de Variables

Las variables fueron clasificadas en:

-   **Variables categóricas**: tipo de contrato, método de pago,
    servicios contratados, etc.
-   **Variables numéricas**: tenure, MonthlyCharges, TotalCharges.

------------------------------------------------------------------------

### 2️⃣ Transformación de Variables

#### 🔹 Codificación de Variables Categóricas

Se utilizó **One-Hot Encoding** para convertir variables categóricas en
variables numéricas binarias, permitiendo su uso en algoritmos de
Machine Learning.

#### 🔹 Transformación de la Variable Objetivo

La variable `Churn` fue transformada a formato binario:

-   0 → No canceló
-   1 → Sí canceló

------------------------------------------------------------------------

### 3️⃣ Separación en Entrenamiento y Prueba

Se utilizó una división:

-   **70% entrenamiento**
-   **30% prueba**

Aplicando `stratify=y` para mantener la proporción original de
cancelación (\~26.5%).

------------------------------------------------------------------------

### 4️⃣ Normalización

Se aplicó **StandardScaler** únicamente para modelos sensibles a la
escala (Regresión Logística).

No se aplicó normalización para modelos basados en árboles (Random
Forest), ya que no son sensibles a la escala de los datos.

------------------------------------------------------------------------

## 🤖 Modelos Implementados

### 🔹 Modelo 1: Regresión Logística

-   Requiere normalización
-   Interpretabilidad mediante coeficientes

### 🔹 Modelo 2: Random Forest

-   Modelo basado en árboles
-   No requiere normalización
-   Permite analizar importancia de variables

------------------------------------------------------------------------

## 📈 Métricas de Evaluación

Se evaluaron ambos modelos utilizando:

-   Accuracy
-   Precision
-   Recall
-   F1-score
-   Matriz de Confusión
-   ROC-AUC

Se realizó además análisis de:

-   Overfitting (comparación train vs test)
-   Underfitting
-   Capacidad de generalización

------------------------------------------------------------------------

## 🔎 Insights Relevantes del EDA

Algunos hallazgos importantes:

-   Clientes con contrato **Month-to-Month** presentan mayor
    probabilidad de cancelación.
-   El servicio **Fiber Optic** está fuertemente asociado al churn.
-   Menor antigüedad (tenure) aumenta significativamente el riesgo de
    cancelación.
-   Clientes con débito automático tienden a cancelar menos.

Estos hallazgos permiten diseñar estrategias específicas de retención.

------------------------------------------------------------------------

## 🚀 Cómo Ejecutar el Proyecto

### 1️⃣ Requisitos

Instalar las siguientes librerías:

``` bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 2️⃣ Ejecutar el Notebook

1.  Abrir el archivo `Telecom_X_Parte_2.ipynb` en Jupyter Notebook o
    Google Colab.
2.  Cargar el dataset tratado (`datos_tratados.csv`).
3.  Ejecutar las celdas en orden secuencial.

------------------------------------------------------------------------

## 📌 Conclusión Estratégica

El modelo de Regresión Logística mostró mejor equilibrio entre
interpretación y desempeño, mientras que Random Forest presentó indicios
de overfitting.

Los principales factores asociados a la cancelación son:

-   Tipo de contrato
-   Tipo de servicio de internet
-   Antigüedad del cliente
-   Método de pago

Este proyecto demuestra cómo aplicar un pipeline completo de Machine
Learning orientado a negocio, integrando análisis exploratorio, modelado
predictivo e interpretación estratégica.

------------------------------------------------------------------------

## 👩‍💻 Autor

Proyecto desarrollado como trabajo final del curso:

**Alura Latam -- Oracle ONE México 9**
