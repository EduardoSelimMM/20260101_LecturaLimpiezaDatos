# Proyecto de fin de módulo

El proyecto final se realizará en **equipos de 3 personas**.

**ENTREGA:** Un documento .qmd (QUARTO) y su correspondiente archivo HTML, donde se describa detalladamente sus procedimientos.

**FECHA DE ENTREGA:** 7 de mayo de 2026

## Primera parte - R: Vuelos de NYC

Utilizaremos las tablas de la base de datos `vuelos.db` que incluye información de:

+ flights: Detalles de todos los vuelos que salieron de NYC (JFK, LGA, EWR) en 2013.
+ airlines: Códigos y nombres de aerolíneas.
+ airports: Información sobre aeropuertos, incluyendo ubicación.
+ planes: Datos sobre aeronaves, incluyendo año de fabricación.
+ weather: Datos meteorológicos por hora para los aeropuertos de NYC.

Responda las siguientes preguntas de 2 formas. Una utilizando verbos de {dplyr} y la otra con sintaxis SQL:

1. ¿Qué aerolínea tuvo el mayor retraso promedio en la salida en 2013?
2. ¿Qué día de la semana tuvo más vuelos retrasados en promedio?
3. ¿Cuál es la distribución de los retrasos en la salida para cada aeropuerto?
4. ¿Qué proporción de vuelos se retrasaron más de 30 minutos?
5. ¿Qué destinos tuvieron los mayores retrasos promedio en la llegada?
6. ¿Qué aerolíneas tuvieron el mayor número de vuelos desde NYC?
7. ¿Cómo varía el retraso de los vuelos según el fabricante de la aeronave?
8. ¿Los aviones más antiguos tienen más retrasos?
9. ¿Qué modelos de aviones se utilizan con mayor frecuencia en vuelos desde NYC?
10. ¿Cuál es la distancia promedio de vuelo por aerolínea?
11. ¿Qué aeropuerto de NYC tuvo el mayor número de retrasos en la salida?
12. ¿Qué aeropuerto tuvo el menor tiempo promedio de taxi-out?
13. ¿Qué porcentaje de vuelos que salen de cada aeropuerto de NYC fueron puntuales?
14. ¿Qué aeropuertos de destino tienen el mayor retraso promedio en la llegada para vuelos desde NYC?
15. ¿Cómo varían los retrasos en la salida según la hora del día en cada aeropuerto de NYC?
16. ¿Cuál es la correlación entre la velocidad del viento y los retrasos en la salida?
17. ¿Los vuelos experimentan más retrasos en días con lluvias intensas?
18. ¿Cómo afecta la temperatura a los retrasos de los vuelos?
19. ¿Cómo afectan los niveles de visibilidad a los retrasos en la llegada?
20. ¿La alta humedad se relaciona de alguna manera con los tiempos de taxi-out más largos?

## Segunda parte - Python: API APOD de la NASA

+ Usarán la API de la NASA llamada APOD (Astronomy Picture of the Day). Busca su documentación en https://api.nasa.gov/
+ Genera una API key en el sitio https://api.nasa.gov/
+ Cada miembro del equipo debe seleccionar la palabra correspondiente al número de la primera letra de tu apellido paterno. Por ejemplo, 1 = A, 2 = B, 3 = C, etc. Si tu apellido empieza con Ñ, selecciona la última palabra de la lista. Si la palabra coincide con la de algunos miembro de tu equipo, toma la inmediata posterior.

1. gravitational
2. retrograde
3. supernova
4. spiral
5. James Webb
6. emission
7. nebula
8. planetary
9. Juno
10. X-ray
11. black hole
12. infrared
13. dust clouds
14. aurora borealis
15. Northern Lights
16. geomagnetic storm
17. Perseids
18. Geminids
19. Einstein
20. elliptical
21. Newton
22. Spitzer
23. Kepler
24. Apollo
25. Voyager
26. Redshift
27. Hand of God
28. Hydrogen
29. alpha
30. Sulfur

