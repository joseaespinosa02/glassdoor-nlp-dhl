# Diagnóstico de marca empleadora — DHL Supply Chain vs. peers

Proyecto Modular 6 (NLP) · Máster en Data Science & IA · Evolve Academy

Análisis de reseñas de Glassdoor para identificar fortalezas y áreas de mejora de **DHL Supply Chain** como empleador frente a **UPS, FedEx, MAERSK, DB-Schenker y Kuehne+Nagel**.

## Metodología
1. Preparación y EDA (rating, recomendación, actuales vs. antiguos, antigüedad, evolución)
2. Control de calidad del sentimiento con `distilbert-base-uncased-finetuned-sst-2-english`
3. Topic modeling con BERTopic (un único modelo para pros y otro para cons, todas las empresas juntas)
4. Comparación con peers mediante balance neto (% pros − % cons)
5. Empleados actuales vs. antiguos (motivos de salida)
6. Matriz de priorización y recomendaciones para RRHH

## Decisiones clave
- Ventana común **jul-2018 → jun-2021**: DHL Supply Chain no tiene reseñas posteriores en el dataset.
- Máximo 2.000 reseñas por empresa (semilla 42) para que UPS no domine el modelo de topics.

## Cómo ejecutar
Abrir `Glassdoor_DHL_NLP.ipynb` en Google Colab (GPU) y subir `glassdoor_reviews_hr.parquet` (no incluido en el repo por tamaño, ~290 MB; dataset de D. Gauthier en Kaggle).
