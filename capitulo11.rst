Sincronización de Procesos
==========================

Se denomina **procesos cooperantes** a aquelos procesos que pueden afectar
o verse afectado por otros procesos que se están ejecutando en el sistema.

Los procesos cooperantes puede compartir, ya sea directamente o a través
de archivos, todo el código y los datos de los programas. Para los hilos,
compartir un datos y variables, es algo normal. Pero cuando varios hilos
tienen acceso concurrente a estos datos puede resultar en inconsistencia
de datos.

Hablamos entonces de **sincronización de procesos**, que trata del mecanismo
que permite asegurar la ejecución ordenada de procesos cooperantes que
comparten los mismos datos, de forma tal que la consistencia de estos datos
se mantiene.

¿Cómo se lleva a cabo la sincronización de procesos?
----------------------------------------------------

Cuando tenemos un conjunto de procesos cooperantes que tienen acceso a datos
compartidos, el sistema operativo tiene que proporcionar mecanismos de
exclusión mutua a esos datos.

Una solución es através del concepto de **sección crítica** de código. Esto es,
la porción de código de un programa de computador en la que se accede a un recurso 
compartido (estructura de datos o dispositivo) que no debe ser accedido por más de un
proceso o hilo en ejecución. La sección crítica por lo general termina en un tiempo
determinado y el hilo, proceso o tarea sólo tendrá que esperar un período determinado 
de tiempo para entrar.

Problema de la sección crítica
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Supongamos que tenemos :math:`n` procesos ejecutándose al mismo tiempo en el mismo
procesador :math:`[P_1, P_2, \cdots, P_n]`. Cada procesos tiene un segmento de código,
que llamaremos **sección crítica**, en la cual los procesos cambian variables
comunes, actualizan una base de datos, imprimen en la pantalla, y así sucesivamente.

Hay que tener en cuenta que una de las característica más importantes del sistema es
que, cuando un proceso está ejecutando en su sección crítica, ningún otro procesos
tiene el permiso de ejecutar código en su sección crítica.

Es por eso que la ejecución de las secciones críticas por los procesos es
**mutuamente exclusiva** en el tiempo. Entonces, el problema de la sección
crítica consiste en diseñar un protocolo que los procesos puedan usar para
cooperar en el uso de datos compartidos.

En estos protocolos, cada proceso debe solicitarle permiso al sistema operativo
para entrar a su sección crítica. Y una vez finalice la ejecución de la sección
crítica, el proceso debe avisarle al sistema operativo que va a salir de la
sección crítica. En forma general, la estrucutra del código de estos procesos
cooperantes :math:`P_i` sería la siguiente:

.. code-block:: python
   :emphasize-lines: 2, 4
   
   while True:
       entrar_seccion_critica()
       seccion_critica()
       salir_seccion_critica()

       resto_del_proceso()

Soluciones al problema de la sección crítica
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Una solución al problema de la sección crítica debe satisfacer los siguientes
tres requerimientos

Exclusión Mutua:
    Si un proceso :math:`P_i` está ejecutando su sección crítica, entonces ninguno
    de los otros procesos puede estar ejecutando sus secciones críticas.

Progreso:
    Si ningún proceso está ejecutando su sección crítica, y algún proceso desea 
    entrar a la sección crítica, entonces solo estos procesos que no están ejecutando
    las secciones críticas pueden participar en la decisión de quien entrará a
    continuación a su sección crítica, y la selección no puede ser pospuesta 
    indefinidamente.

Espera limitada:
    Existe un límite en el número de veces que otros procesos tienen permiso de
    entrar a sus secciones críticas después que un proceso ha hecho un requerimiento
    de entrar a la sección crítica y antes que el permiso sea otorgado por el
    sistema operativo.

Solución con dos procesos
^^^^^^^^^^^^^^^^^^^^^^^^^

Supongamos que tenemos dos procesos :math:`P_0` y  :math:`P_1`, de la siguiente
manera podemos lograr que ambos procesos trabajen cooperativamente usando exclusión
mutua:

**Algoritmo 1**

