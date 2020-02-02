Características de los SO moderno
=================================

A través de los años ha habido una evolución gradual de la estructura 
y capacidades de los SO. La mayoría de los avances entran en las 
siguientes categorías:

* Arquitectura del microkernel: se asignan únicamente unas pocas funciones
  esenciales al kernel, incluyendo espacio de direcciones, comunicación entre
  procesos (IPC) y planificación básica. Los otros servicios del SO son
  provistos por procesos que corren en modo usuario y son tratados como
  cualquier otra aplicación por el microkernel. Este enfoque simplifica la
  implementación, provee flexibilidad y es muy útil para los ambientes
  distribuídos.

* Hilos múltiples: es una técnica en la que un proceso, ejecutando una
  aplicación, se divide en hilos (*threads*) que pueden ejecutarse
  simultáneamente. Un hilo es una unidad despachable de trabajo, se ejecuta
  secuencialmente y es interrumpible para que el procesador pueda cambiar a otro
  hilo. Esta técnica es útil para aplicaciones que realizan un número de tareas
  esencialmente independientes que no requieren ser serializadas.

* Multiproceso simétrico (SMP): se refiere a una arquitectura de hardware que
  incluye múltiples procesadores, tanto como a los SO que reflejan esta
  arquitectura. Un multiprocesador simétrico contiene múltiples procesadores
  que comparten la misma memoria y las facilidades de E/S, y que pueden
  realizar las mismas funciones. El SO de un SMP planifica procesos e hilos a
  través de todos los procesadores. Las ventajas potenciales son la mejora en
  la *performance* por el procesamiento en paralelo, la posibilidad del
  crecimiento incremental del sistema, y la posibilidad de que el sistema
  continúe funcionando aunque uno de los procesadores falle.

* SO distribuídos: proveen la ilusión de un espacio único de memoria principal
  y secundaria más otras facilidades unificadas de acceso para un conjunto de
  computadoras separadas.  

* Diseño orientado a objetos: otorga disciplina al 
  proceso de adicionar extensiones modulares a un kernel chico. Permite al
  programador personalizar el SO sin destruir su integridad.
