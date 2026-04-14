# Verificación de Edad mediante Visión Artificial

## Descripción del Proyecto

La cadena de supermercados Good Seed busca cumplir con las leyes que prohíben la venta de alcohol a menores de edad. Para ello, este proyecto evalúa el uso de ciencia de datos y visión artificial para estimar la edad de los clientes a partir de imágenes capturadas en el área de pago.

Las tiendas cuentan con cámaras que se activan al momento de comprar alcohol. A partir de estas imágenes, se pretende construir un modelo que permita verificar automáticamente la edad de una persona.

## Objetivo

Desarrollar y evaluar un modelo de aprendizaje profundo capaz de estimar la edad de una persona a partir de imágenes faciales, con el fin de apoyar la validación de edad en puntos de venta.

## Descarga del dataset:

https://www.kaggle.com/c/imagenet-object-localization-challenge/data

## Nota:

Este dataset no está enfocado exclusivamente en rostros, pero contiene imágenes de objetos naturales, incluyendo un subconjunto de rostros. Esto permite su uso parcial en tareas relacionadas con estimación de edad.

# Metodología

1. Análisis Exploratorio de Datos (EDA)

- Inspección de imágenes
- Distribución de edades
- Detección de posibles sesgos o desbalance

2. Preprocesamiento

- Redimensionamiento de imágenes
- Normalización
- División en conjuntos de entrenamiento y validación

3. Modelado
   Se utilizó una red neuronal convolucional basada en:

- ResNet50 con pesos preentrenados en ImageNet (weights='imagenet')

Esto permite aprovechar características previamente aprendidas en imágenes generales.

4. Entrenamiento

- Ejecutado en GPU
- Ajuste de hiperparámetros
- Fine-tuning de la red

5. Evaluación

- Métrica principal: MAE (Mean Absolute Error)
- Función de pérdida: MSE (Mean Squared Error)

### Nota:

- MSE permite un entrenamiento más rápido
- MAE se usa como métrica final de evaluación

Es normal que modelos profundos presenten overfitting, siempre que el rendimiento en validación sea adecuado.

El uso de modelos de visión artificial permite estimar la edad con un grado razonable de precisión, lo que puede ser útil como herramienta de apoyo en la verificación de edad en supermercados.

Sin embargo:

- La calidad del dataset influye significativamente en el desempeño
- Modelos más especializados en rostros podrían mejorar los resultados
- Es recomendable complementar este sistema con otros métodos de verificación

