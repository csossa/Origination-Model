# Project Charter

## Business background
### ¿Quien es el cliente, y cual es el dominio del cliente en el negocio?
   El cliente es una entidad financiera que ofrece productos de ahorro y crédito a un segmento de clientes específico, la cual pertenece al sector solidario en Colombia.
  
### ¿Qué problemas de negocio estamos tratando de abordar? 
Evaluar el riesgo de crédito, es de gran importancia para una entidad financiera, pues busca evitar pérdidas que pueden estar relacionadas a cualquier tipo de decisión de concesión de crédito de forma inapropiada. 

Para la entidad financiera es importante asegurar que el aumento en la aprobación de créditos, no se convierta luego en un aumento en los casos de morosidad de los consumidores ya que esto afecta de manera directa la rentabilidad de estas entidades. 

Asimismo, es fundamental conocer con anticipación la máxima mora en que incurrirá una obligación, y poder tomar decisiones más objetivas y eficientes sobre el otorgamiento de crédito y sobre los términos que se establecerán para sus diferentes productos. 

## Scope
### ¿Cuál solución de ciencia de datos se desea realizar?
La construcción de un modelo de Scoring de otorgamiento de crédito que, mediante el análisis de variables cualitativas y cuantitativas, base de datos facilitada por la entidad financiera, permita identificar posible default de una obligación y de esta manera se pretenda definir perfiles de clientes propensos al incumplimiento de sus obligaciones y de buen comportamiento. 

El diseño del modelo debe tener en cuenta las exigencias de la norma, la cual dice que, para dicho fin, se debe realizar un análisis que relacione información cualitativa y cuantitativa de los clientes, que permita diferenciar un perfil de cliente sujeto de crédito y no apto para el otorgamiento.

### ¿Qué haremos? 
Para ello se tomará información histórica del comportamiento de los créditos en el cual se contemplarán variables sociodemográficas del cliente, así como variables propias de la originación del crédito, tales como: el monto, el plazo, la modalidad, etc. 

### ¿Cómo va a ser consumido por el cliente? 
Se espera que esta solución sea consumida por el cliente a través de una aplicación ubicada en la red local de la organización y a través de una conexión directa al sistema de solicitudes de crédito en la entidad financiera. 

## Personnel
### ¿Quiénes están en este proyecto?
	* Microsoft:
		
		* Project Manager
		* Científicos de datos
		* Account manager
	* Client:
		* Administrador de datos
	
## Metrics
* What are the qualitative objectives? (e.g. reduce user churn)
* What is a quantifiable metric  (e.g. reduce the fraction of users with 4-week inactivity)
* Quantify what improvement in the values of the metrics are useful for the customer scenario (e.g. reduce the  fraction of users with 4-week inactivity by 20%) 
* What is the baseline (current) value of the metric? (e.g. current fraction of users with 4-week inactivity = 60%)
* How will we measure the metric? (e.g. A/B test on a specified subset for a specified period; or comparison of performance after implementation to baseline)

## Plan
* Phases (milestones), timeline, short description of what we'll do in each phase.

## Architecture
* Data
  * What data do we expect? Raw data in the customer data sources (e.g. on-prem files, SQL, on-prem Hadoop etc.)
* Data movement from on-prem to Azure using ADF or other data movement tools (Azcopy, EventHub etc.) to move either
  * all the data, 
  * after some pre-aggregation on-prem,
  * Sampled data enough for modeling 

* What tools and data storage/analytics resources will be used in the solution e.g.,
  * ASA for stream aggregation
  * HDI/Hive/R/Python for feature construction, aggregation and sampling
  * AzureML for modeling and web service operationalization
* How will the score or operationalized web service(s) (RRS and/or BES) be consumed in the business workflow of the customer? If applicable, write down pseudo code for the APIs of the web service calls.
  * How will the customer use the model results to make decisions
  * Data movement pipeline in production
  * Make a 1 slide diagram showing the end to end data flow and decision architecture
    * If there is a substantial change in the customer's business workflow, make a before/after diagram showing the data flow.

## Communication
* How will we keep in touch? Weekly meetings?
* Who are the contact persons on both sides?
