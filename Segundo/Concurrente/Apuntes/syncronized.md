# Metodos y Bloques Sincronizados

Mecanismos basicos de exclusion mutua entre hilos.

# Estructura de un hilo

Los hilos son clases que tienen un metodo que se ejecuta de forma concurrente.

```java
    import java.util.concurrent.BrokenBarrierException;
    import java.util.concurrent.CyclicBarrier;

    public class Proceso implements Runnable{
        private Object object;
        
        public Proceso(Object o) {
            this.object = 0;
        }
        
        public void run() {
            try {
                this.object.metodo()
            } catch (InterruptedException e) {
                // TODO Auto-generated catch block
                e.printStackTrace();
            } catch (BrokenBarrierException e) {
                // TODO Auto-generated catch block
                e.printStackTrace();
            }	
        }
    }

```

Los hilos son creados en el main de la siguiente forma.

```java
    public static void main(String[] args) throws Exception {
        Object o = new Object();
        ArrayList<Thread> hilos = new ArrayList<Thread>();
        for(int i=0; i < 3; i++) {
            hilos.add(new Thread(new Proceso(o), "proceso #"+i));
        }
        hilos.forEach(e -> e.start());
    }
```

cada objeto thead tiene una instancia de Proceso y un nombre que servira para identificar el hilo.

# Estructura de un recurso copartido

los recursos compartidos son los objetos que los hilos accederan de forma concurrente y que nosotros tenemos que diseñar para evitar comportamientos inesperados y que esto genere inconsistencia en los datos.

# Metodo Sincronizado

para modelar la sincronizacion podemos implementar metodos sinconizados. cuando un hilo obtiene el lock de un metodo sincronizado entonces podra ejecutar el codigo de dicho metodo. luego al finalizar liberara el lock para que otro hilo pueda tomarlo

> es importante modelar las excepciones en este caso para evitar que un hilo que no pueda terminar su ejeccion no libere el lock.

```java
    public class Recurso {
        private int contador
        public Recurso() {
            this.contador = 0;
        }
        
        public synchronized void metodo(){
            try {
                this.contador++;
            }catch(InterruptedException e) {
                System.out.println(e.getMessage());
            }
        } 
    }
```

la palabra `synchronized` hace que el acceso al metodo requira de un lock.

# Bloque Sincronizado

este enfoque se trata de sincronizar una seccion del codigo del metodo 

```java
   public class Recurso {
        private int contador
        public Recurso() {
            this.contador = 0;
        }
        
        public void metodo(){
            synchronized (this) {
                try {
                    this.contador++;
                }catch(InterruptedException e) {
                    System.out.println(e.getMessage());
                }
            }
        } 
    }
```

esto se puede usar cuando se quiere hacer concurrente parte del codigo y no to

ademas los bloques sinconizados controlan el acceso al lock de un obejto por lo que en una calse podemos tener dos objetos con dos lock diferentes, de esta manera en un metodo podemos tener el control de sincronizacion y en otro otro. de manera que los hilos que ingresan a dos metodos con diferentes objetos sincronizadores no tienen que esperar a que se .

```java
    public calss Recurso(){
        private Object objeto1;
        private Object objeto2;

        public Recurso(){
            objeto1 = new Object();
	        objeto2 = new Object();
        }

        public void metodo1(){
            synchronized(objeto1){
                ...
            }
        }

        public void metodo2(){
            synchronized(obejto1){
                ...
            }
        }

        public void metodo3(){
            synchronized(objeto2){
	            ...
	        }
        }

        public void metodo4(){
            synchronized(obejto4){
	            ...
	        }
        }
    }
```

cuando dos hilos ingresa a metodo1, entonces los demas tendran que esperar. si un hilo ingresa a metodo3 y uno a metodo2 entonces no tendran que esperar por que son dos lock diferentes.

# Espera Activa

Cuando un hilo espera a que se libere el lock de un metodo o de un obejeto este esta esperando activamente e que se libere el lock. en caso de que el hilo que tiene el lock no lo libere por diferentes motivos entonces este hilo se bloqueara para siempre.