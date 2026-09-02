
## PASOS PARA CONSTRUIR UN MODELO

1. Definir el tipo de modelo (puede ser un arbol de decision por ejemplo).
2. Entrenarlo. Capturar patrones de la data.
3. Predecir. 
4. Evaluar (que tan preciso es el modelo?).

La biblioteca mas usada para crear un modelo es **SCIKIT-LEARN**. 

`from sklearn.tree import DecisionTreeRegressor`

`melbourne_model = DecissionTreeRegressor(random_state = 1)`

`melbourne_model.fit(X, y)`

### UNDERFITTING Y OVERFITTING

Se suele buscar un equilibrio entre un **OVERFITTING** (en el caso de modelos basados en arboles, tener uno con una gran cantidad de hojas y pocos casos de analisis en las mismas) y un **UNDERFITTING** (caso contrario, pocas hojas y muchos casos, resultando en malas predicciones). 
Un recurso util para controlar esto es utilizar el atributo *max_leaf_nodes* al momento de crear un modelo 

Ej: `model = DecissionTreeRegressor(max_leaf_nodes = max_leaf_nodes, random_state = 0)`




