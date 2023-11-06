# PRUEBA DATA SCIENCE - HACKATÓN

## Introducción: Presentación del conjunto de datos y de las variables seleccionadas.

### Media del alquiler mensual (€/mes) y por superficie (€/m2) de la ciudad de Barcelona.  

- Trimestre: Indicates the quarter of the year. 
- Codi_Districte: The district code. 
- Nom_Districte: The name of the district. 
- Codi_Barri: The neighborhood code. 
- Nom_Barri: The name of the neighborhood. 
- Lloguer_mitja: Type of average rent, which in this case appears to be the **average monthly rent** in Euros/month and in Euros/m2 month. 
- Preu: Price, indicating the **average monthly** rental price in Euros. 

### Exposición a los ruidos de la población, del Mapa Estratégico de Ruido de la ciudad de Barcelona.  

- Codi_Districte: A numerical code representing a district. 
- Nom_Districte: The name of the district. 
- Codi_Barri: A numerical code for a neighborhood within the district. 
- Nom_Barri: The name of the neighborhood. 
- Concepte: The concept or type of noise measurement. 
- Noise level categories measured in decibels (dB). 

## Descripción detallada de las técnicas de preprocesamiento aplicadas y los criterios de evaluación utilizados:

- Eliminación de filas duplicadas.
- Eliminación de filas con valores NaN.
- Estandarización de las variables numéricas.
- Transformación de la información almacenada en filas en nuevas columnas, específicamente:
  - `Lloguer_mitja`: División de la columna en dos nuevas columnas para evitar conclusiones estadísticas erróneas.
  - `Rang_soroll`: Conversión a columnas para crear un nuevo conjunto de variables que puedan servir en el análisis de este dataset.

## Resultados

Se realizó un PCA del conjunto de datos, reduciendo los datos a dos componentes principales:

- Primer componente principal \(PC1\) está fuertemente influenciado por las características del nivel de ruido.
- Segundo componente principal \(PC2\) tiene fuertes cargas negativas para el precio del alquiler mensual medio y el precio del alquiler por metro cuadrado medio.

El porcentaje de varianza explicada por los dos componentes principales es aproximadamente del 48,92% para el primer componente y del 16,37% para el segundo componente. Juntos, estos dos componentes explican aproximadamente el 65,29% de la varianza total en el conjunto de datos. 


## Conclusiones

Principales inferencias derivadas de los resultados:

- PC1 resume los niveles de ruido en las áreas, y PC2 resume los precios de alquiler.
- Los datos podrían usarse para entender la relación entre el alquiler y el ruido en diferentes barrios y distritos.
- Posibles respuestas a hipótesis sobre la correlación entre el alquiler mensual medio y el nivel de ruido en un barrio, y la distribución de los niveles de ruido en función de los diferentes niveles de alquiler.
