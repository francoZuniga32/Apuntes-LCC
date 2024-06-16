# Apunte 1

## Seguridad 

Se agrega la dimencion temporal a las tecnicas de diseño y programacion. El control de concurrencia introduce la deabilitacion del acceso de forma pasajera/temporal basandose en condiciones de las acciones que estan siendo ejecutadas por otros hilos. Se controla que las variables prpias y la de los objetos en el sistema se mantengan en un estado consistente. Para asegurarse de esto se utilizan mecanismos de exclusion mutua.

## Viveza

Eventualmente algo ocurrira el sistema "vivo" eventualmente progresara hasta completarse, cada metodo invocado se invocara. Pero puede fallar por diversas razones:

- bloque : un metodo sincronizado bloquea un hilo mientras otro hilo mantiene el lock.
- espera: un metodo se bloquea esperando un evento, mensaje, o condicion por todavia tiene que producise
- entrada : un metodo basado en entrada/salida se bloqueara esperando una entrada que todavia no ha llegado de otro proceso o dispositivo
- contencion de CPU: un hilo no logra tener tiempo de CPU aunque pueda ejecutarse.
- falla : se produce una excepcion o falla. 

### Fallas

1. deadlock, dependencias ciruclares entre locks
2. deñales perdidas, un hilo permance dormido por que empezo a esperar despues de que una notificacion se produjo.
3. cierre de monitores anidados, un hilo mantiene el lock que otro hilo que tiene que desbloquearlo.
4. liverlock. una accion que se intenta continuamente, falla.
5. stavation, la maquina virtual falla siempre en asignar tiempo de cpu a un hilo.
6. agotamiento de recursos, un grupo de hilos mantiene todos los recursos.
7. falla distribuida una maquina remota conectada por un socket se hace inacceisble o se rompe.

## Exclusion mutua

Cuando varios hilos trabajan sobre los mismos recursos, pueden genearar inconsistencias en la informacion.  Los recursos que quieren ser accedidos por varios hilos o procesos son recursos critivos, y el sector de programa que desea usarlos es la seccion critica.

para asegurar la exclusion mutua:

- solo un proceso debe acceder a la seccion critica.
- un proceso detenido fuera de su seccion critica no debe afectar a los demas procesos.
- un proceso no puede ser retrasado en acceder a una seccion critica .
- si un proceso esta en su seccion critica, el que quiere entrar debe poder hacerlo sin demoras.
- un proceso no puede permanecer indefinidamente en una seccion critica.
- no se debe asumir nada respecto a la cantidad de procesos ni a la velocidad relativa de los mismos.

si un hilo esta intantando acceder a los atributos de un objeto se debe lograr que no haya mas de un hilo accediendo 