+ **Cuidado:** La API se puede sentir "atacada" y bloquearte si haces muchas solicitudes rápidamente.
+ **Cuidado:** La API sólo permite un número finito de solicitudes.

Basándose en solicitudes de la API en el campo "explanation" haz búsquedas basadas en tu palabra y responde la siguientes preguntas:

**Preguntas del equipo:**

1. ¿Qué tipo de parámetros admite la solicitud?
2. ¿Qué tipo respuestas se pueden obtener con cada solicitud?
3. ¿Qué tipo de restricciones tiene la API?

**Preguntas de cada miembro del equipo:**

1. Para las búsquedas de tu palabra, ¿cuántos resultados obtuviste?
2. Para las búsquedas de tu palabra, ¿en qué rangos de fechas se introdujo el recurso?
3. Para las búsquedas de tu palabra, ¿cuáles son los "media_type" más comunes?
4. Para las búsquedas de tu palabra, ¿quiénes son los autores o instituciones propietaria de los derechos (i.e. el copyright)?

## Tercera parte - Lenguaje R y Python (ambos): Calidad del café

Se usará el conjunto de datos de encuesta de café

`datos <- readr::read_csv("coffee_ratings.csv")`

Actividad 0: Realice un análisis de valores faltantes del objeto `datos`

Actividad 1: Crear una columna llamada `color2` que se base en los valores de la columna `color`, que asigne el valor NA si  `color == NA`, "#00FF66" si `color == 'Green'`, "#CCEBC5" si `color == 'Bluish-green'` y "#BFFFFF" si `color == 'Blue-green'`

Actividad 2: Crear una columna llamada `bag_weight2` que se base en los valores de la columna `bag_weight`, que sólo contenga el valor numérico de ésta. Es decir, `bag_weight2` debe ser numérica. ¿Cuántas observaciones llevaron a ambigüedad para crear esta nueva columna?

Actividad 3: Crear dos columnas llamadas `method1` y `method2` que se basen en los valores de la columna `processing_method`, dividiendo en dos partes los valores dicha columna. ¿Cuántas observaciones llevaron a ambigüedad para crear esta nueva columna?

Actividad 4: Crear tres columnas llamadas `expiration_day`, `expiration_month` y `expiration_year` que se basen en los valores de la columna `expiration`. ¿Cuántas observaciones llevaron a ambigüedad para crear estas nuevas columnas?

Actividad 5: Crear dos columnas llamadas `harvest_mes` y `harvest_anio` que se basen en los valores de la columna `harvest_year`, dividiendo en dos partes los valores dicha columna. ¿Cuántas observaciones llevaron a ambigüedad para crear esta nueva columna?

Actividad 6: Elabore una visualización con {ggplot2} que identifique alguna relación entre las columnas total_cup_points, acidity y color2 de tal forma que se puedan identificar los colores de la variable `color2`. Es decir, debemos ver los colores, "#00FF66", "#CCEBC5" y "#BFFFFF".

Actividad 7: Elabore una visualización de densidad con {ggplot2} de la variable `bag_weight2` diferenciando a los valores de `species`.

Actividad 8: Elabore una visualización que relacione el año/mes de expiración con el `total_cup_points` sólo de los granos mexicanos, brasileños, colombianos y guatemaltecos.

Actividad 9: Elabore una visualización con {ggplot2} que relacione el mes de expiración con el `altitude_mean_meters`, `altitude_low_meters` y `altitude_high_meters` sólo de los granos mexicanos, brasileños, colombianos y guatemaltecos de los años de expiración 2016 y 2017.

Actividad 10: Elabore una visualización con {ggplot2} que relacione el `aftertaste`, `acidity`, `body` y `species` en un mismo canvas.

*Importante:* Sus visualizaciones deben tener formato suficientemente bueno para publicar en alguna revista.
