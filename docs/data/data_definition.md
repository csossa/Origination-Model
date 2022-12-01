# Data and Feature Definitions

Este documento proporciona un eje central para las fuentes de datos sin procesar, los datos procesados/transformados y los conjuntos de funciones. Se proporcionan más detalles de cada conjunto de datos en el informe de resumen de datos.

Para cada dato, se proporciona un informe individual que describe el esquema de datos, el significado de cada campo de datos y otra información que es útil para comprender los datos. Si el conjunto de datos es el resultado de los conjuntos de datos existentes de procesamiento/transformación/ingeniería de características, también se proporcionan los nombres de los conjuntos de datos de entrada y los enlaces a los scripts que se utilizan para realizar la operación.

## Raw Data Sources

| Dataset Name | Original Location   | Destination Location  | Data Movement Tools / Scripts | Link to Report |
| ---:| ---: | ---: | ---: | -----: |
| Data Scoring Model |La ubicación original de la base de datos está en el core financiero de la entidad|El destino será través de una aplicación web dentro de un servidor local que será consumido  a través de un API|  | |

* Resumen data scoring model. Los datos contienen las características sociodemográficas de los usuarios o deudores así como las características de las obligaciones en términos de su estructuración. Todos los datos se cargan desde el servidosr local de la organización y se procesan a través de SQL.

## Processed Data
| Processed Dataset Name | Input Dataset(s)   | Data Processing Tools/Scripts | Link to Report |
| ---:| ---: | ---: | ---: | 
| Processed Dataset 1 | [Dataset1](link/to/dataset1/report), [Dataset2](link/to/dataset2/report) | [Python_Script1.py](link/to/python/script/file/in/Code) | [Processed Dataset 1 Report](link/to/report1)|

* En el procesamiento de los datos se realizaron las siguientes actividades: Eliminación de outlayers, en el cual, después del análisis exploratorio de los datos, se identificó observaciones que se encontraban fuera del rango para la variable estudiada; imputación de datos a través de la media del conjunto de datos para cada variable con datos faltantes; Agrupación por categorías de las variables que contienen pocas observaciones por cada categoría; y por último la codificación de las variables categóricas con el fin de que puedan ser entrenadas en el modelo.
