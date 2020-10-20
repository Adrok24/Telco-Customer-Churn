# Análisis de un data set de Telco Customer Churn y entrenamiento de un modelo predictivo por diferentes métodos

El dataset puede ser encontrado en el siguiente desafo de Kaggle: [Telco-customer-churn](https://www.kaggle.com/blastchar/telco-customer-churn)


# Motivación y dataset

La motivación es predecir el comportamiento para retener clientes. Poder analizar todos los datos relevantes de los clientes y desarrollar programas de retención de clientes.

* Cada fila representa un cliente, cada columna contiene los atributos del cliente descritos en la columna Metadatos.
* El conjunto de datos incluye información sobre:
* Clientes que se fueron en el último mes: la columna se llama RenunciaServicios a los que cada cliente se ha suscrito: teléfono, varias líneas, Internet, seguridad en línea, respaldo en línea, protección de dispositivos, soporte técnico y transmisión de TV y películas.
* Información de la cuenta del cliente: cuánto tiempo ha sido cliente, contrato, método de pago, facturación electrónica, cargos mensuales y cargos totales.
* Información demográfica sobre los clientes: sexo, rango de edad y si tienen socios y dependientes

# Análisis exploratorio y prueba con ML tradicional

Las notebooks que contienen toda la información del análisis exploratorio y entrenamiento de los modelos de machine learning se pueden encontrar en la siguiente [carpeta](https://github.com/Adrok24/tp_digital_house/blob/version_1/ML/)

* El dataset presenta como variable target el Churn Status cuya distribución se ve en el siguiente gráfico.

<p align="center">
  <img src="https://github.com/Adrok24/tp_digital_house/blob/version_1/imagenes/image_1.png?raw=true" alt="grafico"/>
</p>

* El dataset tiene una forma de (7043, 21), no presenta outliers en sus valores y presenta blancos solo en 11 identificados como missing values de los 7043.

* Hay datos Sensibles los cuales se pueden o no tener en cuenta. Edad / Sexo en ocasiones no esta bien visto hacer recomendaciones utilizando esta informacion ya que puede ser visto como discriminación.

* Variables más significativas según modelo Random Forest:

1. Total Charges: El monto total cobrado al cliente
2. Tenure: Número de meses que el cliente ha
permanecido en la empresa.
3. Monthly change: El monto cobrado al cliente mensualmente

<p align="center">
  <img src="https://github.com/Adrok24/tp_digital_house/blob/version_1/imagenes/image_2.png?raw=true" alt="grafico"/>
</p>

* Variables que más correlacionan con variable objetivo:

1. Total Charges: El monto total cobrado al cliente
2. Tenure: Número de meses que el cliente ha permanecido en la empresa.

<p align="center">
  <img src="https://github.com/Adrok24/tp_digital_house/blob/version_1/imagenes/image_3.png?raw=true" alt="grafico"/>
</p>

* Probando con ensambles de árboles, el modelo que mejor resultados obtuvo fue el clasificador AdaBoost:

<p align="center">
  <img src="https://github.com/Adrok24/tp_digital_house/blob/version_1/imagenes/image_4.png?raw=true" alt="grafico"/>
</p>

* Comparación de resultados de una regresión logistica con una red neuronal simple de una sola neurona, con activación sigmoidea:

<p align="center">
  <img src="https://github.com/Adrok24/tp_digital_house/blob/version_1/imagenes/image_6.png?raw=true" alt="grafico"/>
</p>


# Deep Learing (NN)

Los resultados obtenidos para redes neuronales se pueden hallar en la siguiente [notebook](https://github.com/Adrok24/tp_digital_house/blob/version_1/neural_networks/NN_final.ipynb), aunque también se realizaron diversas pruebas que se pueden encontrar en la siguiente [carpeta](https://github.com/Adrok24/tp_digital_house/blob/version_1/neural_networks/).

<p  align="center">
  <img src="https://github.com/Adrok24/tp_digital_house/blob/version_1/imagenes/image_7.png?raw=true" width="300" height="400" alt="neural networks"/>
</p>

* Matriz de confusión y métricas obtenida para los datos de test.

<p align="center">
  <img src="https://github.com/Adrok24/tp_digital_house/blob/version_1/imagenes/image_8.png?raw=true" alt="matriz de confusión obtenida"/>
</p>
