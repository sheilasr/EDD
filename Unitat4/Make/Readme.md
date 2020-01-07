#PAC03 EDD
*Practica* que forma parte de la asignatura *EDD*


Esta carpeta incluye un archivo Readme.md a modo de memoria. También incluye los ficheros correspondientes a las fuentes, encabezados y Makefiles. Por último, incluye un fichero gitignore.


Antes de iniciar la practica he instalado make en el sistema mediante: sudo apt install make. 


El primer ejercicio es la compilación de un fichero, en mi caso, primer.c --> hola 

Primero he creado el fichero primer.c con la orden "touch" y, a continuación, he instalado gcc mediante la orden: sudo apt install gcc. 

GCC es un copilador integrado del proyecto GNU para C entre otros lenguajes. Con este compilador se puede generar un programa ejecutable, en mi caso, lo he creado con "gcc primer.c -o hola".

La compilación involucra cuatro etapas: preprocesamiento, compilación, ensamblado y enlazado. El comando gcc realiza todo el proceso de una sola vez, pasando de un programa fuente escrito a un archivo ejecutable. GCC se emplea para un sólo archivo.

Otra forma de conseguir compilar un programa es utilizando el comando make. En este caso he utilizado la orden: make primer. Con esta orden, interpreta que el fichero fuente se llamará primer.c. Make realmente es una herramienta de construcción que invoca al compilador (que podría ser gc) en una secuencia determinada para recopilar múltiples fuentes y vincularlos entre sí. 

Al ejecutarlos ambos a través de la terminal aparece el mismo resultado "Hola món". Para ejecutarlos en el terminal he utilizado "/home/shesol/GitHub/Unitat4/Make/nombre_archivo", sustituyendo nombre_archivo por "primer" y por "hola" en cada caso. 


Para el segundo TO-DO primero he creado con la orden touch los tres archivos necesarios denominados: calcini.c, calcini.h y calculaini.c. Calcini.c tiene implementadas las funciones. Calcini.h contiene los encabezados de las funciones y, por último, calculaini.c tiene la forma de imprimir los resultados. 

Una vez creados estos archivos he ejecutado "gcc -c calcini.c -o calcini.o" para obtener el fichero objeto calcini.o. A continuación, he obtenido el fichero ejecutable mediante la orden: gcc calcini.o calculaini.c -o calculaini. He comprobado los resultados, ejecutando el programa con /home/shesol/GitHub/Unitat4/Make/calculaini y éste funciona correctamente. 

Para la segunda parte del ejercicio he añadido la nueva función a los tres archivos. En calc.c he añadido que se va a utilizar la funcion "major" y he declarado los dos valores a utilizar. En calc.h he incluido la cabecera de la función "major". Por último, en calcula.c he escrito el códido para imprimir la solución y que el programa señale cuál es el número mayor. Desde el terminal he ejecutado: "/home/shesol/GitHub/Unitat4/Make/calcula" y el resultado es correcto. Aperece la solución de las 4 operaciones anteriores y, además, aparece un mensaje indicando que el 10 es mayor. 


Para el último TO-DO primero he creado el fichero Makefile. Estos ficheros se incluyen en la misma carpeta raiz del proyecto y se indica en ellos que debe hacer "make" con los ficheros fuente para compilarlos. Primero se definen las variables al inicio del fichero. 

Posteriormente, se marcan los targets, es decir, qué ficheros se van a crear. A continuación, se listan los ficheros necesarios para generar este target (cada vez que le digamos a make que compile se asegurará de tener los archivos necesarios para ello) y, por último, las órdenes o pasos que se han de seguir. Por ejemplo, si en el terminal ponemos make calcula se ejecutará todo lo siguiente: $(CC) $(CFLAGS) calcula.c calc.o -o calcula.

En este paso se ha creado también un fichero .gitignore para mantener el proyecto limpio y que los ficheros .o no se suban a los repositorios. Igualmente, se pueden "limpiar" estos proyectos mediante make utilizando  "clean".

Además, se ha añadido un forma de distribuir el código, dejándolo lsito para su instanlación o comprimiéndolo mediante "dist" y "targz". 

Si se envierten las reglas en el Makefile, en principio no importa, ya que make construye por defecto el primero que le indicamos. 


