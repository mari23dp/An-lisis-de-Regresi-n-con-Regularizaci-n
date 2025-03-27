# Análisis de Regresión con Regularización (Ridge, Lasso, Elastic Net)

**Autores: Mariana Diaz Puentes y Fernando Lizarazo**

Este repositorio contiene un análisis de regresión utilizando el lenguaje **R**, implementando tres técnicas avanzadas de regularización: **Ridge**, **Lasso** y **Elastic Net**. Estas técnicas se utilizan para mejorar el rendimiento del modelo de regresión y evitar el sobreajuste, lo que permite generalizar mejor a nuevos datos.

## Descripción

En este proyecto, se aplicaron los siguientes métodos de regularización para modelar y predecir la relación entre las variables en el conjunto de datos:

- **Ridge Regression**: Regularización L2 que penaliza los coeficientes al añadir un término de penalización basado en la suma de los cuadrados de los coeficientes.
- **Lasso Regression**: Regularización L1 que penaliza los coeficientes añadiendo un término de penalización basado en la suma de los valores absolutos de los coeficientes. Esto puede llevar a que algunos coeficientes sean exactamente cero, lo que realiza una selección automática de características.
- **Elastic Net**: Una combinación de las regularizaciones L1 y L2, que permite controlar la mezcla de las penalizaciones de Lasso y Ridge mediante el parámetro `alpha`.

El cuaderno de Jupyter implementa estos tres enfoques y compara su rendimiento en términos de **RMSE** (Root Mean Square Error) y **R²**. Además, se visualizan las trayectorias de los coeficientes de cada modelo a medida que varía el parámetro de regularización `lambda`.

## Lo que hice

El análisis realizado incluye los siguientes pasos:

### 1. Preparación de los datos

Se cargan los datos de los préstamos (`loan_data_train`) y se realiza una limpieza preliminar para asegurar que los datos estén listos para el análisis.

### 2. Modelo de regresión lineal simple

Primero, se construye un modelo de regresión lineal sin regularización utilizando el conjunto de entrenamiento `loan_data_train`. Se evalúa el modelo utilizando las métricas **RMSE** y **R²** para observar el desempeño sin regularización.

### 3. Modelos con regularización

Luego, se aplican tres tipos de regularización (Ridge, Lasso y Elastic Net) sobre el mismo conjunto de datos (`loan_data_train`). Cada uno de estos modelos se ajusta utilizando una penalización controlada por el parámetro `lambda` y el parámetro `alpha` para Elastic Net.

### 4. Evaluación de modelos

Después de ajustar los modelos, se calculan las métricas **RMSE** y **R²** para los modelos regularizados y se comparan con el modelo de regresión lineal sin regularización. Esto permite ver cómo la regularización afecta al rendimiento del modelo.

### 5. Visualización de resultados

Se visualizan las trayectorias de los coeficientes de cada modelo a medida que varía el parámetro de regularización `lambda`, lo que permite analizar cómo cambian los coeficientes a medida que se aplica la regularización.

## Comparación de Modelos

Se comparan los siguientes modelos:

- **Modelo de regresión lineal sin regularización**: Basado en la regresión estándar.
- **Modelo Ridge**: Con regularización L2.
- **Modelo Lasso**: Con regularización L1.
- **Modelo Elastic Net**: Combinación de Lasso y Ridge, controlado por el parámetro `alpha`.

Para cada modelo, se calcula y compara el **RMSE** y **R²** en el conjunto de prueba. Los resultados son presentados de manera que se pueda evaluar la efectividad de cada técnica.

## Requisitos

Para ejecutar este proyecto, necesitarás tener **R** y las siguientes bibliotecas instaladas:

- **R** (versión recomendada: 4.x)
- `glmnet` (para la regresión regularizada, puedes instalarlo con `install.packages("glmnet")`)
- `caret` (para evaluar el rendimiento del modelo)
- `dplyr` (para la manipulación de datos)

## Estructura del Proyecto

El proyecto contiene el siguiente archivo principal:

- **Taller_5_Final.ipynb**: Jupyter notebook que contiene el código fuente y los resultados obtenidos durante el análisis.

