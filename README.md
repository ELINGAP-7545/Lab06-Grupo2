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
 
 ![banco de registros](https://user-images.githubusercontent.com/62779527/81987797-010cbd80-9600-11ea-97ec-07048d09efbd.PNG)


En el siguiente laboratorio veremos como podemos realizar la visualización de un banco de registros el cual cuenta con 4 bits de salida y 2 de entrada, con este banco de registros el cual visualizaremos por medio de quartus podremos entender el comportamiento del banco de registros.

Muchos circuitos digitales necesitan inicializarse antes de comenzar a trabajar normalmente. Su funcionamiento se divide en un estado de arranque, donde se inicializan los valores de los registros y un estado de régimen permanente donde se realiza la función para la que han sido diseñados.

Para lograr esto necesitamos un circuito de inicialización que nos genere una señal de reloj la cual cada 50000 giros por segundo (este valor del reloj es comprendido solo para la implementación en labsland) genera un flanco de subida automático durante todo el funcionamiento de la máquina. Al llegar el primer flanco de reloj, se captura el 1 y se saca por su salida, generando el flanco de subida para realizar la inicialización. Para el resto de ciclos de reloj esta señal siempre estará a 1


![rst](https://user-images.githubusercontent.com/62779527/81989029-1a166e00-9602-11ea-8e40-fe1c8e523a5d.PNG)





## Archivo testbench

## Vídeo de la implementación.

## Código HDL 

## **Opcional. Da mas puntos:**

## Pre cargar el banco de registro con información: 

para este proceso debemos sintetizar nuestro archivo usando $readmenh para el archivo $readmen(este archivo es una extensión la cual nos da a entender que se deberá leer el archivo $readmenh con el cual a su vez nos llevara a el archivo que se encuentra en el src del baoratorio 6 como Reg16.men).

 Existen 2 tipos de archivos el $readmend el cual la informacion es tomada enbinario y el  $readmenh el cual es tomado en hexadecimal. 

Al cargar el archivo $readmenh veremos que nuestros leds se encenderán y visualizaremos que nuestro codigo funciona correctamente





## Documentación

Se realizó un análisis del laboratorio de Banco de Registros de una manera más clara con ayuda del docente, explicando cómo funcionaría el programa o código en las labsland definiendo las entradas

wire [3:0] datW; Este cable, tiene el dato ingresado que se desea grabar en la memoria.

wire [1:0] addrRa; Este cable, nos muestra en el display 1 el dato requerido por el usuario de una de las posiciones de la memoria.

wire [1:0] addrRb; Este cable, nos muestra en el display 2 el dato requerido por el usuario de una de las posiciones de la memoria.

wire RegWrite; Este cable, su estado normal es 0, se coloca en estado 1 para autorizar escribir el dato en la dirección indicada. 

También realizar sus respectivas asignaciones

assign addrW = V_SW[5:4];

assign datW = V_SW[3:0];

assign addrRa = V_SW[9:8];

assign addrRb = V_SW[7:6];

assign RegWrite = V_BT[0];

Determinado la posición y la cantidad de switch a utilizar para su respectivo ingreso de datos

![rst](https://github.com/ELINGAP-7545/Lab06-Grupo2/blob/master/Configuraci%C3%B3n%20Banco%20Registros.JPG)

## Archivo `testbench` el cuál debe simular la escritura de 16 registros y 8 lecturas mas el rst, el resultado de la simulación debe visualizarse en diagrama de tiempo.

## Vídeo de la implementación.

## Código HDL de la solución.
