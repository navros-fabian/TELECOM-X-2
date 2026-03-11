
# 📊 Proyecto Telecom X — Análisis de Evasión de Clientes (Churn)

Este proyecto forma parte del Challenge 2 de Data Science del programa ONE (Oracle Next Education) junto con Alura Latam.
El objetivo es entender por qué los clientes abandonan Telecom X y preparar la base para un modelo que prediga la evasión.

## 📁 Dataset

| Dataset            | Fuente             | Formato | Registros |
|--------------------|-------------------|---------|-----------|
| TelecomX Customers | API pública GitHub | JSON    | 7.043     |


## 💡 Problema de Negocio
Telecom X tiene una tasa de evasión de 26%.
La pregunta clave es: ¿Por qué los clientes se van?

## Factores principales:

- Tipo de contrato (mes a mes vs anual)

- Método de pago

- Tiempo de permanencia

- Cargos mensuales

- Servicios contratados

## 🏗️ Metodología (ETL)
El trabajo se organizó en tres fases:

### 1. Extracción

- Descarga de datos desde la API pública.

- Normalización del JSON con pd.json_normalize().

### 2. Transformación

- Exploración de tipos y valores nulos.

- Limpieza de columnas de cargos.

- Traducción de variables al español.

- Creación de nuevas variables (ej. Cuentas_Diarias).

- Conversión de Churn a binario (1/0).

### 3. Carga y Análisis

- Estadísticas descriptivas.

- Visualizaciones de distribución.

- Matriz de correlación.

📊 Resultados
- Tasa de evasión: ~26% (1 de cada 4 clientes).

- Tipo de contrato: mes a mes = mayor riesgo.

- Tiempo de permanencia: menos meses = más probabilidad de irse.

- Cargos mensuales: clientes con pagos más altos tienden a evadir.

- Método de pago: cheque electrónico = mayor riesgo; pagos automáticos = menor riesgo.

- Género: no influye en la evasión.

🎯 Recomendaciones
1. Incentivar contratos anuales o bianuales.

2. Monitorear clientes con menos de 6 meses de permanencia.

3. Promover pagos automáticos con beneficios.

4. Revisar planes premium para asegurar valor percibido.

5. Construir un modelo predictivo usando las variables clave.
