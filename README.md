# ia1-2bots-Weather_forecast_and_Air_pollution
**Curso: Inteligencia Artificial I -2025-2 C1**<br>
**Equipo: 2bots**<br>
**Autores** 
 <ul> <li>Daniel Fernando Leal Ayala 2191430</li>
     <li>Rafael Andres Pinilla Vargas 2221929 </li>
 </ul>

# Descripción de los datos

Dataset: APIS sobre el clima y contaminación del aire Openmeteo

Fuentes: <ul>
     <li>https://open-meteo.com/en/docs/historical-forecast-api </li>
     <li>https://open-meteo.com/en/docs/air-quality-api</li>
 </ul>
 
Cantidad de datos: Datos actualizados diariamente cada 3 horas,además de registros desde 1940 para los datos del clima y desde el 2015 para datos de contaminación del aire

#  Preguntas a responder
## Antes del EDA 
### Problema y relevancia

*La contaminación atmosférica y las condiciones meteorológicas adversas representan uno de los principales riesgos para la salud pública y la planificación urbana. En muchas ciudades colombianas, los episodios de mala calidad del aire están asociados a fenómenos meteorológicos como baja velocidad del viento, alta humedad o inversiones térmicas. El problema que se busca resolver consiste en predecir eventos de alta contaminación (AQI elevado) y pronosticar variables meteorológicas críticas (temperatura, precipitación, viento) que los explican. Anticipar estas condiciones es esencial para emitir alertas tempranas, proteger la salud y optimizar estrategias ambientales.*

### Objetivo del análisis
El objetivo del EDA es comprender la estructura, calidad y relaciones internas de los datos ambientales y meteorológicos, identificando patrones, correlaciones y tendencias temporales que expliquen la variación del PM2.5 y del AQI. Esta fase permite validar supuestos, detectar valores atípicos o faltantes, y seleccionar las variables más relevantes para los modelos predictivos posteriores de regresión y clasificación.

### Métricas o indicadores
En esta fase se emplearán indicadores descriptivos y estadísticos para conocer el comportamiento de las variables.
Entre ellos: promedios, medianas, desviaciones estándar, máximos, mínimos y correlaciones entre contaminantes y variables meteorológicas.
También se analizarán tendencias y variaciones temporales (por hora, día y semana).
Estos indicadores son útiles porque permiten identificar patrones, anomalías y relaciones iniciales que orientan el posterior modelado y ayudan a formular hipótesis sobre las causas de la contaminación y su relación con el clima.
Estas métricas permiten comprender la distribución y variabilidad del consumo, detectar valores atípicos que podrían distorsionar el análisis y evaluar qué variables están más relacionadas con el consumo. Esto ayuda a seleccionar predictores relevantes y a preparar los datos de manera adecuada antes de construir modelos de predicción.

### Motivación de la elección
El tema fue elegido porque integra datos reales, impacto ambiental y aplicación social directa. Combina modelamiento meteorológico y calidad del aire, áreas clave para la sostenibilidad urbana y la inteligencia ambiental. Además, permite aplicar algoritmos de aprendizaje automático en un contexto de alta relevancia para la salud y la gestión pública.

## Después del EDA 

### Datos utilizados
Se emplearon datos históricos del servicio Open-Meteo API y registros de calidad del aire (PM2.5, PM10, NO₂, SO₂, O₃, AQI). Los datos son numéricos y temporales, con frecuencia horaria y cobertura en varias ciudades colombianas. Representan series de tiempo multivariadas de contaminantes y variables meteorológicas.

### Información contenida en los datos 
El conjunto de datos incluye variables meteorológicas (temperatura, humedad relativa, velocidad del viento, precipitación) y contaminantes atmosféricos (PM2.5, PM10, NO₂, SO₂, O₃), además del AQI calculado. Estas variables permiten analizar interacciones físicas entre meteorología y calidad del aire, estudiar patrones temporales (diarios, semanales, estacionales) y construir modelos predictivos tanto para la estimación de contaminantes como para la detección de episodios críticos. La combinación de ambas fuentes proporciona una base sólida para entrenar modelos multivariados y evaluar la dinámica conjunta de clima y contaminación.

### Desafíos asociados a los datos
Los principales desafíos incluyen valores faltantes por interrupciones en sensores, desbalance de clases (pocos eventos de alta contaminación), y ruido en las mediciones debido a condiciones atmosféricas locales. Existen además diferencias temporales y espaciales entre estaciones meteorológicas y de calidad del aire, lo que puede afectar la correlación. La alta colinealidad entre contaminantes y variables meteorológicas exige técnicas de selección o reducción de dimensionalidad. Finalmente, el tamaño limitado del historial restringe la generalización temporal de los modelos, por lo que se requiere validación cruzada temporal.
