# Proyecto Churn de Clientes - Telecom X

## Descripción
Este proyecto analiza la **evasión de clientes (Churn)** en Telecom X. El objetivo es identificar patrones y factores que influyen en la cancelación del servicio, apoyando al equipo de Data Science en la creación de estrategias para retener clientes.

---

## Objetivos
- Explorar y limpiar datos obtenidos desde una fuente estructurada (DataFrame con información de clientes).
- Crear nuevas variables útiles para el análisis, como `Cuentas_Diarias` y `MonthlyCharges`.
- Transformar datos categóricos en numéricos o dummies para análisis y modelado.
- Realizar análisis exploratorio (EDA) para identificar patrones de churn según diversas variables.
- Generar visualizaciones estratégicas que faciliten la interpretación de los resultados.

---

## Dataset
Las columnas principales incluyen:
- `customerID` : Identificador único del cliente.
- `Churn` : Indica si el cliente abandonó el servicio (1) o no (0).
- `MonthlyCharges` : Facturación mensual del cliente.
- `TotalCharges` : Facturación total del cliente.
- `Cuentas_Diarias` : Facturación diaria promedio calculada a partir de `MonthlyCharges`.
- `Contract` : Tipo de contrato del cliente (`Month-to-month`, `One year`, `Two year`).
- `PaymentMethod` : Método de pago del cliente.
- `Gender` : Género del cliente.
- `SeniorCitizen` : Indicador de cliente senior (0 = No, 1 = Sí).
- `InternetService` : Tipo de servicio de internet contratado.

---

## Procesamiento de Datos
1. **Extracción y normalización** de columnas anidadas (`account`, `Charges`).
2. **Conversión de valores categóricos** (`Yes`/`No`) a numéricos (1/0).
3. **Cálculo de nuevas variables**:
   - `Cuentas_Diarias` = `MonthlyCharges` / 30
4. **Creación de variables dummy** para análisis de correlación y modelado.

---

## Análisis Exploratorio
- Distribución de churn por variables categóricas:
  - Género
  - Tipo de contrato
  - Método de pago
- Probabilidad de churn según tipo de contrato y otros factores.
- Visualizaciones:
  - Gráficos de barras de churn por categoría.
  - Scatter plots de `Churn` vs `MonthlyCharges` con línea de tendencia.
  - Comparación de facturación mensual entre clientes que abandonan y los que no.

---

## Resultados Clave
- Clientes con **contratos “Month-to-month”** presentan mayor probabilidad de churn.
- El **monto mensual promedio** de clientes que abandonan suele ser más alto que el de los que se quedan.
- Patrones interesantes según **método de pago, género y tipo de servicio de internet** permiten identificar perfiles de riesgo.

---

## Conclusión
El análisis permite a Telecom X:
- Visualizar claramente los factores que contribuyen al churn.
- Identificar clientes de alto riesgo y priorizar acciones de retención.
- Preparar los datos para futuros modelos predictivos que reduzcan la evasión.

---

## Herramientas y Librerías
- Python 3.x
- pandas
- matplotlib
- seaborn

---

## Autor
- RODRIGUEZ OLIVARES LUIS FELIPE
