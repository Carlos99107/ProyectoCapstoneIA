# ProyectoCapstoneIA
Predicción de Abandono de Clientes

Descripción del problema y la solución

-El abandono de clientes (churn) representa uno de los principales desafíos estratégicos en el sector retail, especialmente en escenarios donde la pérdida de clientes no se produce por cancelación explícita, sino por la disminución progresiva de la actividad de compra. En el caso de Corporación Favorita, se identificó una tasa aproximada del 40% de abandono dentro de sus programas de fidelización, definido como la inactividad de compra durante un período continuo de cuatro meses

-Este proyecto propone el desarrollo de un sistema de inteligencia artificial capaz de predecir la probabilidad de abandono de los clientes, utilizando datos transaccionales históricos y variables de comportamiento como recencia, frecuencia y gasto. La solución permite anticipar comportamientos de deserción y generar información analítica que apoye la toma de decisiones del área comercial para implementar estrategias de retención más efectivas

-El modelo final implementado corresponde a un enfoque híbrido basado en técnicas de Machine Learning, incluyendo XGBoost, Random Forest y una arquitectura de stacking, logrando un desempeño robusto con métricas como AUC de 0.935 y recall de 0.79 en la clase de abandono

⚙️ Requisitos técnicos y dependencias

Para la ejecución del proyecto se requiere el siguiente entorno:

🖥️ Lenguaje
Python 3.8 o superior
📦 Librerías principales
pandas
numpy
scikit-learn
xgboost
matplotlib
seaborn
🧪 Librerías opcionales (explicabilidad y análisis)
shap
imbalanced-learn
⚙️ Entorno recomendado
Jupyter Notebook / JupyterLab
VS Code / PyCharm

☁️ Entorno de ejecución (GCP)

El proyecto fue desarrollado y ejecutado en Google Cloud Platform (GCP) debido a la naturaleza confidencial de los datos de la empresa.

🔐 Consideraciones
Los datos utilizados son privados y no pueden ser compartidos públicamente
El acceso al dataset está restringido a entornos autorizados dentro de la organización
La ejecución del pipeline requiere permisos sobre recursos en GCP
🧱 Servicios utilizados (referencial)
Google Compute Engine / Vertex AI (entorno de ejecución)
Cloud Storage (almacenamiento de datos)
Jupyter Notebook (entorno de análisis)

▶️ Instrucciones de ejecución
⚠️ Nota importante

Debido a la confidencialidad de la información, este proyecto no puede ser ejecutado completamente fuera del entorno GCP de la empresa. Sin embargo, el flujo general es el siguiente:

🔹 1. Acceso al entorno GCP
Ingresar al entorno autorizado de la empresa
Acceder a la instancia de cómputo o notebook asignado
🔹 2. Carga de datos
Los datos se encuentran almacenados en:
Cloud Storage o repositorio interno
Dataset incluye:
variables transaccionales
variables RFM
variable objetivo (churn)


## 🔁 Reproducibilidad académica del proyecto

Debido a la confidencialidad de los datos reales y al uso de un entorno corporativo en GCP,
la ejecución productiva completa del proyecto no es pública.

No obstante, el proyecto ha sido diseñado siguiendo principios de reproducibilidad,
por lo que:

✅ El pipeline completo (preprocesamiento, feature engineering, modelado y evaluación)
puede ejecutarse con cualquier dataset que respete el esquema definido.

✅ Para fines académicos, el flujo del proyecto es reproducible utilizando
un dataset sintético o anonimizado que replica la estructura y distribución
estadística de los datos reales, sin exponer información sensible.

✅ Las métricas, validaciones y comportamiento del modelo son independientes
del origen de los datos, permitiendo validar correctamente la implementación técnica.

De esta forma, el proyecto cumple con criterios de reproducibilidad académica,
manteniendo el cumplimiento de las políticas de confidencialidad de la organización.

Se realizó la extracción de un sample de los datos con 2000 filas y datos anonimizados para la recreación del modelo
Datos:
https://udlaec-my.sharepoint.com/:x:/r/personal/victor_gomez_udla_edu_ec/Documents/Proyecto_Capstone_Mart%C3%ADnez_Solano_Calder%C3%B3n/Tabla_Exportar.csv?d=w8aafb401efd94f51ba69a991fbe16a27&csf=1&web=1&e=BgZC3f

 Ejecución
- Usa dataset sintético o anonimizado
- Ejecutable en local o Colab
- Reproduce el pipeline completo


🔹 3. Ejecución del pipeline
Ejecutar notebooks o scripts en el siguiente orden:

1. data_preparation.ipynb
2. feature_engineering.ipynb
3. modeling.ipynb
4. evaluation.ipynb

🔹 4. Resultados generados
Probabilidad de abandono por cliente
Segmentación de riesgo
Métricas del modelo:
AUC
Recall
F1-score
Visualizaciones:
matriz de correlación
importancia de variables
distribución de churn


🔄Explicación general del pipeline

El proyecto sigue el enfoque metodológico CRISP-DM, estructurando el desarrollo en fases analíticas claras:

1. Comprensión del negocio

Definición del problema de churn (4 meses sin compra)
Alineación con objetivos del área comercial

2. Preparación de datos

Limpieza y depuración de datos
Construcción de variables:
Recencia (días desde última compra)
Frecuencia de compra
Gasto total
Generación de variable objetivo (churn)

3. Modelado

Implementación de modelos:
XGBoost
Random Forest
Redes neuronales
Construcción de modelo stacking
Validación cruzada para estabilidad

4. Evaluación

Métricas utilizadas:
AUC
Recall
Precisión
F1-score
Comparación entre modelos

5. Resultados

Predicción de probabilidad de abandono
Segmentación de clientes por nivel de riesgo
Análisis de variables influyentes (ej. recencia como predictor clave)
📊 Resultados clave
AUC: 0.935
Recall (churn): 0.79
Variables más importantes:
Recencia
Frecuencia
Gasto

El modelo demuestra alta capacidad para identificar clientes en riesgo, permitiendo su uso como herramienta de soporte para decisiones comerciales estratégicas.

Conclusión

Este proyecto desarrolla una solución robusta de inteligencia artificial aplicada al negocio retail, combinando técnicas avanzadas de Machine Learning con un enfoque orientado a la toma de decisiones. La implementación permite transformar datos transaccionales en información accionable, facilitando la identificación temprana de clientes en riesgo de abandono y fortaleciendo las estrategias de fidelización.
