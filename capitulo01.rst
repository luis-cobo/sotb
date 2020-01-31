Conceptos Básicos de Sistemas Operativos
========================================

Encontrar una definición concreta de un sistema operativo no es cosa sencilla. Muchos
autores lo definen de manera diferente. Para unos autores, se trata de un conjunto de 
programas o software destinado a permitir la comunicación del usuario con un computador
y gestionar los recursos del mismo de manera cómoda y eficiente. 

Otros autores lo definen como *una colección organizada de programas que extienden el 
hardware del computador, y que consisten de rutinas de control para la operación de un
computador y que proporciona un ambiente para la ejecución de los programas*. Sea cual
sea la definición, debemos tener en cuenta que un sistema operativo es una parte muy 
importante en casi cada sistema de cómputo.

Eso si, hay que tener en cuenta que el sistema operativo es el programa más
importante del computador. Sin él, no es posible que funcionen los otros
programas que tenemos instalados en nuestro equipo. Los sistemas operativos
realizan tareas básicas para el usuario, tales como permitir acceso al
teclado, enviar información a la pantalla, llevar registro de los archivos y
directorios de la carpeta, controlar los dispositivos periféricos tales como
impresora, mouse, etc.

En sistemas grandes, el sistema operativo tiene incluso mayor responsabilidad
y poder, es como un policía de tránsito, ya que se asegura de que los
programas y los usuarios que están trabajando en el computador al mismo tiempo
no interfieran entre ellos. El sistema operativo también es responsable de la
seguridad, verificando que los usuarios no autorizados no tengan acceso al
sistema.

A partir de todo la anterior, es que podemos indicar que un sistema de cómputo
puede dividirse principalmente en cuatro componentes:

* El hardware de la máquina
* El sistema operativo
* Los programas de aplicación, y
* Los usuarios

.. figure:: fig01.png
   :alt: Visión abstracta de un sistema de cómputo

   Figura 1 Visión abstracta de un sistema de cómputo [Tomado de (Tomsho, 2017)] 

Niveles de los Sistemas Operativos
----------------------------------

La mayoría de los diseños de sistemas operativos dividen internamente la construcción
del mismo en tres niveles:

* El Shell
* Los Servicios o API de llamado al Sistema y
* El núcleo o *kernel* 

.. figure:: fig02.gif
   :alt: Arquitectura del sistema operativo UNIX

   Figura 2 Niveles del Sistema Operativo [Tomado de (Stevens, 2005)] 

Shell 
    El **shell** es un programa que comunica el núcleo con los usuarios, ya sean
    aplicaciones o personas. El shell cuenta con un extenso grupo de comandos que los
    usuarios pueden utilizar para solicitar acciones. El shell interpreta esos
    comandos y realiza las llamadas al sistema.

Servicios o Llamadas al sistema
    Ofrece a los programas un conjunto de servicios en forma de interfaz de programación o 
    *API*. Cualquier servicio que un programa necesite del sistema operativo se puede obtener
    a través de estos *llamados al sistema*. Cada sistema operativo ofrece a los desarrolladores
    un API con el cual se pueden construir programas en ese sistema operativo. Por ejemplo,
    el sistema operativo Android permite que los programas puedan conocer la ubicación
    geográfica del usuario o el sistema operativo Windows, permite que los programas
    dibujen figuras o imágenes sobre la pantalla. Esos son servicios que se ofrecen a través
    de los APIs.

Núcleo o *Kernel*
    El núcleo es un programa con la capacidad y autoridad de asignar y restringir el uso de todos los recursos. Es el elemento administrador. Sin embargo, los usuarios no pueden interactuar directamente con el núcleo, porque el núcleo sólo atiende llamadas de sistema, que son accedidas desde los programas desarrollados por los programadores.

Funciones de un Sistema Operativo
---------------------------------

Ya que el sistema operativo es el único programa que interactúa directamente con el hardware
del computador, entre sus funciones principales tenemos las siguientes:

* Hacer de interface con el usuario.
* Facilitar la entrada y salida del computador y la comunicación con los periféricos.
* Permitir compartir los diversos dispositivos del computador así como los datos que se generan
  y manejan en él.
* Protección (por ejemplo, que un usuario no borre los datos de otro).

* Planificar la distribución de recursos, es decir, debe distribuir el procesador para que
  varios usuarios puedan trabajar en él simultáneamente. La planificación busca repartir los
  recursos de forma equitativa entre los programas.
