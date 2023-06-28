# Analisis de EEFF
Utilización de herramientas de extracción y transformación de datos para análisis de Estado de Resultados

Título del Proyecto: Análisis de Financieros
Resumen:
El objetivo de este proyecto es aprovechar el poder del análisis de datos para mejorar la eficiencia operativa y respaldar la toma de decisiones estratégicas en la empresa el pato azul. Mediante el análisis de conjuntos de datos internos financieros relevantes, se busca identificar patrones, tendencias y relaciones ocultas que puedan proporcionar información valiosa para mejorar la eficiencia, optimizar los procesos y brindar una ventaja competitiva.

Objetivos del Proyecto:

1.	Recopilar, limpiar y estructurar los datos relevantes disponibles en la empresa, incluyendo fuentes internas y externas pertinentes.
2.	Realizar un análisis exploratorio de los datos para identificar patrones, correlaciones y tendencias significativas.
3.	Diseñar paneles interactivos y visualizaciones claras para presentar los resultados del análisis de manera comprensible y accesible para los diferentes equipos y niveles de la organización.
4.	Realizar el estado de resultados financieros del 01 de enero al 31 de diciembre del 2020
5.	Proponer recomendaciones concretas basadas en los resultados del análisis para mejorar la eficiencia operativa, reducir costos, optimizar los recursos y respaldar la toma de decisiones estratégicas.

Entregables Esperados:

1.	Un conjunto de datos limpios, estructurados y preparados para el análisis en excel.
2.	Informes y visualizaciones que presenten los hallazgos y recomendaciones de manera clara y concisa que respondan las siguientes preguntas;
a.	El top 5 de costos de venta más elevados
b.	Top 10 de gastos Operativos 
c.	Que 5 meses son en los que más se vendieron. 
d.	Que 2 meses son en los que menos se vendieron.

3.	Estado de resultados.
4.	Recomendaciones concretas y accionables para mejorar la eficiencia operativa y respaldar la toma de decisiones.
5.	Subir este análisis a su cuenta de GitHub 

Recursos Necesarios:
1)	Exel
2)	Driver Snowflake

Recursos de datos:
1)	JSON (GASTOS DE VENTA)
2)	SQL (VENTAS)
3)	SNOSFLAKE (GASTOS OPERATIVOS)

Para elaborar el estado de resultado necesitamos poder llegar a obtener la utilidad neta sin llegar a algo más detallado guiarse por el siguiente cuadro

VENTAS	SUM(VENTAS)
COSTO VENTAS	SUM(COSTO VENTAS)
UTILIDAD BRUTA	VENTAS-COSTO DE VENTAS
GASTOS OPERATIVOS	SUM(GASTOS OPERATIVOS)
UTILIDAD OPERACIONAL	UTILIDAD BRUTA - GASTOS OPERATIVOS
ISR 1 TRIMESTRE	SUM(ENE, FEB, MAR) *0.28
ISR 2 TRIMESTRE	SUM(ENE, FEB,MAR) *0.28
ISR 3 TRIMESTRE	SUM(ENE, FEB,MAR) *0.28
ISR 4 TRIMESTRE	SUM(ENE, FEB,MAR) *0.28
UTILIDAD NETA	UTILIDAD OPERACIONAL - ISR TRIMESTRE 1,2,3,4

Para la parte de los datos transaccionales el caso del archivo en classroom llamado PJ utilizar el usuario analista de datos cargado también en classrrom para poder cargar ese archivo plano en SQL favor de llamar a su tabla PJ_(PRIMER NOMBRE)(LETRA INICIAL DE PRIMER APELLIDO) ejemplo PJ_EDERC 

Notas importantes:
En caso de encontrar outliers en los datos, aislarlos y presentar sus interpretaciones de porque se pudieron generar esos datados


**Outliers:**
Se encontraron en la tabla de ventas varias fechas distorsionadas, es decir que los meses contenian cantidades de dias mayores a los que realmente corresponde.

El formato fecha en la tabla de ventas se transformó a un texto para poder tener el nombre del mes y asi determinar de una mejor forma los meses que se debian cumplir a corde a los entregables.

**Recomendaciones:**
Los gastos mas elevados se encuentran en la operación, por lo que se debe de realizar un presupuestos para el mejor manejo de los mismos.

* En el caso de Gastos de tecnología y comunicación incluyendo servicios de Internet telefonía y software, por el monto que tiene, se recomienda registrarlo como una capitalización para que el monto total se baja diluyendo durante la vida útil del mismo (por medio de su depreciación mensual)
* En el caso de los Gastos de almacenamiento y logística buscar otros proveedores que presenten el servicio a un precio mas favorable sin perder la calidad del mismo.
* Para el rubro de Salarios y beneficios de los empleados, realizar un revisión de compensaciones para determinar si estan acorde al mercado, también pudieran cambiarse los beneficios hacia beneficios NO monetarios para no perder la incentivación a los colaboradores.
* En el caso de la Depreciación de activos fijos, se debe de determinar si todos los activos están proporcionando el retorno esperado, ya que la idea de comprar activos fijos es para incrementar las utilidades, es posible que existan AF que no esten siendo utilizados al 100% ó se esten utilizando para otros fines.
