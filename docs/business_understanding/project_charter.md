# Project Charter

dev
## Conocimiento del negocio
### ¿Quién es el cliente, y cuál es el dominio del cliente en el negocio?
El cliente es una entidad financiera que ofrece productos de ahorro y crédito a un segmento de clientes específico, la cual pertenece al sector solidario en Colombia
### ¿Qué problemas de negocio estamos tratando de abordar?

Evaluar el riesgo de crédito, es de gran importancia para una entidad financiera, pues busca evitar pérdidas que pueden estar relacionadas a cualquier tipo de decisión de concesión de crédito de forma inapropiada.
Para la entidad financiera es importante asegurar que el aumento en la aprobación de créditos, no se convierta luego en un aumento en los casos de morosidad de los consumidores ya que esto afecta de manera directa la rentabilidad de estas entidades.
Asimismo, es fundamental conocer con anticipación la máxima mora en que incurrirá una obligación, y poder tomar decisiones más objetivas y eficientes sobre el otorgamiento de crédito y sobre los términos que se establecerán para sus diferentes productos.
## Alcance
### ¿Qué soluciones de ciencia de datos estamos tratando de construir?
Se busca una solución que permita identificar a través de variables o características el posible default de una obligación financiera, para ello se 
La construcción de un modelo de Scoring de otorgamiento de crédito que, mediante el análisis de variables cualitativas y cuantitativas, base de datos facilitada por la entidad financiera, permita identificar posible default de una obligación y de esta manera se pretenda definir perfiles de clientes propensos al incumplimiento de sus obligaciones y de buen comportamiento.
El diseño del modelo debe tener en cuenta las exigencias de la norma, la cual dice que, para dicho fin, se debe realizar un análisis que relacione información cualitativa y cuantitativa de los clientes, que permita diferenciar un perfil de cliente sujeto de crédito y no apto para el otorgamiento.
### ¿Qué haremos?
Para ello se tomará información histórica del comportamiento de los créditos en el cual se contemplarán variables sociodemográficas del cliente, así como variables propias de la originación del crédito, tales como: el monto, el plazo, la modalidad, etc.
### ¿Cómo va a ser consumido por el cliente?
Se espera que esta solución sea consumida por el cliente a través de una aplicación ubicada en la red local de la organización y a través de una conexión directa al sistema de solicitudes de crédito en la entidad financiera.

## Personal
* Quienes están en este proyecto:
	* Microsoft:
		* PM
		* Científicos de datos.		
	* Cliente:
		* Administrador de datos
	
## Métricas
* ¿Cuáles son los objetivos cualitativos? (por ejemplo, reducir la rotación de usuarios)
El objetivo cualitativo busca minimizar el otorgamiento de créditos con una mayor probabilidad de incumplimiento según lo establecido en las políticas de creditos al interior de la entidad y normatividad 
* ¿Qué es una métrica cuantificable? (por ejemplo, reducir la fracción de usuarios con 4 semanas de inactividad)
* Cuantificar que mejoras en los valores de las métricas son útiles para el escenario del cliente  (e.g. reduce the fraction of users with 4-week inactivity by 20%) 
* ¿Cuál es el valor de referencia (actual) de la métrica? (por ejemplo, fracción actual de usuarios con 4 semanas de inactividad = 60 %)
* ¿Cómo mediremos la métrica? (e.g. A/B test on a specified subset for a specified period; or comparison of performance after implementation to baseline)

## Plan
* Fases, cronograma, breve descripción de lo que haremos en cada fase
## Arquitectura
* Datos

        * ¿Qué datos esperamos? Datos sin procesar en las fuentes de datos del cliente (por ejemplo, archivos locales, SQL, Hadoop local, etc.)
* Movimiento de datos desde local a Azure usando ADF u otras herramientas de movimiento de datos (Azcopy, EventHub, etc.) para mover cualquiera:
       * Todos los datos,
       * after some pre-aggregation on-prem,
       * Datos muestreados suficientes para el modelado
