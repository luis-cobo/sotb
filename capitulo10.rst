Procesos en Python
==================

Python ofrece a través de su biblioteca de funciones ``os`` el acceso a las
llamadas al sistema que ofrece el sistema operativo. Algunas de las operaciones
que ofrece Python son las siguientes:

.. code:: python

    # Programa en Python para demostrar el uso de los comando fork y wait

    # Importar el modulo os
    import os 

    # Crear un proceso hijo 
    # usando el comando os.fork 
    pid = os.fork() 


    # Si el identificador del proceso no es cero
    # indica que el proceso es el papá
    if pid : 
        # Esperamos que el proceso hijo
        # complete su ejecución utilizando
        # el metodo os.wait
        status = os.wait() 
        print("\nEstamos en el proceso padre-") 
        print("El PID del hijo es:", status[0]) 
    else : 
        print("Estamos en el proceso hijo-") 
        print("Identificador del proceso:", os.getpid()) 
        print("Hola todos!!") 
        print("Nos vamos") 
        

También tenemos operaciones como:

``os.kill``
    Para enviar una señal al proceso hijo. Algunas de las señales son informativas
    pero otras pueden conducir a que el proceso hijo finalice su ejecución.

``os.system``
    Para ejecutar un programa, creando un nuevo proceso para tal fin.

``os.execlp``
    Para ejecutar un programa, reemplazando el proceso actual.

``sys.exit``
    Para finalizar el proceso actual.
