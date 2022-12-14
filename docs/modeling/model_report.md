# Final Model Report
_Report describing the final model to be delivered - typically comprised of one or more of the models built during the life of the project_

## Analytic Approach
* What is target definition
* What are inputs (description)
* What kind of model was built?

## Solution Description

Se construyó un modelo xgboots, el cual posee tres elementos principales: Una función de pérdida a optimizar, un algoritmo de aprendizaje débil para realizar las predicciones y un modelo aditivo para añadir los algoritmos de aprendizaje débiles que minimizan la función de pérdida.

## Data
* Source
* Data Schema
* Sampling
* Selection (dates, segments)
* Stats (counts)

## Features
* List of raw and derived features 
* Importance ranking.

## Algorithm
* Description or images of data flow graph
  * if AzureML, link to:
    * Training experiment
    * Scoring workflow
* What learner(s) were used?
* Learner hyper-parameters

## Results
* ROC/Lift charts, AUC, R^2, MAPE as appropriate
* Performance graphs for parameters sweeps if applicable
