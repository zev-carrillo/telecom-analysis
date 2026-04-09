# Análisis de Usuarios y Comportamiento de Uso

## Objetivo del Proyecto

El objetivo de este proyecto es analizar el comportamiento de los usuarios de un servicio de telecomunicaciones, identificando patrones de uso, segmentación por edad y tipo de plan, así como posibles oportunidades de mejora en retención y monetización.

Se busca responder preguntas como:
- - ¿Qué segmentos de clientes muestran **mayor o menor uso** de llamadas y mensajes?
- ¿Qué usuarios presentan **valores atípicos** que puedan indicar comportamientos inusuales, fraude o errores de registro?
- ¿Cómo varía el uso según la **edad** y el **tipo de plan contratado**?
- ¿Qué patrones pueden ayudar a **diseñar mejores planes**, optimizar la oferta y mejorar la satisfacción del cliente?



## Datasets Utilizados

### 1. `users`
Contiene información demográfica y de estado del usuario:
- `user_id`
- `first_name`
- `last_name`
- `age`
- `city`
- `reg_date`
- `plan`
- `churn_date`

### 2. `usage`
Contiene información de uso del servicio:
- `id`
- `user_id`
- `type`
- `date`
- `duration` (llamadas)
- `length` (mensajes de texto)

### 3. `plans`
- `plan_name`
- `messages_included`
- `gb_per_month`
- `minutes_included`
- `usd_monthly_pay`
- `usd_per_gb`
- `usd_per_message`
- `usd_per_minute`




## Etapas del Análisis

### 1. Exploración de los datos
- Vista rápida de los datos
- Exploración de estructura de los datos
- Identificación de problemas de calidad en los datos
- Estandarización de fechas

### 2. Limpieza de datos
- Manejo de valores nulos  
- Corrección de valores fuera de rango (ej: edad = -999)  
- Eliminación de datos atípicos (outliers evidentes)  
- Validación de consistencia entre variables

### 3. Transformación de datos  
- Creación de variables categóricas:  
	- `grupo_edad`  
	- `grupo_uso`  
- Unión de datasets (`users` + `usage`)  
- Agregaciones y cálculos por usuario

### 4. Visualización
- Gráficos de barras
- Gráficos apilados (stacked)
- Análisis proporcional por segmento

### 5. Generación de insights
- Identificación de patrones de comportamiento
- Detección de oportunidades de negocio
- Recomendaciones estratégicas



## Cómo ejecutar el Notebook

### Google Colab 
1. Abre Google Colab: https://colab.research.google.com/
2. Haz clic en **"Upload"** (Subir)
3. Sube el archivo `.ipynb` del proyecto
4. Ejecuta las celdas en orden (Shift + Enter)

## Guía de Reproducción

1. Cargar los datasets (`users` y `usage`)
2. Realizar limpieza de datos:
    - Manejo de nulos
    - Corrección de valores inválidos
3. Crear variables derivadas:
    - Segmentos por edad
    - Segmentos por nivel de uso
4. Unir datasets por `user_id`
5. Realizar análisis exploratorio:
    - Distribuciones
    - Crosstab
6. Generar visualizaciones
7. Interpretar resultados y construir insights
