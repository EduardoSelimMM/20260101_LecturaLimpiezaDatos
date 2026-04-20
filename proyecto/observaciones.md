Para la tabla de `vuelos`:

+ dep_time, arr_time: Actual departure and arrival times
+ sched_dep_time, sched_arr_time: Scheduled departure and arrival times
+ dep_delay, arr_delay: Departure and arrival delays, in minutes. Negative times represent early departures/arrivals
+ carrier: Two letter carrier abbreviation
+ flight: Flight number
+ tailnum: Plane tail number
+ origin, dest: Origin and destination
+ air_time: Amount of time spent in the air, in minutes.
+ distance: Distance between airports, in miles.
+ hour, minute: Time of scheduled departure broken into hour and minutes.
+ time_hour: Scheduled date and hour of the flight as a POSIXct date.
+ **IMPORTANTE:** Junto con origin, se puede usar `time_hour` para hacer join de los vuelos con las tablas de vuelos y clima.

"Taxi out" (o rodaje de salida en español) es el tiempo y el proceso en el que un avión se mueve desde la puerta de embarque (gate) hasta la pista de despegue. Incluye el rodaje, paradas y esperas antes de alzar el vuelo. Para esto, considérese las variables dep_delay y arr_delay
