# Apuntes para final de Teoria catedra

## Introduccion

- **POO:** La programación orientada a objetos (POO) es un paradigma de programación que se basa en el concepto de "objetos". Cada objeto representa un elemento del "mundo" con sus relaciones y sus atributos.

- **Clase:** Es la plantilla con la que se crean objetos, definiendo métodos y atributos.
    - Es responsable de la creación de objetos que la instancien.
    - Para crear un objeto, necesitamos enviar un mensaje a la clase (`new`).
    - Podemos usar `new` (deja las variables de instancia con valores nulos), o implementar un mensaje en la clase que inicialice los datos (`inicializar`) para luego pedir algunos datos iniciales (`inicializar(...)`), luego usamos `new inicializar(...)`.
    - También podemos tener un mensaje en la clase personalizado que oculte el inicializar (`crear(...)`) donde le paso los datos iniciales.
    - Se organizan en una jerarquía de clases.
        - Ocultan la estructura y las operaciones propias al resto del programa.
        - Encapsulan todas las operaciones del mismo tipo.
        - Describen la interfaz de los objetos (qué mensajes pueden responder).

- **Objeto:** Es una instancia de una clase.
    - Una vez que es instanciado comienza su tiempo de vida.
    - Identidad: Cada objeto puede ser identificado como una entidad única.
    - Estado: Comprende todas las variables de instancia del objeto y sus valores en un momento determinado del tiempo.
    - Comportamiento: Cómo actúa y reacciona en términos de sus cambios de estado y pasaje de mensajes.
    - Relaciones: Se relacionan con otros objetos mediante el envío de mensajes.

- **Mensaje:** Los objetos interactúan entre sí mediante mensajes. Tienen que llevar la información necesaria para resolverlo. Puede ayudarse de otros objetos para resolver lo que se le pide. Proceso dinámico de pedir a un objeto que lleve a cabo una acción específica. Un mensaje siempre se envía de un objeto a otro. La acción realizada en respuesta al mensaje no es fija, puede variar dependiendo de la clase del objeto receptor.
    - Un único método contiene el código que implementa el mensaje. El mismo código se aplica a todas las instancias de la clase. Es posible acceder y actualizar atributos.
    - `self` y `this` permiten hacer referencia a la instancia actual de la clase.
    - Un objeto que no existe no puede recibir mensajes.
    - Con parte de la interfaz de un objeto.

- **Responsabilidad:** Las responsabilidades estan realcionadas con las obligaciones de un objeto en terminos de su comportamiento.
    - conocimiento: sobre sus atributos y asociaciones.
    - accion: hacer algo por si mismo, iniciar accino en otros objetos, controlar y codignar actividades en otros objetos.
    - la responsabilidad no es un metodo, pero son implementadas utilizando metodos, que actuen solos o con otros metodos y sobre otros objetos.

- **Encapsulamiento:** Sabemos que un objeto tiene que realizar una acción pero no nos importa cómo.

- **Identidad:** Cada objeto tiene su identidad y es tratado de forma individual.

- **Estado:** Abarca a todos los atributos y sus valores actuales.

- **Comportamiento:** De un objeto es cómo actúa y reacciona en términos de estado y mensajes.

- **Abstracción:** Considerar la resolución de un problema sin tener en cuenta los detalles por debajo de un cierto nivel, filtramos los aspectos relevantes obteniendo soluciones más generales.

- **MDO:** Es la forma que tenemos de modelar las relaciones entre objetos.
    - UML para describir las clases y sus relaciones (las que tendrán que respetar los objetos).
    - Un sistema de software es usualmente complejo.
    - Es necesario descomponerlo en partes manejables y de complejidad comprensible.
    - Cada parte puede ser representada como un modelo que describe y abstrae los aspectos esenciales del sistema.
    - Los modelos están compuestos por diagramas y documentos que describen cosas.
    - Los modelos enfatizan información estática o dinámica del sistema.
    - Cada relacion entre clases puede tener: nombre, multiplicidad (cuantas instancias de una clase se puede relacionar), y navegavilidad (direccion de recorrido).
    - una clase se puede relacionar a si misma.
    - en la navegavilidad determina quien puede enviar mensajes a la otra clase y a que clases se lo puede enviar.
    - para modelar la loguica de los mensajes es mediante di diagrama de secuencias.
    - donde marcamos que pasa cuando a una instancia se le solicita una accino por medio.
    - tambian se detallan los mensajes en nivel de logico.

- **Arquitectura en tres capas:** es una forma de separar una solucion en tres capas: interfaz de usuario, la logica de aplicacion, y el acceso a los datos
    - interfaz de usuario: es lo que el usuario vera del sistema y con el que interactura.
    - logica de aplicacion: objetos del dominio, que cumplen con los requerimientos de la aplicacion.
    - acceso a datos: mecanismos de almacenamiento persistente. 
    
- **Herencia:** es un mecanismo para poder repetir atributos y metodos en otras clases sin tener que repetir codigo.
    - una clase toma el comportamiento y la estructura interna de otro y agrega su propia conducta.
    - el comportamiento y datos asociados con la clase hijo (subclase) son siempre una extencion de las propiedades asociadas con la calse padre (superclase).
    - cuando recibe un mensaje lo busca en la clase que lo recibe, en caso de no encontrarlo lo buscara en la superclase. 
    - todos los objetos en la mayoria de los lenguajes son subclase de la clase object.
    - una clase abstracta es aquella que no puede tener instancias, describen atributos y comportamientos de subclases, tiene operaciones abstractas.

- **Polimorfismo:** los objetos de distintas clases y de la mima familia entienden los mismos mensajes.
    - igual semantica, diferentes implementaciones, un mismo mensaje puede provocar la invocaciones de metodos diferentes.
    - **Sobrecarga:** cambian la cantidad de parametros en un mismo mensaje.
    - **Refinamiento:** hace uso del metodo heredado pero cambia luego el resultado.
    - **Remplazo:**: remplaza el metodo heredado. Suele ser usado cuando una clase hereda de una clase abstracta.
    - **Puro:** no se implementa en las subclases se usa directamente el metodo del la clase padre.
    - visiblidad: publica, privada y protected (solo accesible desde subclases).

- **Ligamento:** Algunos lengaues de tipado estatico permiten que asignemos variables de una subclase a un tipo de la clase padre.
    - a la hora de ejecutar un metodo comprobada que existe en la superclase, antes de ejecutar la de la subclase.
    - en el caso de declarar una variables con el valor de una super clase sera el tipo estatico.
    - la subclase que es relacionada como valor sera el tipo dinamico.