* Qué herramientas y recursos de análisis/almacenamiento de datos se utilizarán en la solución, por ejemplo,
  * ASA para agregación de secuencias
  * HDI/Hive/R/Python  para construcción,  agregación y muestreo de características.
  * AzureML para modelamiento y operacionalización del service web
El modelo será usado a través de una aplicacion web dentro de un servidor local que será consumido  a través de un API.
* How will the score or operationalized web service(s) (RRS and/or BES) be consumed in the business workflow of the customer? If applicable, write down pseudo code for the APIs of the web service calls.
Los datos de entrada registrados por el usuario para cada una de las variables predictoras serán preprocesadas antes de ser consumidos por el modelo. La conexión se realizará a través de un API que llevará los datos planos al servidor local para luego ser preprocesados.
  * ¿Cómo usará el cliente los resultados del modelo para tomar decisiones?
Se definiran politicas, a traves de las cuales se defina el apetito al riesgo  en corcondancia con el resultado del modelo y otras variables de analisis.
  
  * Haga un diagrama en 1 diapositiva mostrando el flujo de datos de extremo a extremo y la arquitectura de decisiones.
    * Si hay un cambio sustancial en el flujo de trabajo comercial del cliente, haga un diagrama antes  y después mostrando el flujo de datos.

## Communication
* ¿Cómo nos mantendremos en contacto? ¿Reuniones semanales?
Se realizarán reuniones a través de la metodología scrum, en la cual se contemplan reuniones diarias y metas a corto plazo. Igualmente la comunicación se realizará a través del Github frente al desarrollo del modelo que se plantea.
* ¿Quiénes son las personas de contacto en ambos lados?
Las personas de contacto son el cliente el PM y los cientificos de datos

## Business background
### ¿Quien es el cliente, y cual es el dominio del cliente en el negocio?
   El cliente es una entidad financiera que ofrece productos de ahorro y crédito a un segmento de clientes específico, la cual pertenece al sector solidario en Colombia.
  
### ¿Qué problemas de negocio estamos tratando de abordar? 
Evaluar el riesgo de crédito, es de gran importancia para una entidad financiera, pues busca evitar pérdidas que pueden estar relacionadas a cualquier tipo de decisión de concesión de crédito de forma inapropiada. 

Para la entidad financiera es importante asegurar que el aumento en la aprobación de créditos, no se convierta luego en un aumento en los casos de morosidad de los consumidores ya que esto afecta de manera directa la rentabilidad de estas entidades. 

Asimismo, es fundamental conocer con anticipación la máxima mora en que incurrirá una obligación, y poder tomar decisiones más objetivas y eficientes sobre el otorgamiento de crédito y sobre los términos que se establecerán para sus diferentes productos. 

Existe un área encargada de evaluar las solicitudes de crédito que hacen los clientes. Inicialmente deben recolectar información relevante que ayude a la toma de decisiones. Otro requisito es que toda la información que le den a la Entidad financiera debe ser verificable de alguna manera. Como proceso adicional, el equipo encargado confirma las referencias crediticias del cliente aspirante al crédito en plataformas como Datacrédito. Luego de este proceso una persona se encarga de consignar toda la información en una tabla de Excel donde todos pueden acceder a ella y posteriormente hacer una evaluación conjunta donde basados en ciertas métricas, deciden si el cliente tiene la capacidad de endeudamiento respecto al cupo y plazo de pago solicitado para finalmente denegar o aprobar el crédito. Muchas veces este proceso se vuelve engorroso y difícil de llevar a cabo ya que requiere un estudio muy detallado del cliente y de su caso puntual, lo cual conlleva a que las personas encargadas del proceso deban dedicar más tiempo del debido en esta actividad.

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
* Project Manager
* Científicos de datos
* Administrador de datos
	
## Metrics
### ¿Cuáles son los objetivos cualitativos? (e.g. reduce user churn)
El objetivo cualitativo busca minimizar el otorgamiento de créditos con una mayor probabilidad de incumplimiento según lo establecido en las políticas de créditos al interior de la entidad financiera y normatividad legal vigente.

