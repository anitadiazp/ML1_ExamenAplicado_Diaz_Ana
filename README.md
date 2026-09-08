# Examen Aplicado - Machine Learning I

## Descripción del proyecto

Este proyecto desarrolla un análisis completo de Machine Learning utilizando el dataset **Online Shoppers Purchasing Intention**, disponible en UCI Machine Learning Repository.

El objetivo es analizar el comportamiento de navegación de los usuarios y construir modelos capaces de predecir si una sesión finalizará o no en una compra.

- **Dataset:** Online Shoppers Purchasing Intention
- **Fuente:** UCI Machine Learning Repository
- **URL:** https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset
- **Observaciones:** 12.330
- **Variables predictoras:** 17
- **Variable objetivo:** `Revenue`
- **Tipo de tarea:** Clasificación binaria

## Metodología

1. Exploración inicial y revisión de la estructura del dataset.
2. Análisis de valores faltantes y detección de outliers mediante IQR.
3. Análisis exploratorio de datos y estudio del balance de clases.
4. Preprocesamiento de variables numéricas, nominales y ordinales.
5. División estratificada en conjuntos de entrenamiento y prueba.
6. Reducción dimensional mediante PCA, conservando aproximadamente el 88,96% de la varianza con 11 componentes.
7. Análisis no supervisado mediante K-Means, seleccionando K=2 mediante inercia y Silhouette Score.
8. Entrenamiento y comparación de distintos modelos de clasificación mediante validación cruzada.
9. Optimización de hiperparámetros de los modelos seleccionados.
10. Evaluación final mediante Accuracy, Precision, Recall, F1-score macro, ROC-AUC y PR-AUC.

## Modelo seleccionado

El modelo final seleccionado fue **Random Forest**, debido a que presentó el mejor equilibrio entre las métricas evaluadas, obteniendo el mayor F1-score macro entre los modelos comparados.

| Métrica | Resultado |
|---|---:|
| Accuracy | 0.8792 |
| Precision | 0.5977 |
| Recall | 0.6728 |
| F1-score macro | 0.7803 |
| ROC-AUC | 0.9000 |
| PR-AUC | 0.6703 |

El modelo obtuvo además un F1-score macro de 0.8775 en entrenamiento y 0.7803 en prueba. El tiempo de inferencia para 2.466 observaciones fue aproximadamente 0.0690 segundos.

## Principales resultados

El análisis exploratorio mostró que `PageValues` presenta la asociación lineal más alta con `Revenue`. Otras variables relevantes incluyen `ExitRates`, `BounceRates`, `ProductRelated` y `ProductRelated_Duration`.

El análisis K-Means identificó dos grupos de sesiones de navegación, diferenciados principalmente por el nivel de interacción con el sitio, la duración en páginas relacionadas con productos y las tasas de abandono.

## Reproducir el análisis

Instalar las dependencias mediante:

`pip install -r requirements.txt`

Posteriormente, ejecutar el notebook `ExamenML.ipynb`.

## Video

Enlace al video de presentación: https://drive.google.com/file/d/10MJQVSFx1MciVmK-Smk3Uw5uwF8mDlAQ/view?usp=drive_link

**[AGREGAR ENLACE AL VIDEO]**

## Uso de inteligencia artificial generativa

Durante el desarrollo de este trabajo se utilizó ChatGPT como herramienta de apoyo para la comprensión de conceptos, revisión de código, resolución de errores y mejora de la redacción. Las decisiones metodológicas, ejecución del análisis, revisión de resultados e interpretación final fueron realizadas y verificadas por la autora.

## Autor

**Ana Díaz**
Ingeniería en Inteligencia Artificial
Machine Learning I
