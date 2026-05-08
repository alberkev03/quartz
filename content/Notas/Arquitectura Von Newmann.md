# Arquitectura Von Newmann
Diseño que se usa para almacenar instrucciones y datos.
Define los siguientes elementos:
- CPU.
- Memoria principal.
- Controlador de entrada - salida.
- Buses de sistema.
![[Pasted image 20260331090347.png]]
## CPU
Repite una serie de pasos en los que revisa la memoria para leer la próxima instrucción a ejecutar. Cuando la CPU está implementada en un único circuito integrado, se lo llama **[[Microprocesador]]**.
### Componentes de la CPU
- Unidad de control: Lee instrucciones almacenadas en la memoria principal y genera señales de control necesarias para un ejecutarlas. 
	1. Contador de programa: apunta la dirección de memoria de la próxima instrucción a ejecutar.
	2. Registro de instrucción: Guarda la instrucción en ejecución.
	3. Decodificador: Interpreta la instrucción. 
	4. Reloj: Señal sincrónica.
	5. Secuenciador: Activa el orden adecuado de unidades para ejecutar la instrucción. 
- Unidad aritmético lógica (ALU): Realiza operaciones aritméticas y lógicas con los datos ingresados. Tanto los datos como los resultados se encuentran en los registros de la CPU. 
- Banco de registros: Espacio de almacenamiento de datos con los que trabaja la CPU. Provienen de la memoria principal y son más rápidos de trabajar.
	Los registros se distinguen de la siguiente manera:
	1. Registros de datos.
	2. Registros de direcciones a datos en la memoria.
	3. Registros de control de estado de la CPU.
- Buses: Transportan información entre elementos de CPU.
	- Bus de datos.
	- Bus de control.
## Memoria principal
Guarda información accesible para la CPU. Suele estar formada por dos áreas:
- Memoria RAM (Random Access Memory).
- Memoria ROM (Read Only Memory). Solo permite lectura de datos y es persistente; no pierde su contenido al apagarse la computadora.
## Controladores de I/O
- Periféricos de entrada.
- Periféricos de salida. 
## Buses del sistema
Vías de comunicación que mueven al información.
- Serie de pistas que transportan datos.
- El número de líneas de un bus determina los bits que puede transportar en paralelo. Gobernados por un reloj.
### Bus de datos
Transporta datos, tanto información como instrucciones. El ancho de bits determina la cantidad de datos, pero suele ser: ^608c36
	- **8bits**
	- **16bits**
	- **32bits**
	- **64bits** ^6b9f3a
### Bus de direcciones
Indica el origen y/o destino de los datos, ya sea en la memoria o en donde esté mapeado un periférico.
### Bus de control
Proporciona señales para coordinar tareas. Algunas de ellas son:
- CLK: Frecuencia de reloj.
- CS (Chip Select): Activa el chip a utilizar.
- READY: Verifica si el dispositivo está disponible.
- R/W: Determinar lectura o escritura.

***
## Referencias
[[Arquitectura de Von Newmann.pdf]]

#arquitectura-de-las-computadoras #computadoras #hardware
