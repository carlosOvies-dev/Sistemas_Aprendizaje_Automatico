# Modelo de aprobación de tarjetas de crédito

## Objetivo
Desarrollar un modelo de Machine Learning con `scikit-learn` (Regresión Logística integrada en un `Pipeline`) capaz de predecir si una solicitud de tarjeta de crédito será rechazada o aprobada a partir de datos personales y socioeconómicos del solicitante.

## Dataset
Se utiliza el conjunto de datos **Credit Card Details** de Kaggle, dividido en dos archivos:
* `Credit_card.csv`: información del cliente identificada por `Ind_ID`.
* `Credit_card_label.csv`: variable objetivo `label` (`0` = aprobada, `1` = rechazada).

## Flujo de trabajo
1. Carga, unión de tablas y control de duplicados.
2. Análisis de valores nulos y limpieza de variables.
3. Codificación de variables categóricas (incluyendo Target Encoding).
4. División estratificada en entrenamiento (80%) y test (20%).
5. Construcción y entrenamiento del `Pipeline` completo.
6. Tratamiento del desbalance de clases y comparación con modelo base (`DummyClassifier`).
7. Evaluación con métricas de clasificación y matriz de confusión.