

# DATA SCIENCE - PROYECTO INDIVIDUAL Nº2
# Data Analytics

Este proyecto abarca una serie de pasos para desarrollar un proceso de Data Analytics sobre un dataset de accidentes aéreos, para posteriormente disponibilizar un Dashboard Interactivo utilizando Power BI.

![Logo](https://github.com/Adrsilbad32/Proyecto_Individual_2/blob/main/Imagenes/tecnologia-tecnologia_523458626_160950481_1706x960.jpg)

## Contexto

Se plantea la necesidad de analizar datos históricos de **`accidentes aéreos`** a los efectos de identificar patrones, tendencias y factores que ayuden a mejorar la seguridad en la aviación civil. 

## Dataset

El [dataset](https://github.com/Adrsilbad32/Proyecto_Individual_2/blob/main/AccidentesAviones.csv) en cuestión posee información acerca de vuelos que han sufrido un siniestro a lo largo de todo el mundo desde 1908 hasta 2021. El mismo cuenta con 5008 filas (representando cada fila un accidente aéreo) y 18 columnas (atributos de cada vuelo).

## Objetivo

El propósito del trabajo fue describir las características de vuelos siniestrados a los efectos de analizar los siguientes **`KPI's`** propuestos:

- Evaluar la disminución de un 10% la tasa de fatalidad de la tripulación en los últimos 10 años, comparado a la década anterior.
- Evolución de accidentes aéreos y comparación con métricas anteriores.
- Disminución de la cantidad de accidentes por pais.


## ETL  

Para realizar los procesos de ETL se utilizó **`Python`** con librerías de Numpy, Pandas, Matplotlib y Seaborn, entre otras.
Se pueden visualizar las transformaciones y los análisis realizados en el siguiente
[archivo](https://github.com/Adrsilbad32/Proyecto_Individual_2/blob/main/accidentes_aereos.ipynb)





## Análisis exploratorio de datos

A los efectos de poder entender los datos presentados, se realizaron una serie de análisis y estudios sobre las variables del dataset a los efectos de poder encontrar relaciones entre los datos y comprender la relevancia de los mismos.
Dentro de los análisis efectuados se encuentran: 
- Nubes de palabras para identificar causas comunes en las descripciones de los accidentes;
- Distribuciones de frecuencias y estadísticas de las variables numéricas;
- Análisis e identificación de outliers en variables de interés (total_aboard y total_fatalities);
- Identificación de variables categóricas y sus valores; 
- Análisis de accidentes, tasa de mortalidad, tasa de supervivencia y seguridad en vuelos por: país, aerolínea, aeronave, marca de aeronave y categoría de vuelo;
- Análisis temporales por hora, día, mes y año.

Se pueden visualizar las transformaciones y los análisis realizados en el siguiente
[archivo]((https://github.com/Adrsilbad32/Proyecto_Individual_2/blob/8a9d4556473d5eca8b9726d5d8083ec7e5b39826/accidentes_aereos.ipynb))

## Dashboard e insights

El [dashboard](https://github.com/Adrsilbad32/Proyecto_Individual_2/blob/main/dashboard_air_accidents.pbix) consta de 1 portada y 5 páginas navegables a través de una botonera de navegación.



### País

En la primer página denominada **`País`**, se pueden observar los accidentes por país pudiendo filtrar a su vez por año, categoría del vuelo y superfice de impacto. Tenemos información acerca de pasajeros a bordo, fatalidades y tasa de mortalidad (TM) junto con un gráfico de su evolución a lo largo del tiempo.
Podemos observar a `Estados Unidos` como el país con mayor cantidad de accidentes a lo largo de la historia y Rusia como el segundo.
Por último podemos visualizar una tarjeta de KPI que muestra la tasa de mortalidad por año. 




### Operador

En la segunda página denominada **`Operador`**, se puede observar la cantidad de operadores analizados pudiendo filtrar a su vez por año, País y superfice de impacto. Tenemos información acerca de pasajeros a bordo, sobrevivientes y tasa de supervivencia (TS) junto con un gráfico de su evolución a lo largo del tiempo.
Podemos observar a `Aeroflot` como la aerolínea con mayor cantidad de accidentes históricos seguido por la fuerza aérea de Estados Unidos.



### Aeronave

En la tercer página denominada **`Aeronave`**, se puede observar la cantidad de aeronaves y marcas involucradas en el dataset pudiendo filtrar especificamente por tipo de aeronave, marca de aeronave, operador y año. Tenemos medidores de tasa de mortalidad y tasa de supervivencia, un gráfico de barras con las principales marcas y sus aeronaves y un gráfico de composición de las aeronaves según sea la categoría (vuelo militar o vuelo no militar)
Podemos observar al `Douglas DC-3` como el avión con mayor cantidad de accidentes a lo largo de la historia. El mismo perteneció a la compañía Douglas que con el tiempo mutó a MCDonell Douglas para finalmente convertirse en Boeing.





### Tendencia

La última página del dashboard se denomina **`Tendencia`** y se encarga de analizar los accidentes y la cantidad de pasajeros con sus respectivas tendencias a lo largo del tiempo.
Podemos destacar que no siempre existe una relación directa entre la tendencia de accidentes por período y la cantidad de pasajeros (véase en tendencia mensual).
Por otro lado se pueden analizar la cantidad de accidentes a lo largo de los años con la media móvil de 10 períodos, lo cual nos permite concluír que los años donde la cantidad de accidentes se ha encontrado por debajo de la media móvil, han resultado años con baja siniestralidad, mientras que aquellos años donde la cantidad ha estado por encima han sido años con una gran cantidad de accidentes (años entre 1946 y 2004). Dicha media móvil puede ser ajustada en función de las circunstancias del futuro. Tal es así que podemos inferir que a nivel mundial estamos en una tendencia a la baja en cantidad de accidentes desde 1989 (año en que comienza a descender la cantidad de accidentes) y por debajo del promedio móvil de 10 años en los años siguientes por lo que resulta interesante mantenerse por debajo de dicho patrón para los próximos años.
Por último analizamos la variación interanual de accidentes y podemos filtrar por países como Estados Unidos para observar cómo se ha comportado en los últimos años pese a tener la mayor cantidad de accidentes y pasajeros históricos.

![logo](https://github.com/Adrsilbad32/Proyecto_Individual_2/blob/main/Imagenes/Capturasfacsz.JPG)
![logo](https://github.com/Adrsilbad32/Proyecto_Individual_2/blob/main/Imagenes/Capturadfgdf.JPG)


## Conclusiones

- La Tasa anual de mortalidad, tal como puede visualizarse en la página 'País', oscila entre el 50% y el 100% para la mayoría de los años. La misma si bien presenta tendencia en algunos períodos, no podemos decir que tenga una marcada tendencia a la baja. Es importante en su lugar, estar por debajo del target de tasa conforme al KPI indicado por lo que se sugiere revisarlo año a año;
- La tasa anual de supervivencia, tal como puede visualizarse en la página 'Operador', en contraposición a la tasa anual de mortalidad, oscila entre el 0% y y el 50% para la mayoría de los años. Es deseable para la mayoría de las aerolíneas poder mantenerse por encima del 50%. 
- La tendencia anual de accidentes a lo largo de la historia comenzó una gran tendencia alcista desde los días de los primeros vuelos hasta 1945. La tendencia pudo consolidarse entre 1946 y 2004 para finalmente romper la zona de acumulación en 2005 (año en que confirmamos la tendencia a la baja comenzada en 1989). La media móvil de 10 años nos ayuda a visualizar años de baja siniestralidad, por lo que se alienta a mantenerse por debajo de la misma y activar alertas en el momento en que la tendencia anual se aproxime a la misma (situación que ha acontecido numerosas veces a lo largo de la historia). Es positivo a su vez, poder afirmar que la aviación ha alcanzado un nivel de seguridad que permite estar en los niveles de accidentes más bajos de la historia, considerando la cantidad de vuelos, personas transportadas y avances tecnológicos en contraposición a los primeros días;
- Por último es destacable la tendencia anual de accidentes para los países como Estados Unidos y Rusia, los cuales pese a tener la mayor cantidad de accidentes históricos, mantienen marcadas tendencias a la baja en los últimos años, en concordancia con la tendencia mundial. # Proyecto_Individual_2
