# Detección de Fraudes

## Descripción del proyecto
En este proyecto se procede a identificar y predecir los datos fraudulentos mediante modelos de Machine Learning y aplicando la Ley de Benford.
El Dataset utilizado esta disponible en el repositorio de Kaggle [[Link]](https://www.kaggle.com/datasets/jainilcoder/online-payment-fraud-detection "Kaggle") y  en el archivo `dataset_fraud_detection.parquet`. 

## Objetivo
Identificar y predecir datos fraudulentos de la siguiente manera:
- Realizado un análisis de los datos para detectar comportamientos y características de los datos fraudulentos.
- Aplicando modelos de Machine Learning basados en aprendizaje supervisado, los cuales son entrenados para predecir posibles fraudes.
- Aplicando la Ley de Benford en la primera, segunda y tercera cifra de los datos, si los datos son fraudulentos, estos no se ajustan a esta ley.

## Resultados
**Análisis de los datos**:
Los datos fraudulentos se presentan constantes a traves del tiempo; pertenecen a las categorias CASH_OUT y TRANSFER; y su correlación es diferente a la correlación de los datos auténticos.

**ML - Aprendizaje Supervisado**:
De las variantes realizadas, el mejor predictor sigue la siguiente ruta:
1. balanceo de clases (mediante submuestreo).
2. ajuste a distribución normal y escalado RobustScaler y Standardscaler.
3. selección de características mediante RFECV y XGBClassifier como modelo y clasificador.

**Ley de Benford**:
La mejor manera de distinguir los datos fraudulentos es utilizar los datos previo balanceo de clases y aplicar la Ley de Benford en la segunda y tercer cifra.
Aplicar la Ley de Benford en la primera cifra no ayuda a distiguir entre los datos fraudulentos de los auténticos.

## Conclusión
Tanto los modelos de Machine Learning como la Ley de Benford tienen un nivel de acierto aceptable sin embargo, se puede seguir trabajando en variantes para buscar mejoras en las predicciones.