* Recuperarse de los errores.
* Organizar de datos (en el sentido de localizar rápidamente la información)
* Manejar las comunicaciones por la red.

Según las funciones del Sistema Operativo, podemos clasificarlos en uno de los siguientes 
esquemas:

* Como una *máquina virtual* que ofrece una interface, y
* Como un administrador de recursos

Los Sistemas Operativos como una Máquina Virtual
    Bajo este esquema, la función del sistema operativo es que el usuario vea al sistema
    operativo como el equivalente a una máquina extendida o *máquina virtual*, de tal forma
    que los programas sean más fáciles de desarrollar que lidiando directamente con el
    hardware subyacente en cada computador.

Los Sistemas Operativos como Gestores de Recursos 
    Internamente, un sistema operativo actúa como un administrador de recursos del 
    computador. ¿Cuáles son esos recursos que el sistema operativo debe administrar? Pues
    entre estos recursos encontramos el procesador, la memoria, los dispositivos de entrada
    y salida.

    Bajo este esquema, el sistema operativo lleva registro del estado de cada recurso, y
    es él quien decida quien puede tener acceso a un recurso, por cuánto tiempo puede
    usarlo y en qué momento tiene uso del mismo.

    Cuando tenemos sistemas que soporten *concurrencia* (ejecución simultánea de varios 
    programas en el mismo procesador), es tarea del sistema operativo resolver los diversos
    conflictos que pueden ocurrir cuando varios procesos quieren tener acceso al mismo
    tiempo al mismo recurso. Esta resolución de conflictos se debe hacer preservando la
    integridad del sistem y buscando optimizar el desempeño resultante del equipo.


Servicios del Sistema Operativo
-------------------------------     

Un sistema operativo proporciona un ambiente para la ejecución de los programas. Esto
lo hace a través de un conjunto de servicios que son utilizados por los programas y a
los usuarios de estos programas.

Estos servicios del sistema operativo se brindan para la comodidad del programador, con
el fin de facilitar las tareas de programación.

Ejecución de programas
    El sistema tiene ser capaz de cargar un programa en la memoria del computador y ejecutarlo.
    De igual manera, el programa debe ser capaz de terminar su ejecución, ya sea normal o
    anormalmente (indicándole al sistema operativo el error que ocurrió).

Operaciones de Entrada/Salida
    Un programa en ejecución puede requerir entrada o salida de información. Esta entrada/
    salida puede incluir un archivo en el disco duro del computador o cualquier otro 
    dispositivo unido al computador. 

    Por motivos de eficiencia y protección, los usarios no deberían controlar estos
    dispositivos de entrada/salida directamente. Por lo tanto, el sistema operativo
    debe proporcionar medios para realizar operaciones de entrada/salida sobre estos
    dispositivos de manera controlada.

Manipulación del sistema de archivos
    Los programas necesitan leer y modificar los archivos que están siendo almacenados
    en los discos del computador. De la misma manera, los programas y usuario necesitan
    crear y borrar archivos, dados el nombre del mismo.

Comunicaciones
    En muchas circunstancias, un proceso necesitará intercambiar información con otro proceso.
    La comunicación puede ser implementada de muchas maneras, ya sea compartiendo memoria,
    o técnicas de paso de mensajes, en los cuáles los paquetes de datos son movidos entre
    procesos gracias al sistema operativo.

Detección de Errores
    El sistema operativo necesita tener conocimiento de todos los posibles errores que puedan
    ocurrir en el computador. Estos errores pueden ocurrir en la CPU o en la memoria del 
    equipo, pero también en otros dispositivos de entrada/salida así como en los programas
    de los usuaruos. Para cada tipo de error, el sistema operativo debe tomar la acción
    apropiada que asegure un funcionamiento correcto y consistente.

Asignación de recursos
    Cuando muchos usuarios están trabajando en el sistema o cuando muchas aplicaciones 
    se estén ejecutando al tiempo, el sistema operativo debe asignarles recursos a cada
    uno de estos usuario o aplicaciones.

    Muchos tipos de recursos son gestionados por el sistema operativos, por ejemplo, la
    pantalla, la impresora o la memoria.

Proteccion
    Esta tarea tiene que ver con el control del acceso a los recursos. La seguridad del
    sistema de elementos externos es muy importante. Tal seguridad inicia cuando cada 
    usuario tiene que autenticarse para entrar al equipo, indicando el usuario y la clave,
    y con ello tiene acceso a los recursos del computador.



