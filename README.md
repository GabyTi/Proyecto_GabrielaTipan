# Proyecto_GabrielaTipan

Trabajé en un proyecto sobre muestras de cáncer de mama de Wisconsin. Hice una
implementación de 4 modelos para predecir si un paciente tiene cáncer o no lo tiene.
Luego, a través de un análisis de precisión y de matrices de confusión pude identificar
cual es el mejor modelo predictorio que utilicé en este caso.

El dataset que utilicé es wdbc.data y la información necesaria la tomé del archivo 
wdbc.names.

Primero realicé el preprocesamiento del dataset con el objetivo de obtener un conjunto de 
datos de buena calidad y así evitar contenido que no me aporte en mi predicción.
Detallo a continuación la limpieza realizada:

1. El dataset no tenía encabezado, por lo cual agregué cabeceras para cada columna.
2. Los cambios realizados los guardé en otro archivo idéntico al inicial para no perder la información original (wdbc2.csv)
3. Verifiqué valores nulos
4. Analicé cual es mi variable predictoria y al identificar que esta era de tipo object(string) la transformé
en tipo int.
5. Eliminé la primera columna "id" ya que no me aportaba en nada a mi predicción.
6. Confirmé que los cambios realizados fueran exitosos.

Al tener listo mi dataset realicé una matriz de correlación para identificar las variables que son de 
importancia y se relacionan entre sí. Preparé mis datos para train y test y elegí los siguientes modelos
para realizar mi predicción:

Modelo1: SGDClassifier
Modelo2: RandomForest
Modelo3: Kneighbors
Modelo4: SUPPORT VECTOR MACHINE

Después de obtener y analizar mis resultados de predicción, matriz de confusión y precisión 
considero que el mejor modelo de los 4 utilizados, para este proyecto, es SGDClassifier ya que me dio 
4 falsos negativos lo que permitió obtener un valor de precisión de 0.97 
A pesar de tener 1 falso positivo en este modelo, es el que menor número de falsos negativos tiene.
