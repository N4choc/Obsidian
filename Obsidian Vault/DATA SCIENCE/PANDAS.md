Dataframe: muestra la data que puede verse de forma tabular (tabla). Es un tipo de dato especial de esta libreria. 

# FORMAS DE OBTENER UN SUBCONJUNTO DE LA DATA

### PREDICTION TARGET 
Se hace mediante la notacion de punto. El resultado es obtener una columna del dataframe y alojarlo en una variable. Esta columna sera guardada como una *SERIES*, la cual es simplemente un dataframe pero de una columna. 

A esta columna se la llamara **PREDICTION TARGET** y por convencion, el nombre de la variable suele ser **'y'**.

`y = melbourne_data.price`  <- retorna la columna 'price' del dataframe

### ELIGIENDO 'FEATURES'
Las columnas que terminan siendo inputs para el modelo son llamadas *features*. Por convencion, las variables suelen ser llamadas **'X'**.

`X = melbourne_data['Rooms', 'Bathroom', 'Landsize', 'Lattitude', 'Longtitude']`

### ERRORES Y TESTEO DE MODELOS
La metrica mas basica para medir el error de un modelo es la estadistica llamada **MAE** (median absolute error). La cual consiste entre la diferencia del valor actual menos el predecido. A eso sacarle el valor absoluto, y luego sacar una media de todos ellos. 

NOTA: es muy importante no utilizar la misma data para tanto entrenar como testear el algoritmo, porque si no es obvio que va a arrojar algo similar o igual a la data usada en su entreno. Para testearlo, se deberia usar data que nunca ha visto antes. 


### INDEXACION
Pandas tiene sus propios metodos para indexar, los cuales son *loc* y *iloc*. Estos son mucho mas útiles para cosas mas complejas que simplemente acceder a un indice mediante atributos (dot notation) o keys de un diccionario (por arrays). 

loc y iloc son row first, column second. Cuando en python nativo es primero columnas, luego filas 

`reviews.iloc[:, 0]` traera todas las filas con sus valores de la primera columna. 

Es decir, iloc se maneja a traves de indices. 

En el caso de loc, se maneja a traves de labels

Ej: `reviews.loc[:, ['taster_name', 'taster_twitter_handle', 'points']]`

El metodo `isin()` de pandas permite iterar sobre el dataframe, buscando valores que coincidan con los pasados en un array como argumento. `isin(['Venezuela', 'Bolivia'])`


### MAPPING
Es muy similar al metodo de javascript. Consiste en recorrer un set de datos y obtener otro. 

`review.points.map(lamda p: p - review_points_mean)`

*map* retorna una serie, mientras que *apply* retorna un dataframe. 

En el caso de que se quiera hacer una cuenta o transformacion especifica, es recomendable utilizar el siguiente codigo: 

`reviews.points -= reviews.points.mean()`