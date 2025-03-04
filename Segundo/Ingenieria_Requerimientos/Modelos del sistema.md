Es el proceso para desarrollar modelos abstractos de un sistema. cada modelo presenta una visión o perspectiva diferente de dicho sistema.
El modelado de sistemas se ha convertido en un medio para representar el sistema usando algún tipo de notación gráfica.
Casi siempre se basa en notaciones en el lenguaje de modelado unificado (UML).
## Modelado de casos Usos
El modelado de casos de uso para apoyar la adquisición de requerimientos. Un caso de uso puede tomarse como un simple escenario que describa lo que espera el usuario de un sistema.
Cada caso de uso representa una tarea discreta que implica intereaccion externa con el sistema.
En su forma mas simple un caso de uso se muestra como una elipse, con actores que intervienen en el caso de uso representado como figuras humanas.
![[Pasted image 20240817002907.png]]
![[Pasted image 20240817002921.png]]
## Diagramas de clase
una clase se considera como una definición general de un tipo de objeto del sistema. una asociación es un vinculo que indica que hay una relación entre dichas clases.
Cuando se desarrollan modelos durante las primeras etapas del proceso de ingenieria de software los objetos representan algo en el mundo real.
Conforme se desarrolla una implementan por lo general se necesita definir los objetos de implementacion adicionales que se usan para dar la funcionalidad requerida del sistema.
La primera etapa identificamos los objetos esenciales y representarlos en clases. luego identificamos las relaciones entre clases y se definen las asociaciones entre las mismas.

![[Pasted image 20240817155108.png]]
Para definir las clases con mas detalles, agregamos información sobre sus atributos
![[Pasted image 20240817155139.png]]
### Generalizacion
es una relacion "es-un" entre dos clases donde la subclase o clase hija es una forma especializada de la clase padre o superclase. la superclase se considera como generalizacion de la subclase y la subclase se considera una especializacion de la superclase.
También se suele denominar relación de herencia ya que representa el mismo concepto del paradigma de orientación a objetos.
![[Pasted image 20240817155424.png]]
## Diagramas de actividad
Son diagramas dinámicos centrado en operaciones. Estan organizados respecto a las acciones y usado para especificar:
- un metodo 
- un caso de uso 
- un proceso de negocio (workflow).
Cuando una actividad termina se desencadena el paso a la siguiente actividad. estan asosicado a la implementacion de un caso de uso o a muchos. Un caso de uso puede estar acompañado por cero, uno o mas diagramas de actividad.
Varios casos de uso pueden formar parte de un o varios diagramas. se debe usar diagrama de actividad en situaciones donde todos o la mayoria de los eventos representan la finalizacion de acciones generadas internamente.
Este tipo de diagramas es adecuado en situaciones donde ocurren eventos concurrentes. El objetivo de estos diagramas es el de modelar un proceso de flujo de trabajo, es decir modelar operaciones.
![[Pasted image 20240817160605.png]]
![[Pasted image 20240817160753.png]]
![[Pasted image 20240817160809.png]]
![[Pasted image 20240817160822.png]]
