# Introducción

El notebook presenta una comparativa y análisis de resultados de dos técnicas de entrenamiento de modelos de ML. Por un lado, el entrenamiento por lotes (batch) que se encuentra en la librería [**scikit-learn**](https://scikit-learn.org/1.2/index.html); y por otro lado el entrenamiento en línea (online) que se encuentra en la librería [**river**](https://riverml.xyz/latest).

Para el entrenamiento se utiliza un dataset [Vehicle Insurance Claim Fraud Detection](https://www.kaggle.com/datasets/shivamb/vehicle-claim-fraud-detection) que emula una aplicación de la vida real de prevención de fraude.

Es importante destacar la importancia de utilizar este dataset ya que la inspiración para de esta comparativa surge de poder entender la diferencia de desempeño de las dos técnicas tomando en cuenta el *concept drift*.

## Concept drift

Para entender el *concept drift* se establece lo siguiente:

- *Concept* se entiende como la definición de la variable objetivo, en el caso del dataset, podríamos decir que el *concept* es la determinación de si una reclamación es fraudulenta o no.
- *Drift* entiendase como desplazamiento.

Por lo tanto, el *concept drift* es el desplazamiento del concepto, esto es, el cambio de definición de la variable objetivo. Este cambio de definición ocurre cuando la distribución de las variables predictoras que explican la variable objetivo cambian, ya se por la misma naturaleza de las variables o por cambios en el entorno.

En prevención particularmente, el *concept drift* ocurre frecuentemente, ya que los defraudadores tienden a cambiar sus conductas de modo que sea difícil poder detectarlos. Esto provoca que la definción del concepto cambie.

Para poder mitigiar los efectos causantes del *concept drift* se tienen las siguientes alternativas:

- Detección y modelado de los cambios de concepto: Esto requiere entender en que variables ocurre y porqué ocurre para poder determinar estrategías que modelen o mitiguen estos efectos.
- Entrenamiento en línea: Para esto se utiliza la librería **river**, que tiene una API similar a la de **scikit-learn** que permite entrenar tanto perdictores como preprocesadores con la información transmitida en línea.

# Librerías

Para poder correr el notebook adecuadamente se deben contar con las siguientes librerías y sus dependencias

1. `sklearn==1.2.2`
2. `river==0.22.0`
3. `xgboost==2.0.3`
4. `category_encoders==2.7.0`
5. `pandas==2.2.3`
6. `numpy==1.26.4`
