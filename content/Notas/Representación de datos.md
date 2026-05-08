---
tags:
  - software
  - arquitectura-de-las-computadoras
---

# Representación de datos
- Usamos código [[Circuitos Lógicos|Binario]] de 0s y 1s.
	- 0 → Apagado.
	- 1 → Encendido.
	- Con estas unidades representamos todos los datos de una computadora. 
		- Unidad mínima de información.
## Unidades de medida
- 8 bits = 1 byte.
- 1024 bytes = 1 kilobyte.
- 1024 kilobytes = 1 megabyte.
- 1024 megabytes = 1 gigabyte.
- 1024 gigabytes = 1 terabyte.
- 1024 terabytes = 1 petabyte.
- 1024 petabytes = 1 exabyte.
- 1024 exabytes = 1 zettabyte.
- 1024 zettabytes = 1 yottabyte.
## Método
- Dividir la memoria en celdas de longitud fija y predeterminada de bits. 
	- Combinamos bits para lograr un símbolo deseado. 
	- Asigna dirección en [[Arquitectura Von Newmann|memoria]].
	- Se establecen grupos predeterminados:
		- Números del 0 al 9 (10 grupos de bits).
		- Letras del alfabeto (26 grupos de bits).
		- Otros símbolos.
		- Mínimo 36 combinaciones para letras y números.
			- 1 bit → 2¹ combinaciones.
			- 2 bits → 2² combinaciones.
			- 3 bits → 2³ combinaciones.
	- Grupos de 6 bits logran 2⁶ = 64 combinaciones. 
		- **Conjunto de [[Códigos]] = carácter**.
- Los datos se transmiten y convierten mediante una [[Codificación]] y [[Decodificación]].

***
## Referencias
- [[Representación de la información.pdf]]
