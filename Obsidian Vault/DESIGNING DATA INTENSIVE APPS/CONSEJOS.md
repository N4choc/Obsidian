Una app deberia ser tolerante a fallos individuales, es decir, si alguna parte de la app (sea alguna dependencia externa o algun componente especifico de la misma) falla, la app deberia ser capaz de seguir funcionando y proveyendo el resto de servicios. 

Una buena metrica para medir el tiempo de respuesta (response-time) y el rendimiento (throughput) es utilizar recursos estadisticos como la mediana, los percentiles y la media.

Es ideal buscar la abstraccion y la simplicidad al momento de desarrollar software

## Declarative query languages 

Especificas el patron de data que queres (SQL, CYPHER), pero sin el como conseguir esa meta

## ORM

Los **ORM** suelen utilizarse con sistemas OLTP. 
Para relaciones "one to few" (few para cuando realmente no son muchos, como el historial de trabajos de una persona), lo ideal es usar el modelo de documento (JSON). Para una relacion uno a muchos, lo ideal es usar el modelo relacional tradicional (por ejemplo para los comentarios en una app)