# Challenge-Telecom-X-an-lisis-de-evasion-de-clientes
TelecomX — Análisis de Evasión de Clientes (Churn)

## 1. Propósito del Análisis
TelecomX enfrenta un problema crítico: una parte significativa de sus clientes abandona la empresa. Este fenómeno se conoce como Churn y representa una pérdida directa de ingresos.

El objetivo de este análisis es identificar qué factores están asociados a la evasión de clientes, respondiendo preguntas como:

¿Qué tipo de contrato tienen los clientes que más se van?
¿El servicio de internet influye en la decisión de abandonar?
¿Los clientes nuevos son más propensos al Churn?
¿Existe relación entre el costo mensual y la evasión?
Con base en los hallazgos, se emite una recomendación para que TelecomX pueda orientar sus estrategias de retención.

## 2. Estructura del Proyecto
telecomx/
│
├── TelecomX_LATAM.ipynb       # Notebook principal con el proceso ETL y el análisis
├── TelecomX_Data.json         # Datos fuente en formato JSON (estructura anidada)
├── TelecomX_diccionario.md    # Diccionario con la descripción de cada variable
└── README.md                  # Este archivo
El notebook sigue un proceso ETL completo dividido en cuatro secciones:

Extracción: carga del JSON desde la API de GitHub con requests
Transformación: aplanamiento del JSON anidado, limpieza de tipos y valores nulos
Carga y análisis: visualizaciones exploratorias sobre las variables más relevantes
Informe final: resumen numérico y conclusiones con recomendaciones
## 3. Gráficos e Insights Obtenidos
Tasa general de Churn
Gráfico de torta mostrando la proporción de clientes que abandonaron vs. los que se quedaron.

Insight: Aproximadamente 1 de cada 4 clientes abandona la empresa, una tasa considerablemente alta para el sector.

Churn por tipo de contrato
Barras horizontales comparando la tasa de evasión según el tipo de contrato (mes a mes, anual, bianual).

Insight: Los clientes con contrato mes a mes se van a una tasa mucho mayor que los que tienen contratos a largo plazo. La ausencia de compromiso facilita la salida.

Churn por tipo de servicio de internet
Comparativa entre clientes con DSL, fibra óptica y sin internet.

Insight: Los clientes con fibra óptica, a pesar de pagar más, presentan la mayor tasa de evasión. Esto sugiere una brecha entre el precio cobrado y la experiencia percibida.

Distribución de permanencia (tenure) según Churn
Histograma superpuesto mostrando cuántos meses llevan los clientes en la empresa al momento de irse o quedarse.

Insight: La mayoría de los clientes que abandonan lo hacen durante los primeros 12 meses. La etapa inicial del contrato es la más crítica para la retención.

Cargo mensual promedio según Churn
Barras comparando el gasto mensual promedio entre clientes que se fueron y los que se quedaron.

Insight: Los clientes que abandonaron pagaban en promedio más por mes, lo que refuerza que la percepción de valor es un factor determinante en la decisión de salida.

## 4. Instrucciones para Ejecutar el Notebook
Opción A — Google Colab (recomendado, sin instalación)
Descarga el archivo TelecomX_LATAM.ipynb
Entra a colab.research.google.com
Haz clic en Archivo → Subir notebook
Selecciona el archivo descargado
Ejecuta todas las celdas con Ctrl + F9
Los datos se cargan automáticamente desde GitHub. Solo necesitas conexión a internet.

# Opción B — Localmente con Jupyter
Requisitos previos:

## pip install pandas matplotlib requests jupyter
Pasos:

### 1. Clona este repositorio
git clone https://github.com/tu-usuario/telecomx.git

### 2. Entra a la carpeta
cd telecomx

### 3. Abre el notebook
jupyter notebook TelecomX_LATAM.ipynb

