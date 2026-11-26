# Modelo de aprobación de tarjetas de crédito

## Descripción de lo que hace el programa
Este proyecto desarrolla un modelo de Machine Learning de **Regresión Logística** integrado en un `Pipeline` de `scikit-learn` para predecir si una solicitud de tarjeta de crédito será rechazada (`1`) o aprobada (`0`) a partir de los datos personales y socioeconómicos del solicitante.

El cuaderno `tarjetas_credito_carlos_ovies.ipynb` descarga el dataset **Credit Card Details** de Kaggle (`Credit_card.csv` y `Credit_card_label.csv`) y cubre las siguientes fases:
* Carga, unión de tablas y control de duplicados.
* Análisis razonado de valores nulos y limpieza de variables.
* Codificación de variables categóricas (incluyendo `TargetEncoder`).
* División estratificada en entrenamiento (80%) y test (20%).
* Construcción del `Pipeline` completo, tratamiento del desbalance de clases y comparación con `DummyClassifier`.
* Evaluación con métricas de clasificación, matriz de confusión y conclusiones de negocio.

## Guía de instalación paso a paso
1. Clona el repositorio y entra en la carpeta de este proyecto:
   ```bash
   git clone [https://github.com/carlosOvies-dev/Sistemas_Aprendizaje_Automatico.git](https://github.com/carlosOvies-dev/Sistemas_Aprendizaje_Automatico.git)
   cd Sistemas_Aprendizaje_Automatico/02_tarjetas_credito
   ```
2. Crea el entorno virtual e instala todas las dependencias con `uv`:
   ```bash
   uv sync
   ```
3. Abre `tarjetas_credito_carlos_ovies.ipynb` en VS Code, selecciona el entorno de Python `.venv` de esta carpeta y ejecuta las celdas en orden. Los datos se descargan automáticamente con `kagglehub`.