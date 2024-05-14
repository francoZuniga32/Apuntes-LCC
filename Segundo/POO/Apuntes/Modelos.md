# Modelos
[Inicio](../README.md)

Necesitamos una forma de modelar las interacciones entre objetos que no sea con dibujitos, para esto usaremos UML.

UML (Unified Modeling Language) es un lenguaje estándar de modelado visual utilizado en ingeniería de software para representar sistemas complejos. Proporciona una forma de visualizar la estructura y el comportamiento de un sistema a través de diferentes tipos de diagramas, como diagramas de clases, diagramas de secuencia, diagramas de actividades, entre otros. UML es ampliamente utilizado en el desarrollo de software para comunicar ideas, diseñar sistemas y documentar el proceso de desarrollo.
# Modelo Estatico 
Este modelo indica los objetos, sus atributos, sus mensajes, el nivel de acceso a los metodos y atributos (publicos, privados), ademas de sus relaciones, y la cardinalidad.

1. **Atributos:** son las características o propiedades que describen el estado de un objeto. Por ejemplo, si consideramos un objeto "Coche", los atributos podrían ser "marca", "modelo", "color", etc. Estos atributos representan datos asociados con el objeto y pueden tener diferentes tipos, como números, cadenas de texto, booleanos, entre otros.
2. **Metodos:** por otro lado, son las acciones o comportamientos que un objeto puede realizar. Estos métodos definen qué puede hacer el objeto y cómo interactúa con otros objetos. Siguiendo el ejemplo del coche, podríamos tener métodos como "arrancar", "detenerse", "acelerar", etc. Los métodos pueden acceder y modificar los atributos del objeto, así como realizar cualquier otra operación necesaria para cumplir su función.
3. **Relaciones:** los objetos se realacionan entre si y de esta manera se comunican. Existen diferentes tipos de relaciones entre objetos:
   1. **Dependencia**: La clase A puede verse afectada por cambios en la clase B. Ej: Dependencia en UML. El profesor depende de los materiales del curso
   2. **Asociacion**: El objeto A conoce el objeto B. La clase A depende de B. Ej: Asociación en UML. El profesor se comunica con los estudiantes.
   3. **Composición:** El objeto A conoce el objeto B, consiste (se construye con B) en B y gestiona el ciclo vital de B. La clase A depende de B. Ej: Composición en UML. La universidad consta de departamentos.
   4. **Agregación:** La clase A define métodos declarados en la interfaz B. Los objetos A pueden tratarse como B. La clase A depende de B
4. **Cardinalidad:** Define con cuantos objetos del otro grupo se pueden relacionar. tenemos uno-uno, uno-muchos, muchos-muchos.
