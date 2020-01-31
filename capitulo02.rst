Evolución de los Sistemas Operativos
====================================

Los Sistemas Operativos han evolucionado a través de los años. A continuación
revisaremos esta evolución a través del tiempo. Puesto que los Sistemas
Operativos han estado relacionados históricamente con la arquitectura de las
computadores en las cuales se ejecutan, analizaremos las generaciones
sucesivas de computadores para ver cómo eran sus sistemas operativos.

El primer prototipo real fue diseñada por el matemático inglés
Charles Babbage (1792-1871). Aunque Babbage consumía gran parte de su vida y
fortuna en el intento de construir su «maquina analítica», nunca logró que
funcionara de manera adecuada, ya que ésta era un diseño puramente mecánico y
con la tecnología de su época, no podía producir las ruedas, engranajes, levas y
demás partes mecánicas, con la precisión que él necesitaba. Sobra decir que la
maquina-analítica no tenía un sistema operativo.

.. figure:: fig03.jpg
   :alt: Máquina Analítica de Babbage

   Figura 3 Máquina Analítica de Babbage

La evolución de los Sistemas Operativos se puede clasificar de la siguiente manera:

* La primera generación (1945-1955): bombillas y conexiones.
* La segunda generación (1955-1965): Transistores y sistemas de procesamiento por lotes.
* La tercera generación (1965-1980): Circuitos integrados y Multiprogramación.
* La cuarta generación (1980-presente): Computadoras personales.


La primera generación (1945-1955): Tubos al vacío y conexiones.
---------------------------------------------------------------

Luego de los fallidos intentos de Charles Babbage, hubo un déficit de
construcción de computadoras digitales. Esto ocurre hasta la Segunda Guerra
Mundial. A mitad de la década de los años 40, Howard Airen (Harvard), Jon Von
Newman (Princeton), J.Prespe, R. Eckert y William Mauchley (Universidad de
Pennsylvania), así como Conrad Zuse (Alemania), entre otros, lograron
construir máquinas de cálculos mediante tubos al vacío. Estas máquinas eran enormes
y llenaban piezas completas con una increíble cantidad de tubos al vacío, pero eran
mucho más lentas que la computadora casera más económica en nuestros días.

.. figure:: fig04.jpg
   :alt: Computador de la primera generación 

   Figura 4 Computador de la primera generación

Toda la programación se llevaba a cabo mediante lenguaje máquina absoluto y
frecuentemente utilizaban conexiones para controlar las funciones básicas de
la máquina. La mayoría de los lenguajes de programación eran desconocidos
(incluso el ensamblador), no se oía de los Sistemas Operativos. El modo usual
de operación que consistía en pegar una hoja en la pared, ir al cuarto de
máquina, insertar una conexión en el computador y pasar unas horas,
esperando que ninguno de los 20,000 tubos al vacío se quemara durante la ejecución. La
mayoría de los problemas eran cálculos numéricos directos; por ejemplo, el
cálculo de valores de senos y cosenos.

A principios de la década de los ’50, la rutina mejora un poco con la
introducción de las tarjetas perforadas. Fue posible entonces escribir los
programas en estas tarjetas y dárselas al computador para que las lea en vez
de insertar conexiones; por lo demás, el proceso era el mismo.

.. figure:: fig05.jpg
   :alt: El computador ENIAC

   Figura 5 El Computador ENIAC

La segunda generación (1955-1965): Transistores y sistemas de procesamiento por lotes.
--------------------------------------------------------------------------------------

La introducción del transistor a mediados de los ’50, modificó radicalmente el
panorama. Los computadores se volvieron confiables, de manera que podían
fabricarse y venderse a clientes, con la esperanza de continuaran funcionando
lo suficiente como para realizar un trabajo en forma sin inconvenientes.

Debido a su alto costo, no debe sorprender el hecho de que las personas
buscaran por vías rápidas reducir el tiempo invertido. La solución que por lo
general se adoptó, fue el anteriormente mencionado «proceso por lotes».

.. figure:: fig06.jpg
   :alt: Procesamiento por lotes

   Figura 6 Procesamiento por lotes

En resumen las computadoras grandes de la segunda generación se usaban
primordialmente para cálculos científicos y de ingeniería, como la resolución
de ecuaciones diferenciales parciales. Estas máquinas generalmente se
programaban en FORTRAN y lenguaje ensamblador. Los sistemas operativos típicos
eran FMS (el Fortran Monitor System) e IBSYS, el sistema operativo de IBM para
la 7094.

La tercera generación (1965-1980): Circuitos integrados y Multiprogramación.
----------------------------------------------------------------------------

La máquina 360 de IBM fue la primera computadora que utilizó circuitos
integrados, lo cual proporcionó una gran ventaja en el precio y desempeño
respecto de las máquinas de la segunda generación, que se construían a partir de
transistores individuales. Se trabajó con un sistema operativo de la línea IBM
360. Los sistemas operativos similares de esta generación, producidos por
otros fabricantes de computadoras, realmente pudieron satisfacer en forma
razonable a la mayoría de los clientes. También se popularizaron técnicas
fundamentales, ausentes de los Sistemas Operativos de la segunda generación de
las cuales la más importante era la Multiprogramación.

.. figure:: fig07.jpg
   :alt: El IBM System/360

   Figura 7 El IBM System/360

