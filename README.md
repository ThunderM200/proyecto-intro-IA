# Proyecto Introducción a la inteligencia artificial.

Primer proyecto del curso introducción a la inteligencia artificial.

Se trabaja con el dataset ['santander-customer-satisfaction'](https://www.kaggle.com/competitions/santander-customer-satisfaction/code).

El problema planteado para el dataset es la predición de la satisfacción de clientes a través del uso de multiples modelos de clasificación; Regresión lineal, regresión logística, Naive Bayes, K-nearest neighbors, decision trees y random forest, evaluando el rendimiento de cada modelo antes y después de la aplicación de PCA.

> [!NOTE]
> El dataset utilizado viene previamente preparado desde el origen, por lo que ya están predefinidos los conjuntos de entrenamiento y de prueba. (Y sí, tuve que buscar como se hacen las anotaciones)

> [!NOTE]
> Buscando más información y viendo como los modelos clasifican datos, en realidad voy a usar Regresión logística, decision trees y random forest porque son los que mejor se ajustan a este dataset.

---

## De acuerdo a los resultados obtenidos, aquí detallados:

### Regresión logística:

|Métrica        |Sin PCA    |Con PCA|
|---------------|-----------|-------|
|Accuracy       |  0.7030   |0.7026|
|F1-Score       |  0.1659   |0.1660|
|ROC-AUC        |  0.7964   |0.7919|

### Decision trees:

|Métrica         |Sin PCA    |Con PCA|
|-----------------|----------|------|
|Accuracy         |0.9201    | 0.8957|
|F1-Score         |0.0515    | 0.0758|
|ROC-AUC          |0.5052    | 0.5180|

### Random forest:

|Métrica         |Sin PCA    |Con PCA|
|---------------|----------|------|
|Accuracy       |  0.9515  |   0.9603|
|F1-Score       |  0.0844  |   0.0000|
|ROC-AUC        |  0.7377  |   0.6695|

---

Tenemos que el que mejor rendimiento se obtuvo al trabajar con regresión logística, antes y después de aplicar analisis por PCA.

## Conclusiones

Mientras trabajaba en el proyecto y buscaba información respecto a los modelos de clasificación y las métricas que se usan, esperaba que random forest fuera el mejor modelo entre los que usé. 

Pero las métricas que obtuve mientras trabajaba mostraron que la regresión logística fue la mejor de los tres modelos.

