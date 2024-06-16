# Tipos de sincronizacion

# Sincronizacion por Competencia

Es cuando los hilos compiten por el acceso a un recurso y tenemos que diseñar mecanismos que permitan la exclusion mutua.

# Sincronizacion por Cooperacion

En algunos casos la ejecucion de un hilo dependen de ciertas condiciones que otros hilos tendran que notificar  cuando se cumplan.
en estos casos podemos diseñar una espera activa y que el hilo se ejcute cuando se cumpla dicha condicion. este es un mal caso para emplear la espera activa ya que estaria despediciando cpu.
