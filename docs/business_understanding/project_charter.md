# Project Charter

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
