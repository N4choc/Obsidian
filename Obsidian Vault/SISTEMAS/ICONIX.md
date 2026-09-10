
A nivel de proceso, se distinguen dos tipos de requerimientos: los requerimientos funcionales y los requerimientos de comportamiento. (tambien los hay no funcionales pero no estan involucrados en la etapa de modelado). 

-Requisitos funcionales: definen el QUE debe ser capaz de hacer el sistema. 
-Requisitos de comportamiento: definen el COMO el usuario y el sistema van a interactuar. Segun el libro se recomienda hacer un prototipo de GUI para asi poder ir identificando casos de uso. 

Nota: obviamente se debe asegurar que los casos de uso coincidan con las expectaciones del cliente. 


## MODELO DE DOMINIO
Forma parte de la fundacion de la parte estatica del proyecto. Es decir, la parte que describe la estructura del mismo. 

### DIAGRAMA DE SECUENCIA

La idea principal es poder darle *personalidad* a las clases. Esto quiere decir, que luego de identificar a las controladoras en el diagrama de robustez, se pueda transformar a estas controladoras como métodos o mensajes entre las distintas instancias de objetos. (Recordar no darle demasiada responsabilidad a una sola clase, si no también delegar para obtener un poco menos de dependencia)

