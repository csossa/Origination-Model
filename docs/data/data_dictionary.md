# Data Dictionary

# Database " Data"


![UML Diagram](/file/uml/database1)

La base de datos que se utilizará para el trabajo contiene el histórico de seguimiento de créditos de 3.336 clientes, correspondiente al periodo 2009 - 2022, donde se identificaron 28 variables con relación a cada registro de clientes de la entidad financiera. 

## Table 1
La Tabla 1 muestra las variables que se usaron en el modelo, en total son 27 variables independientes y  1 variable dependiente Max_mora

| column | type | description |
| --- | --- | --- |
| #Obligación 	| Object | Número interno que identifica el crédito o la obligación| 
| Modalidad	| Object | número que agrupa el tipo de cartera (comercial, vivienda, consumo) | 
| Garantia 	| Object | tipo de garantía que respalda el crédito | 
| Linea 	| Object | Subdivisión de la modalidad del crédito con origen específico | 
| Forma pago 	| Object |Puede ser ventanilla o nómina| 
| Género 	| Object|Sexo del cliente | 
| Estado civil 	| Object | Puede ser soltero, casado, viudo etc. | 
| Madre cabeza familia 	| Object | Mujer que tiene a cargo exclusivo la responsabilidad económica del hogar | 
| Profesión	| Object | código de la profesión del cliente | 
| Tipo vivienda 	| Object | Puede ser vivienda propia, arrendada, familiar | 
| Ocupación	| Object | Actividad económica en la que se agrupa el deudor | 
| Tipo contrato 	| Object | Pueder ser obra o labor, término indefinido, término fijo, etc | 
| Escolaridad 	| Object | Nivel de estudios del deudor (bachiller, universitaria, especialista, Magister | 
| Monto 	| int64 | Es el volumen del préstamo concedido | 
| Reestructurado| int64 | según el comportamiento del cliente, el crédito ha tenido que ser modificado en sus condiciones iniciales, para asegurar que éste cumpla con las obligaciones financieras.  | 
| Edad 	| int64| Años de vida del cliente| 
| Personas a cargo 	| int64 | Número de personas que dependen económicamente del cliente | 
| #Creditos	| Int64 | Cantidad de créditos otorgados al cliente | 
| Cuota 	| Int64| Abono periódico en el que se responsabilizan el deudor y el acreedor con el objetivo de devolver el financiamiento que le fue otorgado | 
| Max_mora	| Int64| Número de días en el cual la entidad financiera considerará que entra en mora o en incumplimiento la obligación | 
| Plazo	| float64 | El tiempo establecido en el cual el cliente va a pagar la deuda | 
| Estrato 	| Float64 | Estrato socioeconómico del cliente que se ubica de 1 a 6 | 
| Sueldo 	| Float64 | Ingreso mensual percibido por la ocupación o actividad principal del deudor| 
| Ingresos mes 	| Float64| Agrupa todos los ingresos percibidos por el deudor en un mes en promedio | 
| Egresos mes 	| Float64| Agrupa todos los gastos percibidos por el deudor en un mes promedio | 
| Flujo neto 	| Float64| Remanente de los ingresos menos los egresos | 
| Monto sobre ingresos 	| Float64 | Relación del valor del monto del prestado sobre los ingresos mes | 
| Cuota sobre ingresos 	| Float64 | Relación de la cuota pactada en el crédito sobre los ingresos mes | 
| Aportes 	| Float64 | Ahorros que tiene el cliente por concepto de la permanencia en la sociedad | 
