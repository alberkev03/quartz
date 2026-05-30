---
tags:
- software
- arquitectura-de-las-computadoras
- matematica
---

# Representación de datos numéricos
No es fácil representar números en una computadora.
- Existen dos métodos fundamentales para hacer:
	- Codificar dígitos decimales individualmente.
	- Codificar el número completo. En este caso, tenemos dos formatos: **Punto fijo** y **números de punto flotante**.
## Números de punto fijo
- Madera más “natural” de escribir un número en memoria.
- Para operaciones matemáticas eficaces, se requieren números de bytes fijos, los cuales se extienden hasta abarcar el **mayor número representable** necesario para la operación.
- No es posible usar signos + o -. Usamos convenciones.
	- Bit 0 para positivo.
	- Bit 1 para negativo.
- Forma binaria directa: Se representa directamente con el binario, de 00000000 a 11111111 (0 a 255 en decimal).
	- Como desventaja, solo se representan números positivos, y se nos limita la operación a 255. 
### Representación de números negativos
La forma binaria directa es eficaz con números positivos, pero presenta dificultades al usar negativos. Se proponen las siguientes soluciones:
- Binario con signo. Indicado por el **bit más significativo** (el primero de la izquierda). “0” para positivo, “1” para negativo. Reducimos de 255 a 127 y perdemos un bit para representar el signo. 
- Palabra de memoria. Cadena de bits relacionada con un bloque fijo de memoria. [[Unidades de memoria]].
	- Permite trabajar con números más grandes en caso de que lo necesitemos. Por ejemplo, con 16bits podemos trabajar desde -32767 a 32767 (último bit para signo, restantes 15 para el número. 2¹⁵ = 32.768), con 32bits desde -2.147.483.647 a 2.147.483.647, etc.
	- Impone que se reserve un bit para el signo.
- Complemento a 1. 
	- Otra manera de representar números en binario, sobre todo los negativos. La fórmula es la siguiente:
	$n=e+f(e)*b^d$
		1. Se calcula la frontera[^1] usando la fórmula $b^d/2$.
		2. usamos la fórmula $f(e)$.
			- Si e > 0 = 0.
			- Si e < 0 = 1.
		3. El número natural es el que la máquina convierte a binario.
	- De esta manera, por ejemplo, calculamos el natural de -20 en un byte.
		- $n=(-20)+1*2^8$ = 236. En binario: 11101100.
	- De manera más sencilla, todos los negativos son el inverso de los positivos. Por ejemplo: 0011 (3) → 1100 (-3). 
- Complemento a 2. Obtenemos el complemento (número negativo) realizando el complemento a 1 *y además* se la suma un 1 al bit menos significativo (extremo derecho). Ejemplo: 0111 (7) → 1001 (-7).
	- Proceso simple para los procesadores. Soluciona el problema de tener dos ceros (0000 y 1111).
- Cero desplazado. Usamos la fórmula $N=E+F$ si conocemos el Natural, o $E=N-F$ si conocemos el Entero. F es la frontera y se calcula como $b^d/2$.
	- Por ejemplo, tenemos el número entero 30 y lo queremos representar en una secuencia de 8 bits. Entonces: 
		1. N=30+128=158.
***
## Representación de punto flotante
- Sirve para representar fracciones decimales. Se expresa de forma **exponencial normalizada**.
- El objetivo es no desperdiciar bits representando ceros. En lo lugar de eso, por cada cero no representado corresponde una potencia decimal, de la siguiente manera.
	- Si el número es menor que cero, se desplaza el exponentes de manera que el número quede a partir de un “0,”. 
		- Si se desplaza la coma hacia la derecha, el exponente será negativo.
		- Si se desplaza la coma hacia la izquierda, el exponente será positivo.
	- La cantidad de dígitos que nos desplazamos va a ser igual al exponente de la operación decimal. De manera que quedría así:
		- $13,76$ -> $0,1376*10^2$
		- $978$ -> $0,978*10^3$
		- $0,00076$ -> $0,76*10⁻^3$
	- Estos números se denominan **mantisa normalizada**. De manera que la fórmula sería $SM*10^e$, o Signo y Mantisa por 10 elevado al exponente correspondiente.
- ¿Y cómo se representa el número en una palabra de memoria? Por ejemplo, en una palabra de 32bits:
	- Primer bit para el signo.
	- 7 bits para el Exponente.
	- 24 bits para la mantisa.
- El BMS determina el signo **de la mantisa**. Para calcular el exponente, se realiza una [[Técnica]] de desplazamiento, similar al cero desplazado.
	- Con 7 bits, tenemos 128 combinaciones. Con frontera, va desde -64 a 64.
	- Usamos la fórmula $C=E+64$ para calcular el número real. Es decir, Característica almacenada es igual a Exponente más 64. Con esta operación, la máquina calcula el exponente real y puede representar correctamente todo el número.
***
## Referencias
- [[Representación de la información.pdf]]
## Ver más
- [[Representación de datos]]
- [[Arquitectura Von Newmann]]

[^1]: Frontera: Límite dentro de un rango de números que determina a partir de cuál se empiezan a representar los números negativos. Por ejemplo, en un byte, donde se pueden representar 256 números, hasta el 128 corresponde a un positivo, y de ahí en adelante corresponde a negativo. Usamos el complemento a 1 o a 0 para calcular a qué número entero corresponde el natural negativo.
