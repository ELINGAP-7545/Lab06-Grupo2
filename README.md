# GRUPO 2
# lab06 Diseño de banco de Registro

# Introducción

Para este paquete de trabajo, deben estar inscrito en un grupo y clonar la información del siguiente link [WP06](https://classroom.github.com/g/XHLhUCe3). Una vez aceptado el repositorio debe descargarlo en su computador, para ello debe clonar el mismo. Si no sabe cómo hacerlo revise la metodología de trabajo, donde se explica el proceso

Las documentación deben estar diligencia en el archivo README.md del repositorio clonado.

Una vez clone el repositorio, realice lo siguiente:


## Descipción 
Se debe diseñar un banco de registro tal que:

* El banco de registro debe tener 16 registros de R/W.
* Permitir la lectura de 2 registros  simultáneamente 
* Permitir la escritura  de 1 registro, acorde a la señal de control regwrite
* Contar con señal de rst, la cual  ponga  todos los registros en un valor conocido.

![cn](https://github.com/Fabeltranm/SPARTAN6-ATMEGA-MAX5864/blob/master/lab/lab07-BancosRgistro/doc/caja%20negra.png)

* Visualizar la información, en al menos dos display de 7 segmentos (información de cada registro leído).
* El ingreso de la información se debe hacer por medio de los interruptores.

**Opcional. Da mas puntos:**
* Parametrizar el tamaño de palabra de cada registro  y la cantidad de registro ( Por defecto =4 bits). Se recomienda leer el documento de este [link](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-884-complex-digital-systems-spring-2005/related-resources/parameter_models.pdf) .
* Pre cargar el banco de registro con información.  _Usar $readmenh_  (Investigar: "Initialize Memory in Verilog").

Entregables:

* Documentación
* Archivo `testbench` el cuál debe simular la escritura de 16 registros y 8 lecturas mas el rst, el resultado de la simulación debe visualizarse en diagrama de tiempo.
* Vídeo de la implementación.
* Código HDL de la solución.
.

 ![caja](https://github.com/Fabeltranm/SPARTAN6-ATMEGA-MAX5864/blob/master/lab/lab07-BancosRgistro/doc/banco%20registro.png)
 
 
# SOLUCIÓN 

 ## Diseño de banco de Registro:

En el siguiente laboratorio veremos como podemos ralizar la visualizacio de un banco de registros el cual cuenta con 4 bits de salida y 2 de entrada, con este banco de registros el cual visualizaremos por medio de quartus podremos entender el comportamiento del banco de registros.

Muchos circuitos digitales necesitan inicializarse antes de comenzar a trabajar normalmente. Su funcionamiento se divide en un estado de arranque, donde se inicializan los valores de los registros y un estado de régimen permanente donde se realiza la función para la que han sido diseñados.

Para lograr esto necesitamos un circuito de inicialización que nos genere una señal de relog la cual cada 50000 giros por segundo genera un flanco de subida automatico durante todo el funcionamiento de la maquina. Al llegar el primer flanco de reloj, se captura el 1 y se saca por su salida, generando el flanco de subida para realizar la inicialización. Para el resto de ciclos de reloj esta señal siempre estará a 1

## Archivo testbench

## Vídeo de la implementación.

## Código HDL 

**Opcional. Da mas puntos:**

## Pre cargar el banco de registro con información: 

para este proceso debemos sintetizar nuestro archivo usando $readmenh (este archivo es una extensión las cual nos da a entender que se deberá leer el archivo menh con el cual a su vez nos llevara a el archivo que se encuentra en el src del baoratorio 6 como reg16.men).

Al cargar el archivo $readmenh veremos que nuestros leds se encenderán y visualizaremos que nuestro codigo funciona correctamente





## Documentación



## Archivo `testbench` el cuál debe simular la escritura de 16 registros y 8 lecturas mas el rst, el resultado de la simulación debe visualizarse en diagrama de tiempo.

## Vídeo de la implementación.

## Código HDL de la solución.
