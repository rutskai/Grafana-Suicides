# Dashboard de Análisis de Suicidios

## Descripción general

Este dashboard interactivo permite explorar y analizar datos globales y regionales relacionados con suicidios a lo largo del tiempo, con especial enfoque en visualizaciones comparativas y distribución geográfica. Está diseñado para facilitar la interpretación rápida de patrones y diferencias entre regiones, periodos y variables demográficas.

---

## Objetivos

* Visualizar tendencias históricas de suicidios a nivel mundial.
* Comparar cifras entre regiones.
* Analizar datos específicos de países (ej. China).
* Explorar métodos utilizados y resultados clínicos.
* Detectar patrones relevantes.

---

## Requisitos

* Grafana instalado
* Dataset cargado dede GitHub
  - China: https://raw.githubusercontent.com/rutskai/Grafana-Suicides/refs/heads/master/SuicideChina.csv
  - Global: https://raw.githubusercontent.com/rutskai/Grafana-Suicides/refs/heads/master/age_std_suicide_rates_1990-2022.csv
* Permisos de lectura sobre la fuente de datos

## Paneles incluidos

---

### 1. Total suicidios por región (1990–2022)

Gráfico de barras que muestra el total acumulado por continente o región. Permite identificar rápidamente qué áreas concentran mayor número de casos.

**Métrica:**
`SuicideCount (sum)`

---

### 2. Mapa mundial de suicidios (1990-2022)

Mapa interactivo con marcadores geográficos que representan la distribución global de casos.
Sirve para detectar concentración regional y comparar densidad de suicidios entre zonas.

---

### 3. Hospitalizados totales (China 2009–2011)

Panel de estadística resumida que muestra el total de personas hospitalizadas registradas en el dataset filtrado para ese país y rango temporal (2009-2011).
- Variable utilizada en el título.

---

### 4. Fallecidos totales (China 2009–2011)

Indicador numérico que representa el total de personas fallecidas dentro del mismo subconjunto de datos y entre el año 2009 y 2011.
- Variable utilizada en el título.

---

### 5. Fallecidos vs No Fallecidos (China 2009-2011)

Visualización tipo gauge doble que compara proporción entre:

* Pacientes que sobrevivieron
* Pacientes fallecidos

Permite evaluar la tasa de letalidad dentro del conjunto analizado entre el 2009 y 2011.
- Variable utilizada en el título.

---

### 6. Métodos utilizados (China 2009-2011)

Gráfico circular que muestra la distribución de métodos registrados.
Ejemplos de categorías:

* Pesticidas
* Ahorcamiento
* Otros venenos
* Métodos no especificados
* Cortes
* Ahogamiento
* Saltos

---

## Fuente de datos

El sistema está diseñado para trabajar con datasets estructurados en formato CSV que contengan campos como:

* Año
* Región / País
* Sexo
* Edad
* Hospitalización
* Resultado (vive/fallece)
* Método
* Variables socioeconómicas (opcional)

---

## Tecnologías utilizadas

* Grafana para visualización
* Dataset estructurado como fuente de datos
* Transformaciones internas de Grafana:

  * Reduce
  * Group By
  * Count
  * Sum
  * Filter

---

## Posibles mejoras futuras

* Filtros por género y grupo de edad
* Ratio de mortalidad por método
* Comparador entre países
* Predicciones basadas en series temporales
* Panel de correlaciones socioeconómicas


---


## Notas

Los datos deben interpretarse con contexto estadístico y social. Las visualizaciones muestran tendencias agregadas y no sustituyen análisis clínicos.
### Grafana-Kaggle
https://www.kaggle.com/datasets/ronaldonyango/global-suicide-rates-1990-to-2022

---

**Autora:**
Ruth Collado García.



