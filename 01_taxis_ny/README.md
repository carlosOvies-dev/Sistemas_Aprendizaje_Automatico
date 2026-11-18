# Práctica: Análisis de Viajes en Taxi en Nueva York y Codificación con Embeddings

## ¿De qué trata este ejercicio?
En esta práctica trabajamos con un conjunto de datos de viajes de vehículos con conductor (VTC y taxis) en Nueva York del año 2019. Como cada empresa aplica sus propias tarifas y no tenemos el precio final del viaje, nuestro objetivo (variable objetivo o *target*) es calcular y predecir la **duración del viaje** a partir de las fechas de inicio y fin. Conocer cuánto dura un trayecto nos permite estimar de forma justa qué viajes son más rentables.

## Datos con los que trabajamos
El dataset registra para cada viaje:
* Identificadores de la licencia del vehículo (`hvfhs_license_num`) y de la empresa que gestiona el viaje (`dispatching_base_num`).
* Fecha y hora exacta de recogida (`pickup_datetime`) y de llegada (`dropoff_datetime`).
* Códigos numéricos de la zona donde sube el pasajero (`PULocationID`) y donde baja (`DOLocationID`).
* Un indicador sobre si el viaje ha sido compartido o de un tipo de reserva especial (`SR_Flag`).

## Pasos que vamos a realizar
1. **Exploración y limpieza de datos:** Cargar los datos, revisar qué valores faltan (nulos), qué significan y limpiar posibles errores lógicos (como viajes con duraciones imposibles).
2. **Estudio de las zonas de recogida y destino:** Dibujar histogramas para ver qué barrios tienen más tráfico y agrupar las zonas con muy pocos viajes en una categoría común para que el modelo aprenda mejor.
3. **Creación de Embeddings:** Usar una red neuronal para transformar los códigos de las zonas en vectores de números (embeddings) que capturen cómo se comporta cada zona con respecto a la duración de los viajes.
4. **Reducción a 2 dimensiones con PCA y análisis:** Comprimir esos embeddings a 2 dimensiones para poder dibujarlos en un gráfico plano, buscar grupos de zonas parecidas y analizar algún caso concreto que destaque en la gráfica.