Supongamos que los procesos comparten una variable entera en común llamada ``turno``
, que puede ser inicializada en 0 o en 1. Entonces se da que si ``turno == i``,
entonces el proceso :math:`P_i` tiene permiso de entrar y ejecutar su **sección
crítica**.

La estructura del proceso se muestra a continuación:

.. code-block:: python

   while True:
       while turno == i:
           pass
       
       seccion_critica()

       turno = j
       resto_del_proceso()

Esta solución asegura que únicamente un proceso a la vez puede estar en su
sección crítica. Sin embargo, esta solución no satisface el requerimiento de
progreso, ya que requiere la ejecución alternativa de los procesos en la
sección crítica. Por ejemplo, si ``turno == 0`` y :math:`P_1` está listo
para entrar a su sección crítica, no puede hacerlo hasta que :math:`P_0`
use la sección crítica, aunque esté lejos de entrar en ella.

**Algoritmo 2**

El problema con el algoritmo 1 es que no retiene suficiente información acerca
del estado de cada proceso; el algoritmo solo recuerda el proceso que va a entrar
a la sección crítica. Para remediar este problema, podemos reemplazar la variable
``turno`` por un vector de variables booleanas que denominaremos ``banderas``. Todas
las banderas se inicializan en ``False``. Si ocurre que ``banderas[i]`` es
verdadera o ``True``, indica que :math:`P_i` está listo para entrar a la 
sección crítica.

.. code-block:: python

   while True:
       banderas[i] = True
       while banderas[j]:
           pass
        seccion_critica()
        baderas[i] = False
        resto_del_proceso()

En este algorimo, lo primero que hace el proceso :math:`P_i` es colocar el valor
de la variable ``banderas[i]`` en True, para indicar que está listo para entrar
en su sección crítica. Luego, proceso verifica que otro proceso :math:`P_j`
no se encuentra ya en su sección crítica. Si el proceso encontró que ya alguien
está en su sección crítica, espera a que finalice antes de solicitar el acceso 
a la misma.

Cuando ya termina la ejecución de la sección crítica, el proceso coloca un false
en las ``banderas[i]``, de forma tal que si había otro proceso esperando entrar
a su sección crítica, pueda hacerlo ahora.

En esta solución, el requerimiento de la exclusión muta se satisface sin problema.
Infortunadamente, el requerimiento de **progreso** no se tiene.

Semáforos
^^^^^^^^^

Un semáforo es una herramienta de sincronización. Es una de las primitivas de
sincronización más antiguas de la historia de la computación. Fue inventada por
el científico de la computación holandés Edsger W. Dijkstra. 

Los semáforos mantienen dentro de si un contador entero que indica el número de
procesos o hilos que pueden hacer uso concurrente a un recurso compartido. Además
del contador, los semáforos poseen dos operaciones estándar atómicas: ``acquire()``
y ``release()`` (En la versión original de Dijkstra se llamaba **P** y **V**).

Las operaciones funcionan de la siguiente manera: el contador interno del semáforo
se decrementa cada vez que se ejecuta ``acquire()`` y es incrementado cada vez
que se ejecuta ``release()``. Pero la regla general de los semáforos impide que
el contador caiga por debajo de cero. De esta forma, cuando ``acquire()``
encuentra que el contador es cero, se bloquea, esperando que un hilo utilice
la operación ``release()``.

Por ejemplo, el siguiente código en Python muestra dos hilos que comparten una
variable en común, ``num``, y usamos un semáforo para proteger el acceso a esta
variable.

.. code-block:: python

   num = 0
   sem = Semaphore(1)

   def sumar_uno():
        global num
        sem.acquire()
        num += 1
        sem.release()

    def sumar_dos():
        global num
        sem.acquire()
        num += 2
        sem.relase()

    # Creamos los hilos
    thread1 = Thread(target=sumar_uno)
    thread2 = Thread(target=sumar_dos)
    thread1.start()
    thread2.start()

    # Esperamos que finalicen los hilos
    thread1.join()
    thread2.join()

    print(g)