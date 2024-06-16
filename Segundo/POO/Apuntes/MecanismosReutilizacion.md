# Herencia vs Colaborador Interno

[Inicio](../README.md)

## Herencia

La herencia nos permite tener un mecanismo donde metodos y atributos comunes a un grupo de objetos se encuentren en una clase que los empaquete. Pero tiene la dificultad de mantener ¿que pasa si necesito eliminar uno de estos atributos en una de las subclases?. 

La herencia es util para modelar un caso particular de un dominio donde queremos que el comportamiento de un conjunto de clases sea parecido no exactamente igual pero en grandes razgos parecido.

para esto hacemos uso de una clase auxiliar.

## Colaborador Interno (Delegación)

Se utiliza cuando solo se requiere parte de la funcionalidad de una superclase, proporcionando un control más granular sobre qué métodos y datos reutilizar. Una clase utiliza otra clase para implementar algunas de sus funcionalidades, seleccionando qué partes de la interfaz se utilizan y cuáles se ignoran.

De esta manera cuando necesitamos modelar el comportamiento 