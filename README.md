# Proyecto de Inteligencia Artificial

![Banner del Proyecto](banner.png)

## Objetivos del Proyecto

El objetivo principal de este proyecto es aplicar diferentes enfoques de Machine Learning (Supervisado y No Supervisado) sobre un conjunto de datos reales de comercio electrónico para extraer valor analítico y optimizar la toma de decisiones estratégicas de negocio.

### Objetivos Específicos:
1. **Análisis Exploratorio y Preprocesamiento:** Limpiar, transformar y escalar los datos, eliminando valores nulos o atípicos y analizando las correlaciones iniciales entre variables financieras y de rendimiento.
2. **Modelado de Regresión:** Evaluar algoritmos clásicos y redes neuronales para predecir variables continuas (como el `rating` de los productos) y entender las limitaciones del ruido subjetivo en los datos.
3. **Modelado de Clasificación:** Transformar el enfoque predictivo mediante la discretización de variables para catalogar productos en categorías de rendimiento (ej: Éxito vs. No Éxito).
4. **Segmentación Avanzada (Clustering):** Descubrir estructuras ocultas y perfiles comerciales naturales en el catálogo utilizando el algoritmo no supervisado **DBSCAN** centrado en el volumen de ventas (`quantity_sold`).

---

## Información del Dataset (Dataset Info)

El conjunto de datos utilizado corresponde a un catálogo de productos de una plataforma de E-commerce, el cual registra métricas de precios, descuentos, popularidad y volúmenes de comercialización.

* **Variables Principales Utilizadas:**
  * `actual_price` / `discount_percentage`: Variables financieras clave que influyen directamente en el comportamiento del consumidor.
  * `rating`: Calificación promedio otorgada por los usuarios (escala 1-5).
  * `review_count`: Cantidad de opiniones que respaldan la calificación de un producto.
  * `quantity_sold` (Variable Eje del Clustering): Volumen físico de unidades vendidas por artículo.

* **Procesamiento de Datos:**
  * Remoción de valores nulos, duplicados y columnas irrelevantes en la fase inicial.
  * Partición de datos bajo una estrategia **80% Entrenamiento / 20% Prueba** implementando un reordenamiento aleatorio (*Shuffle*).
  * Escalado de características numéricas mediante `StandardScaler`, garantizando la convergencia óptima de algoritmos sensibles a la magnitud como Máquinas de Soporte Vectorial (SVM) y Redes Neuronales Artificiales.

---

## Tecnologías y Modelos Implementados

A lo largo de las entregas del proyecto se desarrollaron y compararon las siguientes metodologías:

1. **Modelos Clásicos de Aprendizaje Supervisado:**
   * Árboles de Decisión (`DecisionTree`)
   * Bosques Aleatorios (`RandomForest`)
   * Máquinas de Soporte Vectorial (`SVM / SVR / SVC`)
2. **Validación Cruzada (Cross-Validation):** Evaluación robusta utilizando $K=10$ pliegues para garantizar la estabilidad de las métricas frente a datos no observados.
3. **Deep Learning:** Red Neuronal Perceptrón Multicapa (MLP) diseñada en TensorFlow/Keras para evaluar patrones complejos.
4. **Aprendizaje No Supervisado:** Reducción de dimensionalidad (PCA) y agrupamiento espacial basado en densidad con **DBSCAN** para identificar de forma matemática 4 franjas claras de tracción comercial en las ventas.

---

## 📺 Sustentación en Video

Puedes ver la explicación detallada del proceso, las gráficas obtenidas (matrices de correlación, curvas de error, dispersión de predicciones y clústeres de DBSCAN) y las conclusiones de negocio en nuestro video de YouTube:

🔗 **[Ver Video de Sustentación en YouTube]([https://www.youtube.com/](https://youtu.be/J_ZBdu1DYOc))**
