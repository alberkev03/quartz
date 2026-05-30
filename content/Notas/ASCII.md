---
tags:
- software
- arquitectura-de-las-computadoras
---

# ASCII - American Standard Code for Information Interchange
- Uso universal en microprocesadores.
- Cada carácter se divide en dos partes: 
	1. Zona a la izquierda.
		- Separa los caracteres en prefijos, como mayúsculas, minúsculas, símbolos y números.
			- 0-31 - Caracteres no imprimibles. Sirven para controlar periféricos, impresoras, etc. Su clase es 000
			- 32-127 - Caracteres alfanuméricos. Su clase va desde el 010 al 111.
				- La letra “A” es el número 41 en código ascii, y en binario es `1000001`
	2. Numérica a la derecha.
		- Identifica al carácter. 
- Utiliza 7 bits. 2⁷ = 128 combinaciones (decimal). 
	- El octavo bit izquierdo (conocido como paridad) sirve para conservar el contenido de un byte. *Generalmente no usado*.

***
## Referencias
- [[Representación de la información.pdf]]
- [Tabla ASCII](https://www.ibm.com/docs/es/aix/7.1.0?topic=adapters-ascii-decimal-hexadecimal-octal-binary-conversion-table)
