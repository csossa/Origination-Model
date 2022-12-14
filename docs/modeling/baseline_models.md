# Baseline Model Report

_Baseline model is the the model a data scientist would train and evaluate quickly after he/she has the first (preliminary) feature set ready for the machine learning modeling. Through building the baseline model, the data scientist can have a quick assessment of the feasibility of the machine learning task._

> If using the Automated Modeling and Reporting tool, most of the sections below will be generated automatically from this tool. 

## Analytic Approach
* What is target definition
* Es la variable dependiente binaria  que puede tomar  dos posibles  valores, que se etiquetará  con 0 y 1.
* What are inputs (description)
* Es el conjunto de n variables independientes (𝑥1, 𝑥2, … , 𝑥𝑛) relacionadas con la información propia del solicitante, tomadas con el fin de explicar y/o predecir el valor de Y ( Dias_mora)
* What kind of model was built?
* Se construyó un modelo de regresión logística con el conjunto de datos de la entidad financiera para definir la precisión del modelo de scoring de originación. 

## Model Description

* Models and Parameters

	* Description or images of data flow graph
  		* if AzureML, link to:
    		* Training experiment
    		* Scoring workflow
	* What learner(s) were used?
	* Learner hyper-parameters


## Results (Model Performance)
* ROC/Lift charts, AUC, R^2, MAPE as appropriate
* Performance graphs for parameters sweeps if applicable

## Model Understanding

* Variable Importance (significance)

* Insight Derived from the Model

## Conclusion and Discussions for Next Steps

* Conclusion on Feasibility Assessment of the Machine Learning Task

* Discussion on Overfitting (If Applicable)

* What other Features Can Be Generated from the Current Data

* What other Relevant Data Sources Are Available to Help the Modeling