En la IBM 7094,  cuando  el  trabajo  actual  hacía  una  pausa  para  esperar
que se  completara  una  operación de cinta  u  otra  operación  de  E/S,  la
CPU  simplemente  permanecía ociosa  hasta que la E/S terminaba. En los
cálculos científicos, con  gran  uso  de  CPU,  la  E/S  es poco frecuente,
así que el tiempo  desperdiciado  no es significativo. En el procesamiento de
datos comerciales, el tiempo de espera por E/S puede ser el 80 al 90% del
tiempo total, de modo que algo debía hacerse para evitar que la CPU estuviera
ociosa tanto tiempo.

La solución a la que se llegó fue dividir la memoria en varias secciones, con
un trabajo distinto en cada partición. Mientras un trabajo estaba esperando 
que terminara su E/S, otro podía estar usando la CPU. Si se podían tener en la
memoria principal suficientes trabajos a la vez, la CPU podía mantenerse
ocupada casi todo el tiempo. Tener múltiples trabajos en la memoria a la vez
requiere hardware especial para proteger cada trabajo contra espionaje por
parte de los demás, pero la 360 y otros sistemas de tercera generación estaban
equipados con este hardware.

.. figure:: fig08.png
   :alt: Particiones de Memoria

   Figura 8 Particiones de Memoria

Otro avance importante durante la tercera generación fue el crecimiento
fenomenal de las minicomputadoras, comenzando con la DEC PDP-1 en 1961. La
PDP-1 sólo tenía 4K de palabras de 18 bits, pero a US$120 000 por máquina
(menos del 5% del precio de una 7094), se vendieron  como pan caliente. Para
ciertos tipos de trabajos no numéricos, la PDP-1 era casi tan rápida como  la
7094, e hizo nacer una industria totalmente nueva. A esta máquina pronto
siguió una serie de Otras PDP (todas incompatibles, a diferencia de la familia
IBM), culminando en la PDP-11.

.. figure:: fig09.jpg
   :alt: El Sistema DEC PDP-11

   Figura 9 El Sistema DEC PDP-11

La cuarta generación (1980-presente): Computadoras personales.
--------------------------------------------------------------

Con la invención de los circuitos integrados a gran escala (LSI), chips que
contienen miles de transistores en un cm2 de silicio, nació la era del
computador personal. En términos de arquitectura,  lo computadores
personales no eran muy diferentes de las minicomputadoras de la clase  PDP-
11, pero en términos de precio sí que eran muy diferentes. Si bien la
minicomputadora hacía posible que un departamento de una compañía o
universidad tuviera su propio computador, el   chip microprocesador permitía
que un solo  individuo  tuviera  su  propio  computador personal.  Los 
computadores personales  más  potentes empleadas  por  empresas, 
universidades  e  instalaciones  del  gobierno  suelen  llamarse *estaciones de
trabajo*, pero en realidad sólo son computadores personales grandes. Por lo
regular estas máquinas están interconectadas mediante una red.

.. figure:: fig10.jpg
   :alt: El IBM PC XT de 1981

   Figura 10 El IBM PC XT de 1981

Dos sistemas operativos dominaron inicialmente el campo de los computadores
personales y las estaciones de trabajo: MS-DOS de Microsoft y UNIX. MS-DOS se
usaba ampliamente en la IBM PC y otras máquinas basadas en la CPU Intel 8088 y
sus sucesoras, la 80286, 80386 y 80486 (que en adelante llamaremos la 286, 386
y 486, respectivamente) y más tarde la Pentium y Pentium Pro. Aunque la
versión inicial de MS-DOS era relativamente  primitiva,  versiones 
subsecuentes   incluyeron características más avanzadas, muchas de ellas
tomadas de UNIX. El sucesor de Microsoft para MS-DOS, WINDOWS, originalmente
se ejecutaba encima de MS-DOS (es decir, era más un shell que un verdadero
sistema  operativo),  pero  a  partir  de  1995  se  produjo  una  versión 
autosuficiente  de  WINDOWS, WINDOWS 95®, de modo que ya no se necesita MS-DOS
para apoyarlo. Otro sistema operativo de Microsoft es WINDOWS NT, que es
compatible con WINDOWS 95 en cierto nivel, pero internamente se reescribió
desde cero.   

El otro competidor importante es UNIX, que domina en las estaciones de trabajo
y otros computadores de alto desempeño, como los servidores de red. UNIX es
popular sobre todo en máquinas basadas en chips RISC de alto rendimiento.
Estas máquinas por lo regular tienen la potencia de cómputo de una
minicomputadora, a pesar de estar dedicadas a un solo usuario, por lo que
resulta lógico que estén equipadas con un sistema operativo diseñado
originalmente para minicomputadoras, a saber, UNIX.

.. figure:: fig11.jpg
   :alt: Una estación de trabajo con UNIX

   Figura 11 Una estación de trabajo con UNIX

A mediados de los ’80 se produjo un incremento en las redes de computadoras
personales con sistemas operativos de red y sistemas operativos distribuidos.
En este tipo de sistemas, los de red, los usuarios eran consientes de la
existencia de varias computadoras interconectadas, otras conectadas a máquinas
remotas y realizar operaciones con archivos, ya sea copiar, mover desde una
máquina a otra. Cada computadora ejecuta su sistema operativo local y tiene su
propio usuario.

Su contraparte, el sistema operativo distribuido, es aquel que aparece ante
los usuarios como un sistema tradicional de un solo procesador, aun cuando
esté compuesto por varios procesadores. En un sistema distribuido verdadero,
los usuarios no deben ser consientes del lugar donde su programa se ejecute o
del lugar donde se encuentran sus archivos; eso debe ser manejado de forma
eficaz y automática por el sistema operativo.