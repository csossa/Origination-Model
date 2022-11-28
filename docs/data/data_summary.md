# Data Report

En este documento se observan los resultados del análisis exploratorio de los datos para el modelo de originación. El tamaño de la matriz es de (79276, 29) el cual contiene 79.276 observaciones y 29 características.

## General summary of the data
 El número de características del tipo Objet es de 13, del tipo float64 son 9 y del tipo int64 son 7. La siguiente tabla resume la descripción de cada una de las características observadas en la base de datos.
 
 ![image](https://user-images.githubusercontent.com/59837975/204335005-1d51f8f8-bfa6-43bc-abc8-ac8e4556c2ec.png)


## Data quality summary

En la siguiente gráfica se puede observar las variables con valores ausentes:

![image](https://user-images.githubusercontent.com/59837975/204337488-a1ab3842-c7ba-4e22-ac5d-c56bd02cee69.png)

Asímismo, se observa el porcentaje de los datos faltantes por cada una de las variables.

![image](https://user-images.githubusercontent.com/59837975/204339111-355380b1-346c-47b7-b2bc-0f14d2c8cc20.png)

Igualmente, se realiza un análisis estadístico de las variables númericas, en la cual se muestra la descripción frente al número de datos, la media, desviación estandar, mínimo, máximo, entre otros.

![image](https://user-images.githubusercontent.com/59837975/204338730-8ad03a25-b1bb-4a01-a863-6fd2bbb96465.png)

## Target variable
Construimos una gráfica con la distribución de la variable objetivo para identificar el número de datos con la etiqueta 1 y la cantidad de datos con etiqueta cero (0). Logrando así identificar que existe un desbalanceo frente a la variables puesta, de la cual se observa un número mayor de observaciones para la etiqueta cerp (0). En la siguiente gráfica se observa lo anteriomente mencionado:

![image](https://user-images.githubusercontent.com/59837975/204341208-5098bf5b-5f1e-4cd3-b722-ca3f4950d378.png)

## Individual variables
Se realiza un análisis de cada una de las variables númericas y categóricas en cuanto a su distribución frente a la totalidad de los datos y se realizan una depuración frente a datos outlayer.
### Variables núméricas
![image](https://user-images.githubusercontent.com/59837975/204339741-87a1a7cd-fb40-427a-b286-2ee5514b0cae.png)

### Variables categóricas
![image](https://user-images.githubusercontent.com/59837975/204339972-0eae89a9-9bcc-4b0a-9b78-1adb78962437.png)

Para las variables categóricas se realiza un método de ajuste por categoría.

![image](https://user-images.githubusercontent.com/59837975/204340083-6c85dea8-ebbb-47d7-b6ce-aeffd050528c.png)

## Variable ranking

Una vez analizados los datos se penalizan algunas variables por la representatividad frente a los datos totales. En la siguiente tabla se observan las variables que se eligen con base en el análisi exploratorio realizado.

![image](https://user-images.githubusercontent.com/59837975/204340555-ce73319a-6a7a-4324-97aa-590801578e38.png)

## Relationship between explanatory variables and target variable

En la siguiente gráfica se encuentra la correlación de las variables numéricas y la variable respuesta.
![image](https://user-images.githubusercontent.com/59837975/204340685-e75dbc38-a691-48d0-aa0b-1fa3ef6b2105.png)

Asmímismo, se observa la maríz de correlaciones entre las variables núméricas.
![image](https://user-images.githubusercontent.com/59837975/204340811-8efb2a25-d606-49ef-99da-7f18e9d26b4f.png)

Por otra parte, se analiza la correlación entre la variable respuesta y las variables categóricas.
![image](https://user-images.githubusercontent.com/59837975/204340971-6f02478d-5826-41ea-9fa6-14ebbff4cbb1.png)
