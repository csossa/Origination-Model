# Deployment

In this folder you can add deployment documentation, including

Se realiza un despliegue del modelo XGBoost a través de la herramienta MLFlow y la función log_model
lo cual generó un paquete que contiene el artefacto del modelo entrenado.

En relación a la utilización desde el usuario final, que para el caso práctico de este proyecto, es el análista de crédito, utilizará una herramienta de Office 365,
llamada PowerApps en la cual se inlcluyen las caracteristicas que seran datos de entrada para el modelo. Entre las cuales se encuentran:

['Monto',
 'Edad',
 'Personas a cargo',
 '#Creditos',
 'Monto sobre ingresos',
 'Cuota',
 'Plazo_1',
 'Sueldo_1',
 'Ingresos mes_1',
 'Egresos mes_1',
 'Aportes_1',
 'Estrato_1',
 'Modalidad_1',
 'Garantia_1',
 'Linea_1',
 'Forma pago_1',
 'Género_1',
 'Estado civil_1',
 'Profesión_1',
 'Tipo vivienda_1',
 'Ocupación_1',
 'Escolaridad_1']
 
 Asimismo, se relaciona el contenido del modelo con el cual se realiza la implementación y despliegue del paquete. Junto con la importancia de las características 
 tenidas en cuenta en el entrenamiento del modelo.
 
 ![image](https://user-images.githubusercontent.com/59837975/208200120-3529195d-6322-4e65-80bb-e0b08161da75.png)

El uso final de la aplicación se realiza entre las siguientes funciones que contemplan el preprocesamiento y la generación de la predicción.

![image](https://user-images.githubusercontent.com/59837975/208200457-eaae9bca-ec39-4b48-b4ec-64799ad2c83d.png)
![image](https://user-images.githubusercontent.com/59837975/208200510-0a53f98b-2173-48e6-8103-45ba79b0dfe2.png)

![image](https://user-images.githubusercontent.com/59837975/208200580-b9ab6dd0-4240-4d75-b9c7-5ed77a52830e.png)


