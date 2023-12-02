# PLN_PROYECTO_AlanJafetLeonLoeza

Este proyecto consiste en cuatro etapas principales:
1.	EDA.
2.	Creación de un analizador de sentimientos.
3.	Creación de modelos de ML para realizar predicciones.

ETAPA 1: ANÁLISIS EXPLORATORIO DE LOS DATOS.
Paso 1. Importe las librerías necesarias (pandas, numpy, seaborn, nltk, etc...)
Paso 2. Cargue y muestre información del dataset; muestre información estadística de las columnas numéricas.
Paso 3. Identifique los datos nulos: muestre las filas que contienen datos nulos (no se deben tratar aún).
Paso 4. Muestre la distribución de la columna "Rating", haga un análisis de la distribución.
Paso 5. Identifique si alguna de las columnas se puede convertir en categórica.

ETAPA 2: ANÁLISIS DE SENTIMIENTOS.
Paso 1. Muestre las primeras 10 filas del dataset con las columnas "Rating" y "Review", haga un análisis rápido de esa información.
Paso 2. Haga una función que se encargue del pre-procesamiento:
- Genere los tokens.
- Filtre las palabras de parada.
- Obtenga el lema de las palabras y guárdelo en una lista.
- Retorne la lista en forma de una cadena, para ello debe unir los elementos de la lista mediante un espacio.
Paso 3. Aplique la función creada para obtener el lema de las columnas "Review" y "Title", guárde el resultado en nuevas columnas dentro del dataframe original (por ejemplo: "ReviewText", "TitleText").
Paso 4. Haga una función para obtener el sentimiento de las palabras, para ello puede utilizar el SentimentIntensityAnalizer() y su función "polarity_scores()". Al final debe retornar el puntaje de sentimiento.
Paso 5. Aplique la función creada para obtener el sentimiento en las columnas creadas en el paso 3, guarde el resultado en un par de columnas nuevas (por ejemplo: "ReviewSentiment", "TitleSentiment").
Paso 6. Prepare un dataframe con las columnas originales + las columnas creadas previamente, tendrían que haber 8 columnas, 3 de ellas deben ser numéricas (incluyendo "Rating").

ETAPA 3: MACHINE LEARNING.
Paso 1. Asigne a la variable X las columnas numéricas menos "Rating"; asigne a la variable y la columna "Rating", seleccione únicamente las filas sin datos nulos (no elimine ni trate las filas con datos nulos, esas se usarán para predecir)
Paso 2. Divida en una muestra de entrenamiento y en una muestra de pruebas, estratifique en base a la proporción de la variable objetivo. El tamaño de la muestra para entrenamiento debe ser del 85%. Asigne una semilla para poder reproducir los resultados.
Paso 3. Entrene los siguientes modelos:
- KNN para clasificación
- SVM para clasificación
- RandomForest para clasificación
Paso 4. Evalúe el rendimiento de los modelos (puede usar accuracy) creados en el paso previo, muestre las predicciones realizadas y compare con las etiquetas reales.
Paso 5. Debido a que este es un problema de clasificación, pero hay varias clases que son originalmente numéricas, se puede aplicar también una métrica de evaluación para regresión. Aplique el RMSE a las predicciones y las etiquetas reales, analice el resultado.
Paso 6. Utilice el modelo que se comportó mejor para predecir el "Rating" de las filas que tienen ese dato nulo, revise manualmente si la calificación predicha es consistente con el comentario en la reseña.
Paso 7. Escriba sus conclusiones al respecto.
