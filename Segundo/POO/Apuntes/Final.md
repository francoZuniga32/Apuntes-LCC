# Apunte Final Teoria

## ¿Que es POO?
La programación orientada a objetos (POO) es un paradigma de programación que se basa en el concepto de "objetos". Cada objeto es una instancia de una clase, y las clases son plantillas para crear objetos.

En la POO, los objetos tienen propiedades (llamadas atributos o variables de instancia) y comportamientos (llamados métodos). Por ejemplo, considera un objeto "Coche". Podría tener propiedades como "marca", "modelo", "color", etc., y comportamientos como "arrancar", "detenerse", "acelerar", etc.

## ¿Que es una instancia, una clase?
Una clase es una plantilla o molde que sirve para construir instancias. Estos moldes definen que datos tienen los las instancias de ese modelo (atributos) y como se comportan (metodos).
Las instancias son objetos creados de un modelo que tienen una serie de atributos y un comportamiento dado.

## ¿Que son los atriburos y metodos?
Los atributos es informacino que posee cada objeto y estan definidos por la clase que los crea.

```java
public class Auto{
    private String patente;
    private String modelo;
    private Date fechaCreacion;
}
```
luego cada instancia de Auto tendra informacion diferente:
```js
Auto auto1 = {
    patente: "AR-2020",
    modelo: "2008",
    fechaCreacion: "20/04/2008"
}

Auto auto2 = {
    patente: "AR-2021",
    modelo: "2009",
    fechaCreacion: "02/11/2009"
}
```
* (la sintaxis no es del todo correcta en estos dos ejemplos, es meramente representativo).
Vease que cada auto tiene su informacion en particular, pero se mantienen dentro del mimo **Dominio**.

Los metodos con como actua al auto:
```java
public class Auto{
    private String patente;
    private String modelo;
    private Date fechaCreacion;

    public bool Arrancar(){
        ...
    }
}
```

Entonces cada instancia de Auto podra realizar la accion `Arrancar()` y el funcionamiento estara definido por la clase Auto.
```js
"arrancar el auto1" 
auto1.Arrancar();
"arancar el auto2"
auto2.Arrancar();
```

De esta manera la clase dererminara como es que se comporte cada Auto, pero cada auto tendra autonomia de accion.

## ¿Que es la resposabilidad?
Es normal que los objetos interactuen entre si ante un mensaje, un objeto no siempre es responsable de resolver todo lo que se les solicita, este delegara a otros parte de la solucion.
Ej: Juan le solicita a las inmobiliarias la busqueda de una casa. La inmobiliaria buscara en su registro de propietarios y les consultara si tienen diponibles alquileres. 

Vemos que la inmobiliaria delega la parte de saber si tienen diponibles alquileres a los propietarios. No realiza una investigacion a ver si tienen o no alquieres diponibles.

De esto se trata la responsabilidad de que cada clase sea responsable de:
1. sabes su estado actual
2. poder resolver parte del problema que le solicitan
3. poder delegar parte de la solucion a otras clases y que estan sepan resolver esa parte del problema.

## ¿Como modelamos clases?
Los objetos interactuaran entre si, su forma de interactuar vendra definida en las clases, pero sera importante definir como se comportaran previo a su construccion (implementacion en un lenguaje de programacion).

Las calses se modelan mediente UML (Unified Modeling Language) es un lenguaje estándar de modelado visual utilizado en ingeniería de software para representar sistemas complejos. 

Una clase en UML cuenta con:
|Nombre|
|---|
|Atributos|
|Metodos|

Los atributos y metodos pueden ser publicos (visibles por las demas clases) o privados (solo accesibles desde dentro de la clase / algun metodo). Se denotan privados con `-` y publicos con `+`.

## ¿Como modelamos las interacciones entre objetos?
Para diagramar la forma que tienen los objetos de comunicarse, y resolver lo que se les solicita usaremos los diagramas de secuencia. que son una forma de modelar las interacciones entre objetos

Un diagrama de secuencia se ve como lo siguiente:

//imagen de diagrama.

## ¿Cuales son las bases de la POO?
- principios de la poo.

## ¿Que es la herencia?

## ¿Cuales son los diferentes tipo de polimorfismo?



## ¿Que son los principios SOLID?