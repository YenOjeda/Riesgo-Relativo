# PROYECTO RIESGO RELATIVO

En el actual escenario financiero, la disminución de las tasas de interés ha generado un notable aumento en la demanda de crédito en el banco "Super Caja". Sin embargo, esta creciente demanda ha sobrecargado al equipo de análisis de crédito, que se encuentra actualmente inmerso en un proceso manual ineficiente y demorado para evaluar las numerosas solicitudes de préstamo. 

Con el fin de abordar este desafío, la propuesta es la automatización del proceso de análisis utilizando técnicas avanzadas de análisis de datos, con el objetivo de mejorar la eficiencia, la precisión y la rapidez en la evaluación de las solicitudes de crédito. Además, el banco ya tiene una métrica para identificar a los clientes con pagos atrasados, lo que podría ser una herramienta valiosa para integrar en la clasificación de riesgo dentro del nuevo sistema automatizado.

# Base de datos

Conte con 4 datasets, una relacionada con la información de los clientes del banco (fecha del último salario, número de dependientes, salario,etc), otroa con la información de los créditos (tipos de creditos por cliente), otra con la información y estado del crédito (númerode días de retraso en el pago, utilización de la capacidad de pago, etc) y la última con la información del score crediticio manejado por el banco (clasificación del cliente como buen o mal pagador).

# Objetivo del proyecto

- Calcular el Riesgo Relativo de acuerdo a variables de interes.
- Comprobar las Hipotesis planteadas por el banco:
  1.- Los jovenes tienen mayor riesgo de ser impagos.
  2.- Las personas con un mayor número de créditos activos tienen un mayor riesgo de ser malos pagadores.
  3.- Las personas que se han retrasado más de 90 días tienen el riesgo de ser malos pagadores.
- Diseñar un Score Crediticio para categorizar a los solicitantes, en niveles de riesgo basado en la probabilidad de incumplimiento.

  El objetivo del análisis es armar un score crediticio a partir de un análisis de datos y la evaluación del riesgo relativo que pueda clasificar a los solicitantes en diferentes categorías de riesgo basadas en su probabilidad de incumplimiento. Esta clasificación permitirá al banco tomar decisiones informadas sobre a quién otorgar crédito, reduciendo así el riesgo de préstamos no reembolsables. Además, la integración de la métrica existente de pagos atrasados fortalecerá la capacidad del modelo para identificar riesgos, lo que en última instancia contribuirá a la solidez financiera y la eficiencia operativa del banco.

# Proceso

- ETL en BigQuery (SQL).
- Análisis Exploratorio de los Datos: a través de visuales (Looker Studio), se visualizaron los datos, se detallaron patrones, datos outliers, distribución de los datos, gráficas de dispersión,etc.
- Técnicas de Análisis: cálculo de cuartiles, segmentación y cálculo de Riesgo Relativo:
  * RR = 1 = No hay riesgo
  * RR > 1 = Hay riesgo.
  * RR < 1 = No hay riesgo.
- Cálculo de variables Dummy (convierte una variable categorica en una variable binaria, con el fin de utilizarla en un modelo predictivo).
- Segmentación de variables dummy (Buen pagador y Mal pagador).
- Score Crediticio.
- Matriz de confusión (evalua la efectividad del modelo para predecir correctamente el riesgo de incumplimiento).

# Insides

- Los jovenes tienen un MAYOR RIESGO de ser malos pagadores.
- Las personas con un mayor número de creditos activos tienen un MENOR RIESGO de ser malos pagadores.
- Las personas que se han retrasado más de 90 días en sus pagos tienen un MAYOR RIESGO de ser malos pagadores.

# HERRAMIENTAS UTILIZADAS

    •  Big Query (SQL).
    •  Google Colab (Python).
    •  Looker Studio.
    •  Google Slides.
    •  Loom.
