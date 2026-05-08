---
tags:
- software
- arquitectura-de-las-computadoras
---

# EBCDIC - Extended Binary Coded Decimal Interchange Code
- Usado en equipos de IBM.
- Cada caracter se representa por un conjunto de 8 bits dividido en dos partes: 
	1. Zona a la izquierda.
	2. Numérica a la derecha.
- Alternativa al código [[ASCII]].
- Su [[Codificación]] es la siguiente.
	1. Primeros 2 bits separan caracteres especiales (01), minúsculas (10), y mayúsculas o números (11).
	2. Siguientes 2 bits suman a la clase.
	3. Últimos 4 bits determinan el caracter.
***
## Referencias
- [[Representación de la información.pdf]]
