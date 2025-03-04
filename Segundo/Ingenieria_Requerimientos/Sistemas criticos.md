Son aquellos donde un fallo puede ocasionar perdidas económicas significativas, daño físico, o en el peor de los casos amenazas a la vida.
## Especificación de requerimientos dirigida por riesgos
Toma en cuenta los eventos peligrosos que pudieran ocurrir, la probabilidad de que realmente sucedan, la posibilidad de que el daño derivara de tal evento y el grado del daño causado.
![[Pasted image 20240820205249.png]]
## Identificación del riesgo
se identifican los riesgos potenciales al sistema. Estos dependen del entorno en que se usa el sistema. Pueden surgir riesgos de interacciones entre el sistema y las condiciones de su entorno operacional.
## Análisis y clasificación del riesgo
Cada riesgo se considera por separado. aquellos potencialmente serios y no improbables se seleccionan para un mayor análisis. En esta etapa, los riestos pueden eliminarse por que es improbable que surjan o por que no se pueden detectar con el software.
## Descomposición de riesgo
cada riesgo se analiza para descubrir la causa raiz potenciales de dicho riesgo. Dichas causas son las razones por las que es posible que falle un sistema. puede ser errores de software, hardware o vulnerabilidades inherentes que son consecuencia de decisiones de diseño del sistema.
## Reducción del riesgo
Se hacen proposiciones de forma para reducir o eliminar los riesgos identificados. Ello contribuye con los requerimientos de confiabilidad del sistema que definen las defensas contra el riesgo y como se manejara este.
![[Pasted image 20240820210918.png]]

## Métodos formales
Son aproximaciones con base matemática al desarrollo del software. Es necesario traducir los requerimientos del usuario, que se expresan en lenguaje natural, diagramas y tablas a un lenguaje matemático que tenga semántica definida.
De este manera usando métodos manuales o soportado por herramientas es posible comprobar el comportamiento de un programa es congruente con la especificación.
Son la forma mas resisa de especificar sistemas y por ende de reducir el ámbito para las malas interpretaciones.
Construir una especificación formal fuerza un análisis detallado de los requerimientos y esta es una forma efectiva de descubrir problemas de requerimientos. 
Como es costoso es posible limitar el uso de este enfoque a aquellos componentes que son críticos para la operación del sistema. Estos se identifican en el diseño arquitectónico del sistema.
![[Pasted image 20240820213644.png]]
### Ventajas
Mientras se desarrolla una especificación formal a detalle se obtiene comprensión profunda y pormenorizada de los requerimientos del sistema. Si la especificación se expresa en un lenguaje con semántica definida formalmente puede analizarse de manera automática para descubrir inconsistencias y aquello que no se completo.
Los costos de las pruebas del programa suelen reducirse porque el programa se verifico contra su especificación.
### Desventajas
Es posible que los propietarios y expertos de dominio no entiendan una especificación formal, de modo que no pueden comprobar que representan con precisión sus requerimientos.
Es bastante sencillo cuantificar los costos de crear una especificación formal, pero es mas fácil estimar el posible ahorro en los costos que resultara de su uso.
La mayoría de los ingenieros de software no han sido capacitados para usar lenguajes de especificación formal. por lo tanto están pocos dispuestos a proponer su uso en procesos de desarrollo.
Es difícil escalar los enfoques actuales a la especificación formal para sistemas muy grandes. Cuando se usa especificación formal, es básicamente para especificar software núcleo (kernel), critico en lugar de sistemas complejos.
La especificación formal no es compatible con los métodos de desarrollo ágiles.
