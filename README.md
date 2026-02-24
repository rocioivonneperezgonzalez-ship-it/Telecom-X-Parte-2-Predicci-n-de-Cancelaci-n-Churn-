# 📊 Telecom X -- Predicción de Cancelación de Clientes (Churn)

## 🚀 Descripción del Proyecto

Este proyecto desarrolla modelos de Machine Learning para predecir la
cancelación de clientes (Churn) en una empresa de telecomunicaciones.

El objetivo principal es identificar los factores más influyentes en la
cancelación y construir modelos predictivos comparables que permitan
evaluar desempeño, generalización y riesgo de overfitting.

------------------------------------------------------------------------

## 🎯 Objetivos

-   Analizar el comportamiento de cancelación de clientes.
-   Transformar variables categóricas y numéricas correctamente.
-   Implementar al menos dos modelos de clasificación.
-   Evaluar desempeño mediante métricas estándar.
-   Analizar críticamente resultados y comportamiento del modelo.

------------------------------------------------------------------------

## 🗂 Estructura del Proyecto

1.  **Carga y exploración de datos**
2.  **Limpieza y transformación**
    -   Codificación de variables categóricas
    -   Normalización de variables numéricas
3.  **Análisis exploratorio**
    -   Distribución de la variable objetivo
    -   Desbalance de clases
4.  **Separación de datos**
    -   70% entrenamiento
    -   30% prueba
    -   Estratificación por variable objetivo
5.  **Modelado**
    -   Regresión Logística
    -   Random Forest
6.  **Evaluación y comparación**
    -   Accuracy
    -   Precision
    -   Recall
    -   F1-score
    -   Matriz de confusión
    -   ROC-AUC
    -   Detección de overfitting

------------------------------------------------------------------------

## ⚙️ Tecnologías Utilizadas

-   Python
-   Pandas
-   NumPy
-   Scikit-learn
-   Matplotlib

------------------------------------------------------------------------

## 📈 Resultados Principales

### 🔹 Regresión Logística

-   Accuracy ≈ 0.80
-   ROC-AUC ≈ 0.84
-   Buen equilibrio entre sesgo y varianza
-   No presenta sobreajuste significativo

### 🔹 Random Forest

-   Accuracy ≈ 0.79
-   ROC-AUC ≈ 0.81
-   Presenta sobreajuste (Train Accuracy ≈ 0.99 vs Test ≈ 0.78)

📌 **Conclusión:** La Regresión Logística mostró mejor capacidad de
generalización.

------------------------------------------------------------------------

## 🔍 Variables Más Influyentes (Regresión Logística)

-   Tenure (negativamente asociada al churn)
-   InternetService_Fiber optic
-   Contract_Month-to-month
-   PaperlessBilling_Yes
-   ChargesMonthly

Estos resultados sugieren que los contratos mensuales y ciertos tipos de
servicio incrementan la probabilidad de cancelación.

------------------------------------------------------------------------

## 🧠 Análisis Crítico

-   El dataset presenta desbalance de clases (\~73% no churn vs \~27%
    churn).
-   Random Forest muestra sobreajuste debido a alta complejidad.
-   La Regresión Logística ofrece mayor estabilidad y mejor
    interpretación.

------------------------------------------------------------------------

## 📌 Posibles Mejoras

-   Aplicar validación cruzada.
-   Ajustar hiperparámetros con GridSearchCV.
-   Manejar desbalance con técnicas como SMOTE.
-   Evaluar modelos adicionales (XGBoost, Gradient Boosting).
-   Ajustar umbral de decisión para optimizar recall.

------------------------------------------------------------------------

## 👩🏻‍🔬 Autora

Ing. Rocío Ivonne Pérez González\
Maestría en Ciencias y Tecnologías Biomédicas

------------------------------------------------------------------------

## 📄 Licencia

Proyecto con fines académicos y de portafolio profesional.
