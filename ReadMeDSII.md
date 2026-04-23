# Proyecto Data Science II — Predicción de Trastornos del Sueño

Este proyecto analiza un dataset de hábitos de sueño, salud y estilo de vida para predecir el tipo de trastorno del sueño mediante Machine Learning. Incluye EDA, preprocesamiento, modelos, optimización e interpretabilidad.

---

## Correcciones aplicadas (según feedback docente)

- Winsorización de outliers en Frecuencia Cardíaca (percentiles 1–99).
- Aclaración: los puntos restantes en boxplot son outliers estadísticos, no valores extremos reales.
- Boxplots reorganizados priorizando análisis univariado.
- Título del proyecto corregido.
- Conclusiones ampliadas y alineadas con el análisis.
- Se agregó toda la sección de ML:
  - Logistic Regression
  - Random Forest
  - Validación cruzada
  - GridSearchCV
  - Matriz de confusión
  - SHAP global
- Comparación real entre modelos: Random Forest optimizado supera a Logistic Regression.

---

## EDA — Principales hallazgos

- Menos horas de sueño → mayor estrés.
- BMI elevado → mayor probabilidad de apnea.
- Frecuencia cardíaca y presión arterial distinguen bien entre clases.
- No hay valores faltantes.
- Nuevas variables creadas: Categoría_Sueño, Grupo_Edad, OMS_Status.

---

## Modelado Predictivo

- Modelos base: Logistic Regression y Random Forest.
- Ambos tuvieron accuracy similar (~0.89).
- Tras optimización, Random Forest alcanzó ~0.9035, siendo el mejor modelo.
- Mejor estabilidad, mejor matriz de confusión y mejor desempeño en clases minoritarias.

---

## Interpretabilidad (SHAP)

Variables más influyentes:

- Horas de sueño
- Nivel de estrés
- Frecuencia cardíaca
- BMI
- Presión arterial

Los patrones coinciden con evidencia clínica.

---

## Conclusiones

- Random Forest optimizado es el mejor modelo para este dataset.
- El análisis confirma que factores fisiológicos y de estilo de vida influyen en la calidad del sueño.
- El proyecto cubre todo el pipeline de Data Science.

---

## Limitaciones

- Dataset pequeño
- Variables autorreportadas
- Falta de datos clínicos avanzados

---

## Próximos pasos

- Incorporar más datos fisiológicos
- Probar XGBoost / LightGBM
- Implementar pipeline reproducible
- Evaluar balanceo si se amplía el dataset
