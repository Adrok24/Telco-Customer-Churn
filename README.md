# Análisis de un data set de Telco Customer Churn y entrenamiento de un modelo predictivo por diferentes métodos.

https://www.kaggle.com/blastchar/telco-customer-churn


# Motivación y dataset

La motivación es predecir el comportamiento para retener clientes. Poder analizar todos los datos relevantes de los clientes y desarrollar programas de retención de clientes.

* Cada fila representa un cliente, cada columna contiene los atributos del cliente descritos en la columna Metadatos.
* El conjunto de datos incluye información sobre:
* Clientes que se fueron en el último mes: la columna se llama RenunciaServicios a los que cada cliente se ha suscrito: teléfono, varias líneas, Internet, seguridad en línea, respaldo en línea, protección de dispositivos, soporte técnico y transmisión de TV y películas.
* Información de la cuenta del cliente: cuánto tiempo ha sido cliente, contrato, método de pago, facturación electrónica, cargos mensuales y cargos totales.
* Información demográfica sobre los clientes: sexo, rango de edad y si tienen socios y dependientes

# Análisis exploratorio

* El dataset presenta como variable target el Churn Status cuya distribución se ve en el Gráfico 1.

* El dataset tiene una forma de (7043, 21), no presenta outliers en sus valores y presenta blancos solo en 11 identificados como missing values de los 7043.

* Hay datos Sensibles los cuales se pueden o no tener en cuenta. Edad / Sexo en ocasiones no esta bien visto hacer recomendaciones utilizando esta informacion ya que puede ser visto como discriminación.

