# Supply-Chain-Freight-Prediction
Modelo predictivo de Machine Learning (Random Forest y Gradient Boosting) para estimar los fletes marítimos globales (Baltic Dry Index) a partir de variables macroeconómicas mediante APIs en tiempo real.


Este repositorio contiene un proyecto final de analítica predictiva enfocado en el sector logístico y macroeconómico. El objetivo principal es modelar y predecir el comportamiento de los fletes marítimos globales utilizando como proxy el **Baltic Dry Index (BDI)** a partir de variables macroeconómicas clave, tasas de interés y choques geopolíticos históricos.

El proyecto implementa un flujo completo de Ciencia de Datos: extracción autónoma mediante APIs, ingeniería de variables, análisis exploratorio de datos (EDA) y entrenamiento comparativo de modelos de ensamble (*Ensemble Learning*).

## 📊 Estructura del Portafolio Técnico

Con la adición de este proyecto, mi portafolio transiciona hacia un perfil integral de datos:
1. **Analítica Descriptiva y BI:** Proyecto de exploración de datos COVID-19 utilizando **SQL** para la manipulación profunda y **Power BI** para el despliegue de tableros interactivos corporativos.
2. **Analítica Predictiva y Machine Learning (Este Repositorio):** Modelado predictivo avanzado utilizando **Python**, consumo de APIs financieras en tiempo real y algoritmos supervisados de Machine Learning.

---

## 🗂️ Arquitectura del Conjunto de Datos

El modelo no depende de archivos estáticos rígidos; el script está automatizado para consumir datos actualizados directamente de las APIs de **Yahoo Finance** y la **FRED (Federal Reserve Economic Data)**. Las variables consolidadas en el dataset final (`Dataset_SupplyChain_Macro.csv`) son:

*   **Variable Objetivo:** `Fletes_BdryETF` (Proxy del Baltic Dry Index a través de ETF financiero).
*   **Variables Macroeconómicas:** Precio del Crudo Brent (`Petroleo_Brent`), Índice de Precios al Consumidor (`CPIAUCSL`) y la Tasa de Fondos Federales (`FEDFUNDS`).
*   **Variable de Entorno:** Indicador binario para capturar la volatilidad por `Shock_Geopolitico`.

---

## ⚙️ Fase de Entrenamiento y Metodología

El desarrollo predictivo se estructuró bajo un enfoque de validación **Hold-Out (80% Entrenamiento / 20% Prueba)**, garantizando una evaluación fuera de la muestra robusta frente a datos no observados históricamente.

Se evaluaron y compararon dos de los algoritmos de ensamble más potentes de la literatura de aprendizaje supervisado:
1.  **Random Forest Regressor:** Ensamble por *Bagging* enfocado en la reducción de varianza mediante el promedio de múltiples árboles de decisión independientes construidos mediante *Bootstrap*.
2.  **Gradient Boosting Regressor:** Ensamble por *Boosting* secuencial enfocado en la reducción del sesgo mediante la corrección iterativa de los residuos del árbol anterior utilizando descenso de gradiente.

### Métricas de Rendimiento Evaluadas
*   **Coeficiente de Determinación ($R^2$):** Medida de la proporción de la varianza explicada por el modelo.
*   **Raíz del Error Cuadrático Medio ($RMSE$):** Magnitud promedio del error de predicción expresada en unidades monetarias reales (USD), penalizando errores grandes.

---

## 🛠️ Tecnologías Utilizadas

*   **Lenguaje:** Python 3.x
*   **Entorno:** Jupyter Notebook (Anaconda Toolbox)
*   **Librerías Clave:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn, YFinance.