Con ayuda de herramientas de software se propone utilizar los datos de los clientes que se ha recolectado para implementar un modelo de score crediticio, el cual se integre a su lógica de negocio y ayude a las personas encargadas de determinar la viabilidad del crédito, a tomar una decisión teniendo en cuenta los resultados que este modelo arroje.

### What is a quantifiable metric  (e.g. reduce the fraction of users with 4-week inactivity)
### Quantify what improvement in the values of the metrics are useful for the customer scenario (e.g. reduce the  fraction of users with 4-week inactivity by 20%) 
* Alcanzar un alto nivel de precisión en el xxx en las solicitudes de crédito a un xx% de confiabilidad.
* Aplicar un modelo  el cual presente resultados mínimos del 70 % de confiabilidad , que sirvan como una medida de confianza para toma de decisiones
* Alto impacto en la reducción de la cartera al contar con una predicción confiable del 70% de  la posibilidad de incurrir en mora una obligación.
* Implementar el modelo complementaría complementaría el estudio de crédito y mejoraría la cartera en un xx % aproximadamente, lo que impactaría directamente en el flujo de recursos disponibles de la entidad.

### What is the baseline (current) value of the metric? (e.g. current fraction of users with 4-week inactivity = 60%)
Actualmente el área de otorgamiento de crédito se demora xx días para el análisis de una solicitud de crédito  más de 15 minutos  y determinar si es viable su aprobación
### How will we measure the metric? (e.g. A/B test on a specified subset for a specified period; or comparison of performance after implementation to baseline)



## Plan
* Phases (milestones), timeline, short description of what we'll do in each phase.			
				
![image](https://user-images.githubusercontent.com/111644646/204054285-12a8d217-0a8d-4a7d-aa09-e738083d13c1.png)


## Architecture
### Datos
  ### ¿Qué datos esperamos? Datos sin procesar en las fuentes de datos del cliente
  * Esperamos datos tabulares desde dos fuentes un reporte en csv y datos desde SQL
  ### Movimiento de datos de local a Azure mediante ADF u otras herramientas de movimiento de datos
  * Inicialmente se espera transferir los datos desde AzCopy

### ¿Qué herramientas y recursos de análisis/almacenamiento de datos se utilizarán en la solución?
El modelo será usado a través de una aplicación web dentro de un servidor local que será consumido  a través de un API. 

  * Se usará Python para construcción, segmentación y muestreo de características
  * AzureML para modelado y operacionalización de servicios web

  
### ¿Cómo se consumirá la puntuación o el servicio web operacionalizado (RRS y/o BES) en el flujo de trabajo empresarial del cliente? Si procede, escriba el pseudocódigo de las API de las llamadas al servicio web.
Los datos de entrada registrados por el usuario para cada una de las variables predictoras serán preprocesadas antes de ser consumidos por el modelo. La conexión se realizará a través de un API que llevará los datos planos al servidor local para luego ser preprocesados. 

  *  ¿Cómo usará el cliente los resultados del modelo para tomar decisiones? 
Se definirán políticas, a través de las cuales se defina el apetito al riesgo en concordancia con el resultado del modelo y otras variables de análisis. 

  * Haga un diagrama en 1 diapositiva mostrando el flujo de datos de extremo a extremo y la arquitectura de decisiones.
    
    ![Diagram Model](https://user-images.githubusercontent.com/59837975/204069751-aab14c80-893f-45b3-a70c-973bdebcb025.jpg)

## Communication
### ¿Cómo nos mantendremos en contacto? ¿Reuniones semanales? 
Se realizarán sesiones a través de la metodología scrum, en la cual se contemplan reuniones diarias y metas a corto plazo. Igualmente la comunicación se realizará a través del Github frente al desarrollo del modelo que se plantea. 

### ¿Quiénes son las personas de contacto en ambos lados? 
Las personas de contacto son el cliente, el Project  Manager y los científicos de datos.
master
