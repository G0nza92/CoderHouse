# CoderHouse
Proyecto Final de Data Science II

# 📊 Telco Customer Churn Prediction

Proyecto final desarrollado para el curso **Data Science II: Machine Learning para la Ciencia de Datos**, con el objetivo de construir un modelo de Machine Learning capaz de predecir el abandono de clientes (*Customer Churn*) de una empresa de telecomunicaciones.

El proyecto desarrolla un flujo completo de Data Science, desde la comprensión del problema de negocio hasta la interpretación de un modelo mediante técnicas de Explainable AI (SHAP).

---

# 🎯 Objetivo

Desarrollar un modelo de clasificación que permita identificar clientes con alta probabilidad de abandonar el servicio, brindando información útil para que la empresa pueda implementar estrategias de retención y reducir la pérdida de clientes.

---

# 📂 Dataset

**Nombre:** Telco Customer Churn

**Fuente:** IBM Sample Dataset (disponible en Kaggle)

**Cantidad de registros:** 7.043 clientes

**Variable objetivo:** `Churn`

El dataset utilizado en este proyecto corresponde al archivo:

```text
Telco_Customer_Churn.csv
```

---

# 🛠️ Tecnologías utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* XGBoost
* SHAP

---

# 📌 Flujo del proyecto

El proyecto fue desarrollado siguiendo las siguientes etapas:

1. Definición del problema de negocio.
2. Carga y exploración del dataset.
3. Limpieza y preparación de los datos.
4. Análisis Exploratorio de Datos (EDA).
5. Ingeniería de atributos (Feature Engineering).
6. Preprocesamiento utilizando `ColumnTransformer` y `Pipeline`.
7. Entrenamiento de distintos modelos de clasificación.
8. Optimización de hiperparámetros mediante `GridSearchCV`.
9. Comparación de modelos utilizando diferentes métricas de evaluación.
10. Interpretación del **Random Forest optimizado** mediante SHAP para comprender la influencia de cada variable en las predicciones.
11. Elaboración de conclusiones.

---

# 🤖 Modelos evaluados

Durante el desarrollo del proyecto se entrenaron y compararon los siguientes modelos:

* Logistic Regression
* Decision Tree
* Random Forest
* Random Forest Optimizado (GridSearchCV)
* XGBoost

La comparación se realizó utilizando las siguientes métricas:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC

---

# 📈 Resultados

Los modelos fueron evaluados utilizando el mismo conjunto de entrenamiento y prueba.

| Modelo                       | Accuracy   | Precision  | Recall     | F1-Score   | ROC-AUC    |
| ---------------------------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| **Logistic Regression ⭐**    | **0.8041** | **0.6667** | **0.5241** | **0.5868** | **0.8460** |
| Random Forest (GridSearchCV) | 0.7970     | 0.6477     | 0.5160     | 0.5744     | 0.8440     |
| Random Forest                | 0.7871     | 0.6285     | 0.4840     | 0.5468     | 0.8210     |
| XGBoost                      | 0.7786     | 0.5969     | 0.5107     | 0.5504     | 0.8221     |
| Decision Tree                | 0.7339     | 0.4988     | 0.5348     | 0.5161     | 0.6701     |

El modelo con mejor desempeño fue **Logistic Regression**, obteniendo un **Accuracy de 80.41%** y un **ROC-AUC de 0.8460**, además de mantener el mejor equilibrio general entre las métricas evaluadas.

Si bien también se optimizó un modelo **Random Forest** mediante **GridSearchCV**, la mejora obtenida no fue suficiente para superar el rendimiento de la Regresión Logística.

**La interpretabilidad del modelo mediante SHAP se realizó sobre el Random Forest optimizado (GridSearchCV), ya que los modelos basados en árboles permiten analizar de forma más clara la contribución de cada variable a las predicciones.**

---

# 🔍 Principales hallazgos

A partir del análisis exploratorio y de la interpretación mediante SHAP sobre el **Random Forest optimizado**, se obtuvieron las siguientes conclusiones:

* Los clientes con menor antigüedad presentan una mayor probabilidad de abandonar el servicio.
* Los contratos mensuales están asociados con un mayor riesgo de churn.
* La permanencia del cliente (`tenure`) fue una de las variables con mayor influencia en las predicciones.
* El tipo de contrato y los cargos mensuales también tuvieron un impacto importante en el comportamiento del modelo.
* SHAP permitió interpretar el **Random Forest optimizado**, identificando las variables que más contribuyen a las predicciones y facilitando la comprensión del funcionamiento del modelo.

---

# 📁 Estructura del repositorio

```text
📦 Telco_Churn_Portfolio
│
├── Telco_Churn_GonzaloMatos.ipynb
├── Telco_Customer_Churn.csv
├── requirements.txt
├── README.md
└── images/
    ├── eda_churn.png
    ├── confusion_matrix.png
    ├── roc_curve.png
    └── shap_summary.png
```

---

# ▶️ Cómo ejecutar el proyecto

1. Clonar el repositorio.

```bash
git clone https://github.com/G0nza92/Telco_Churn_GonzaloMatos.git
```

2. Instalar las dependencias.

```bash
pip install -r requirements.txt
```

3. Abrir el notebook:

```text
Telco_Churn_Portfolio.ipynb
```

4. Verificar que el archivo **Telco_Customer_Churn.csv** se encuentre en el mismo directorio del notebook.

5. Ejecutar todas las celdas utilizando **Run All**.

---

# 💡 Aprendizajes

Durante este proyecto pude reforzar conocimientos sobre:

* Limpieza y preparación de datos.
* Análisis Exploratorio de Datos (EDA).
* Ingeniería de atributos.
* Construcción de Pipelines y ColumnTransformer.
* Entrenamiento y comparación de modelos de clasificación.
* Optimización mediante GridSearchCV.
* Interpretabilidad de modelos utilizando SHAP.

Este proyecto me permitió comprender el flujo completo de un problema de Machine Learning, desde el análisis inicial hasta la interpretación de los resultados obtenidos.

---

# 👨‍💻 Autor

**Gonzalo Matos**
