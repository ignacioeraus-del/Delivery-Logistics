# Delivery-Logistics
## 1. Contexto y objetivo del proyecto 
Análisis de tiempos de entrega y tasas de fallo en una red de distribución logística con diferentes partners de entrega, con el objetivo de identificar que     factores (delivery_partner, clima, distancia) influyen en el rendimiento de las entregas
## 2. Fuente de datos
- Dataset "Delivery Logistics Dataset (India - Multip-Partner)" de Kaggle, ~25.000 resgistros de entregas con variables de transportista, tipo de vehículo, clima, distancia, coste y estado de entrega.
`https://www.kaggle.com/datasets/kundanbedmutha/delivery-logistics-dataset-india-multi-partner`
## 3. Limpieza y preparación de datos
- Se detecta que las columnas `delivery_time_hours` y `expected_time_hours` se importaban incorrectamente como fechas. Solucionado a traves de Power Query forzando el tipo de columna a texto, extrayendo los últimos 9 caracteres y cambiando de nuevo el tipo de columna a número entero.
- Se identifica que ~500 registros tenían valores de `delivery_id` corruptos y duplicados. Se genera una columna índice mediante Power Query para garantizar la trazabilidad de cada registro.
- Se ajusta el delimitador de importación (`;` en lugar de `,`) por la configuración de Excel.
## 4. Herramientas utilizadas
- Excel + Power Query (limpieza), SQLite + DBeaver (análisis SQL)
## 5. Preguntas de negocio respondidas
### ¿Qué transportista tiene mayor tasa de fallos?
- DHL (5.92%) seguido de XpressBees (5.91%)
  
