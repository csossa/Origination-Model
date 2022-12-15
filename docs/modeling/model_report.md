# Final Model Report
_Report describing the final model to be delivered - typically comprised of one or more of the models built during the life of the project_

## Analytic Approach
What is target definition 

Es la variable dependiente binaria que puede tomar dos posibles valores, que se etiquetará con 0 y 1.

What are inputs (description) 

Es el conjunto de n variables independientes (𝑥1, 𝑥2, … , 𝑥𝑛) relacionadas con la información propia del solicitante, tomadas con el fin de explicar y/o predecir el valor de Y ( Max_mora)

What kind of model was built? 

Se construyó un modelo xgboost con el conjunto de datos de la entidad financiera para definir la precisión del modelo de scoring de originación.

## Solution Description

Se construyó un modelo xgboots, el cual posee tres elementos principales: Una función de pérdida a optimizar, un algoritmo de aprendizaje débil para realizar las predicciones y un modelo aditivo para añadir los algoritmos de aprendizaje débiles que minimizan la función de pérdida.

## Data

En el siguiente link se encuentra la fuente, descripción, esquema de datos y estadísticas.

https://github.com/csossa/Origination-Model/blob/master/docs/data/data_summary.md

## Features
* List of raw and derived features 

![image](https://user-images.githubusercontent.com/111644646/207732596-c7a12be2-c89b-46e0-87eb-df00cb73288c.png)

* Importance ranking.
La Figura muestra la importancia de predictores de acuerdo con el modelo XGBoost, donde se observa que “monto” es también el predictor que más pesa para determinar si se otorga una obligación a una solicitud de crédito.

![image](https://user-images.githubusercontent.com/111644646/207732118-ffcd54fb-154a-4a1e-9b44-2d6eb5c59571.png)


## Algorithm
En la siguiente imagen se describe el flujo de datos:

![image](https://user-images.githubusercontent.com/111644646/207741743-d684c7fa-cbe7-45a3-9ec1-6166b97479ba.png)


## Results
Se entrena un modelo XGBoost que logra un accuracy de 90 %

![image](https://user-images.githubusercontent.com/111644646/207730439-d7fb8f28-a231-49bc-8fb3-2cfd23e5d483.png)

El modelo  que tuvo mayor precisión fue XGBoost seguido del Random Forest ,regresión logística, y por último perceptrón multicapa.
