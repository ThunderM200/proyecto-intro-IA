# Proyecto Introducción a la inteligencia artificial.

Primer proyecto del curso introducción a la inteligencia artificial.

Se trabaja con el dataset ['santander-customer-satisfaction'](https://www.kaggle.com/competitions/santander-customer-satisfaction/code).

## Dependencias
En el proyecto se usan las librerías especificadas en `requirements.yaml`; pandas, numpy, matplotlib, seaborn, scikit-learn y kagglehub.

El problema planteado para el dataset es la predición de la satisfacción de clientes a través del uso de multiples modelos de clasificación; Regresión lineal, regresión logística, Naive Bayes, K-nearest neighbors, decision trees y random forest, evaluando el rendimiento de cada modelo antes y después de la aplicación de PCA.

> [!NOTE]
> El dataset utilizado viene previamente preparado desde el origen, por lo que ya están predefinidos los conjuntos de entrenamiento y de prueba, pero el archivo con los datos de prueba no es útil para el analisis que se realiza, así que se trabaja únicamente con el archivo train.csv. (Y sí, tuve que buscar como se hacen las anotaciones)

> [!NOTE]
> Buscando más información y viendo como los modelos clasifican datos, en realidad voy a usar Regresión logística, decision trees y random forest porque son los que mejor se ajustan a este dataset.

---

## Código

- El código realiza la eliminación de la columna `ID`.

- La separación de variables de predicción y de objetivo.

- Estandarización de los datos usando `StandardScaler`

- PCA conservando el 95% de la varianza.

Luego de eso se realiza el analisis de los modelos de clasificación, cuyos resultados se detallan más abajo.

---

## Modelos trabajados


Se trabajó con tres algoritmos de clasificación:

- Regresión logística.
- Árboles de decisión.
- Random Forest.

Cada modelo fue evaluado en dos escenarios:

1. Utilizando todas las variables originales.
2. Aplicando PCA para reducir la dimensionalidad.

El randomstate utilizado es `33550336`.

---

## Análisis exploratorio y visualización

Se realizaron las siguientes visualizaciones:

- mapa de calor de correlaciones;
- porcentaje de varianza explicada por PCA;
- varianza acumulada;
- curvas ROC;
- matrices de confusión.

---

## Metricas de evaluación

Para comparar los modelos se utilizaron:

- Accuracy.
- F1-Score.
- ROC-AUC.
- Matriz de confusión

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

## Conclusiones

Aunque Random Forest obtuvo el mayor accuracy, la regresión logística presentó un mejor equilibrio entre sensibilidad y capacidad de discriminación, reflejado en sus valores de F1-Score y ROC-AUC.

La aplicación de PCA no produjo mejoras significativas y, en algunos casos, redujo el rendimiento de los modelos.

Por ello, la regresión logística sin PCA resultó ser la alternativa con mejor desempeño para este problema.

Especialmente sabiendo que si decía satisfecho a todo, estaría correcto aproximadamente el 95% del tiempo.

