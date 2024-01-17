# Observatorio de Movilidad y Seguridad Vial (OMSV) - Proyecto de Análisis de Datos

## Introducción

Este proyecto se centra en abordar la problemática de los siniestros viales en la Ciudad Autónoma de Buenos Aires (CABA) a través de un análisis exhaustivo de datos. La información utilizada comprende diversas variables, incluyendo las fechas de los accidentes, la ubicación geográfica, los participantes y otros elementos relevantes, proporcionando así una visión integral del fenómeno.

Se ha llevado a cabo un Análisis Exploratorio de Datos (EDA) utilizando un archivo en formato .xlsx, originado en Excel. Este archivo fue procesado con dataframes utilizando la biblioteca pandas, entre otras, para realizar descripciones estadísticas respaldadas con representaciones gráficas visuales.

Además, se ha desarrollado un dashboard dinámico utilizando Power BI. Este dashboard incluye los tres KPIs solicitados por Henry, permitiendo una presentación visual y accesible de los resultados.

Finalmente, este README se presenta como un informe detallado que proporciona información adicional sobre el proyecto, sirviendo como una guía completa para entender nuestros hallazgos y metodología.

## Contexto

En Argentina, los siniestros viales causan aproximadamente 4,000 muertes anuales. El Observatorio de Movilidad y Seguridad Vial (OMSV) busca contribuir a la reducción de este problema a través de un proyecto de análisis de datos. El dataset utilizado abarca información sobre homicidios en siniestros viales en Buenos Aires entre los años 2016 y 2021.

## Desarrollo

### EDA (Exploratory Data Analysis) - Python

Antes de sumergirnos en el Análisis Exploratorio de Datos (EDA), se llevó a cabo un análisis preliminar exhaustivo con el objetivo de entender a fondo la estructura de los datos. Se exploraron diversas facetas, como la composición de las columnas, los tipos de datos presentes, la existencia de duplicados, así como la identificación y evaluación de valores atípicos.

La detección de valores atípicos fue especialmente relevante, y su impacto se visualizó a través de gráficos que destacaron su importancia en la muestra. Es crucial destacar que, tras un análisis detallado, se determinó que estos valores atípicos eran coherentes dentro del rango general de los datos. La decisión de mantener el 100% de la base de datos original se tomó con el objetivo de preservar la integridad y consistencia en todo el análisis, reconociendo la relevancia de estos valores dentro del contexto general de la información.

En el desarrollo del EDA, se le dio especial énfasis al enfoque temporal, aprovechando la riqueza de información proporcionada en el archivo de origen. Este incluía detalles precisos como la fecha exacta del siniestro, año, mes, día y hora. Se realizaron análisis detallados en todas estas temporalidades, permitiendo una comprensión profunda de la dinámica temporal de los siniestros viales. Además, se abstrajo la información en relación con las estaciones del año (verano, otoño, invierno, primavera) para capturar posibles patrones estacionales que pudieran influir en la incidencia de los accidentes.

La exploración de variables clave, como comuna y tipo de calle, fue respaldada por gráficos de barras que facilitaron la identificación de patrones significativos. Se resaltaron 5 comunas específicas (1, 4, 9, 8 y 7) con un número notablemente superior de accidentes viales en comparación con el resto de la muestra. En el caso de los tipos de calle, la observación de que “AVENIDA” superaba significativamente a otras categorías como “CALLE”, “AUTOPISTA” o “GRAL PAZ” fue especialmente reveladora, desafiando posibles suposiciones basadas en el flujo de vehículos.

Finalmente, el análisis detallado de los participantes, tanto acusados como víctimas, destacó la importancia de categorías específicas. Autos, pasajeros y carga emergieron como los principales causantes de accidentes viales mortales. Se notó la vulnerabilidad de motociclistas y peatones, mostrando una pequeña diferencia entre ambos, lo cual se alineó con su mayor exposición al contacto directo con el entorno durante colisiones o atropellos.

Estos hallazgos subrayan la importancia de considerar múltiples perspectivas al abordar la seguridad vial en la Ciudad Autónoma de Buenos Aires. Específicamente, las intervenciones deben centrarse en mejorar la seguridad de los usuarios de la vía más vulnerables, como los peatones y los motociclistas, y en las áreas con una alta concentración de accidentes. Estos resultados proporcionan una base sólida para futuras investigaciones y la implementación de medidas de seguridad vial más efectivas.

### Dashboard - Power Bi

El diseño del dashboard se concibió con una orientación clara hacia la usabilidad, permitiendo al usuario navegar de manera intuitiva. La estética adoptada es ligera y minimalista, enfocándose en la presentación directa de datos relevantes mediante gráficos de barras que abordan aspectos cruciales como las muertes por año en siniestros, siniestros viales por año y gráficos de torta que presentan las calles con mayor incidencia de accidentes. Este enfoque facilita la comprensión rápida de patrones y tendencias.

En una segunda instancia, se desarrollaron tres Key Performance Indicators (KPIs), dos especificados por Henry y uno elegido de manera deliberada. Estos KPIs fueron representados gráficamente y comparados según criterios específicos:

#### Evaluación de KPIs - Mejora de la Seguridad Vial en CABA

1. **Reducción del 10% en la tasa de homicidios en siniestros viales en CABA comparando los últimos seis meses con el semestre anterior (Año 2021).**

   Tras calcular las tasas de homicidios en siniestros viales para ambos semestres, se observó una disminución del 23.86%. Esta reducción, que supera considerablemente el objetivo del 10% establecido como KPI, se ilustra a través de gráficos que resaltan la mejora significativa en la seguridad vial durante el periodo analizado.

   *La población de CABA se obtuvo de --> https://www.argentina.gob.ar/caba#:~:text=Datos%20Jurisdiccionales%20Superficie%3A%20200%20Km%C2%B2.%20Poblaci%C3%B3n%3A%203.121.707%20habitantes,precipitaciones%20resultan%20ser%20m%C3%A1s%20abundantes%20en%20%C3%A9poca%20estival.

2. **Reducción del 7% en la cantidad de accidentes mortales de motociclistas en CABA respecto al año anterior (Año 2021-2020).**

   La evaluación de la evolución de los accidentes mortales con víctimas en moto reveló un aumento del 70.37%, lo que indica que no se alcanzó la reducción del 7% propuesta como KPI. La presentación gráfica enfatiza esta discrepancia y resalta la necesidad de estrategias específicas para abordar los desafíos asociados a la seguridad de los motociclistas en la Ciudad Autónoma de Buenos Aires.

3. **Reducción de un 10% en el número de accidentes mortales con acusados en auto, del año 2021 en comparación con el año 2020.**

   La evolución de los accidentes mortales con acusados en auto mostró un aumento del 24%, lo que indica que no se cumplió la meta del 10% de reducción establecida como KPI. La presentación gráfica proporciona una visión detallada de este incremento y subraya la importancia de estrategias específicas para mitigar los riesgos asociados a los accidentes mortales con acusados en auto.

Estos KPIs y sus análisis detallados resaltan la necesidad imperante de evaluar y ajustar estrategias específicas, guiando así futuras acciones en la mejora continua de la seguridad vial en la Ciudad Autónoma de Buenos Aires.

