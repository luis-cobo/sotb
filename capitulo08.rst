Linux
=====

GNU/Linux es un sistema operativo derivado de UNIX, que se distribuye en forma libre.

¿Qué es UNIX?
-------------

UNIX es un sistema operativo multitarea, multiusuario, creado en 1969 por los investigadores
Thompson y Ritchie de los Laboratorios Bell, en los Estados Unidos. Las primeras versiones fueron
escritas en assembler, pero muy pronto fue re-escrito en lenguaje C.

En sus primeros años, no se le utilizó comercialmente, sino que se lo usaba para proyectos de
investigación en laboratorios y se distribuía gratuitamente en las universidades, donde tuvo mucha
aceptación.

En 1975, Bell decidió comercializarlo. Dado que el sistema se vendía con una licencia que permitía
modificarlo y redistribuirlo, a lo largo del tiempo fueron surgiendo una gran variedad de sistemas
derivados del UNIX original. Los más conocidos, actualmente, son: Solaris, AIX, HPUX, SCO, BSD.

Por esta razón, varias veces se hizo necesario normalizar estos sistemas, para que cumplan con
determinadas normas (POSIX, UNIX95, etc), para permitir la compatibilidad entre los diferentes
sistemas.

De estas normas, el sistema operativo GNU/Linux satisface la norma POSIX-1, y casi completamente
la POSIX-2.

¿Qué es GNU?
------------

La sigla GNU significa *GNU is Not Unix*.

En 1984, Richard Stallman fundó el Proyecto GNU con el objetivo de conseguir un sistema operativo
libre y abierto. Esto es, un sistema operativo tal que los usuarios puedan usarlo, leer el código
fuente, modificarlo, y redistribuirlo.

A partir de ese momento, un gran número de colaboradores se fueron sumando al proyecto, desarrollando
software libre para reemplazar cada una de las herramientas del sistema UNIX.

La filosofía GNU apoya el crecimiento de la sociedad como un conjunto, haciendo especial hincapié en 
la valoración de las libertades personales, aún cuando esto puede estar en conflicto con intereses
empresariales.

¿Qué es Linux?
--------------

En 1991, Linus Torvalds completó el sistema con su kernel (que es la aplicación encargada de
comunicar los procesos con el hardware del computador). A este kernel lo bautizó Linux.

De esta manera, se formó el sistema GNU/Linux.

¿Qué es BSD?
------------

La Universidad de Berkeley estuvo relacionada con el desarrollo de los sistemas operativos UNIX.
Recibió de AT&T una versión gratuita de UNIX, y a partir de entonces comenzó a promover el
desarrollo de aplicaciones para UNIX dentro de la universidad.

Más adelante, desarrolló su propio sistema operativo UNIX, sin utilizar el código fuente de AT&T.
El kernel fue creado desde Berkeley, pero las herramientas utilizadas son en su mayoria GNU, es decir
las mismas que en el sistema GNU/Linux.

Existen actualmente 3 sistemas operativos libres, derivado de BSD: FreeBSD, OpenBSD y NetBSD.

¿Qué es X?
----------

El sistema operativo GNU/Linux cuenta con una interfaz gráfica, llamada XFree86 o simplemente
X.

El protocolo X fue desarrollado por el MIT, principalmente como un logro académico para proporcionar
un entorno gráfico a UNIX. La licencia mediante la cual se distribuye permite usarlo,
modificarlo, redistribuirlo e incluso relicenciarlo.

¿Qué son las distribuciones?
----------------------------

El código fuente del sistema GNU y del kernel Linux está accesible a todo el mundo, sin embargo,
hacer funcionar un sistema a partir del código fuente es bastante difícil. Por eso, un sistema operativo
se distribuye (normalmente) en formato binario, es decir ya compilado.

Poco después de que apareciera el kernel Linux, comenzaron a aparecer las primeras distribuciones,
que agrupaban versiones probadas de varios programas, junto con el kernel, de tal manera que
formaban un sistema operativo listo para usar.

A medida que fue pasando el tiempo, algunas distribuciones se fueron haciendo más sofisticadas,
otras desaparecieron, otras se hicieron comerciales y aparecieron mucha más. Existen distribuciones
de muchos tipos: distribuciones que ocupan menos de 1MB y distribuciones que llegan a ocupar 10 GBs;
distribuciones orientadas a una finalidad en especial (redes, seguridad, etc) y distribuciones de uso
general.

Cada usuario de GNU/Linux suele elegir la distribución con la que se siente más cómodo, y no
tiene sentido entrar en discusiones acerca de cuál es mejor.

A menos que aclaremos lo contrario, lo que se enseña en este curso es aplicable a la gran mayoría
de los sistemas UNIX, y a cualquiera de las distribuciones de GNU/Linux.

Introducción a Linux
--------------------

En el siguiente enlace podemos conocer más sobre el sistema operativo Linux 
`Manual práctico de Linux <https://www.edu.xunta.gal/centros/iesfelixmuriel/system/files/manual_practico_de_linux_alumnos.pdf>`_.

Taller 04: Ejercicios de Linux
------------------------------

1. Mostrar la carpeta donde te encuentras cuando ingresas a la terminal de Linux.
2. Crear 3 carpetas **docs**, **libros** y **tareas**.
3. Cambia a la carpeta **docs**. Crear un archivo de texto llamado “datospersonales” 
   que contenga su nombre completo y fecha de nacimiento dentro de él. Muestre el contenido del archivo. 
4. Sin moverte de **docs** haz una copia del archivo “datospersonales” dentro de la carpeta **libros**.
5. Muestra el contenido de la carpeta **docs** y de la carpeta **libros** sin moverte de la carpeta **docs**.
6. Presentar la ayuda o página de manual del comando **cal** para mostrar el calendario.   
7.  Mostrar el calendario del año en que usted nació.   
8.  Mostrar el calendario del mes y año en que nació Gabriel García Márquez.    
9.  Contar el número de líneas del archivo ``/etc/passwd``  
10. Muestra las 3 prímeras líneas y las 3 últimas líneas del archivo ``/etc/passwd``
