# Baseline Model Report

_Baseline model is the the model a data scientist would train and evaluate quickly after he/she has the first (preliminary) feature set ready for the machine learning modeling. Through building the baseline model, the data scientist can have a quick assessment of the feasibility of the machine learning task._

> If using the Automated Modeling and Reporting tool, most of the sections below will be generated automatically from this tool. 

## Analytic Approach
* What is target definition

Es la variable dependiente binaria  que puede tomar  dos posibles  valores, que se etiquetará  con 0 y 1.

* What are inputs (description)

Es el conjunto de n variables independientes (𝑥1, 𝑥2, … , 𝑥𝑛) relacionadas con la información propia del solicitante, tomadas con el fin de explicar y/o predecir el valor de Y ( Max_mora)
 
* What kind of model was built?

Se construyó un modelo de regresión logística con el conjunto de datos de la entidad financiera para definir la precisión del modelo de scoring de originación. 

## Model Description

Para evaluar el modelo, se divide el dataset en dos partes. Se deja el 80% de los datos como datos de entrenamiento (train), y reservamos el 20% restando como datos de prueba (test). A continuación, se entrena el modelo de nuevo, pero ahora sólo con los datos de entrenamiento. Una vez entrenado el modelo, lo aplicamos a los datos reservados como «test», y calculamos las métricas precisión (Accurary) y exactitud (Precisión)


## Results (Model Performance)

![image](https://user-images.githubusercontent.com/111644646/207728820-cff3ff30-d5b5-48de-8817-87c5c18a7fb5.png)

## Model Understanding

* Variable Importance (significance)

 La Figura muestra la importancia de predictores de acuerdo con el modelo de regresión logística, se observa que la variable monto es el predictor que más pesa para determinar si se otorga una obligación a una solicitud de crédito.


## Conclusion and Discussions for Next Steps

* Conclusion on Feasibility Assessment of the Machine Learning Task

De acuerdo con el resultado obtenido en el accuaracy, se observa que el % de precisión del modelo no es suficiente para la producción y puesta en marcha. Por lo tanto, es necesario revisar y  estudiar otros modelos que se  mejoren la predicción.

![image](https://user-images.githubusercontent.com/111644646/207729070-5cc559fa-a5fd-4463-9d2c-8d7e6a9378b7.png)

A partir de los resultados expuestos, se comprueba que el modelo tiene un nivel predictivo del 57%

* Discussion on Overfitting (If Applicable)

* What other Features Can Be Generated from the Current Data

Otra caracteristica que podria predecir el modelo con los datos actuales sería el número de días en mora llegase a tener la futura obligación, con lo cual se realizarían agrupaciones de la variable máx-mora.

* What other Relevant Data Sources Are Available to Help the Modeling

Se puede construir información histórica a partir de otras variables que se encuentran dentro del formulario de solicitud de crédito del cliente. Adicionalmente, se pueden obtener características de comportamiento de pago registrados en los movimientos bancarios.
