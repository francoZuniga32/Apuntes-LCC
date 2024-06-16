# Semaforo Binario / Semaforo General

Los semaforos son otro mecanismo para la exclucion mutua que permite evitar la espera activa entre hilos. Normalmente los semaforos tienen n permisos los cuales son tomados por los hilos.

```java
public class Recurso{
	private Semaphore libre;

    public Recurso() {
        //un semaforo de un permiso
		this.libre = new Semaphore(1);
	}

    public boolean metodo() {
		if(this.semaforo.tryAcquire()) {
			System.out.println("Imprimiendo el trabajo "+trabajo);
			this.libre.release();
			return true;
		}else {
			return false;
		}
	}
}

public class Proceso() implements Runnable{
    ...
    public void run(){
        while(!recurso.metodo()){
            System.out.println("Esperando al recurso compartido");
        }
    }
}

```

cuando un hilo trata de hacer tryAcquiere() en caso de no poder obtener el permiso, no se bloquara (podemos hacer que se bloque haciendo acquiere()) ademas en los semaforos de n permisos podemos indicar la cantidad de permisos a tomar o la cantidad de permisos a liberar.

- con `acquiere()` se toma un permiso con `acquiere(n)` se toman n permisos
- con `tryAcquiere()` se trata de tomar un permiso, con `tryAcquiere(n)` se trata de tomar n permisos.
- con `releace()` se libera un permiso con `releace(n)` se liberan n permisos.

## Rendezvous

cuando un hilo depende de que otro hilo libere un permiso para que este pueda continuar con su ejecucion.