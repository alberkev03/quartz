---
tags:
- administracion
- sistemas-y-organizaciones
---

# Red Program Evaluation & Revision Technique (PERT)
Herramienta de gestión virtual para organizar, coordinar y cartografiar las tareas de un proyecto. Identifican el tiempo y los recursos necesarios para completar cada tarea. ![[Excalidraw/Red PERT]]

Como cada tarea depende de otras, un diagrama PERT permite visualizarlo y tomar decisiones acordes a las necesidades del proyecto. Permite también ver qué tareas tienen prioridad sobre otras, o la secuencia con la que deben realizarse. 

A diferencia de un [[Diagrama de Gantt]], una red PERT se emplea **antes** de comenzar un proyecto para separar las tareas grandes en otras más pequeñas. Un Diagrama de Gantt está pensado para usarse **durante** el proyecto para programar y gestionar esas tareas.

## Metodología
1. Se define el proyecto a realizar.
2. Se definen las actividades necesarias para completar el proyecto.
3. Se clasifican las actividades en el siguiente orden:
	1. Tipo de actividad, asignadas a una clave (Por lo general números o letras en orden) y ordenadas de primera a última.
	2. Predecesora. Se agrupan las tareas en base a cuál va antes. De esa manera, ordenamos y priorizamos las mismas.
	3. Tiempos. Establecemos un tiempo más probable, uno optimista, uno pesimista y el tiempo esperado. **El tiempo esperado es el usado en la red**.
		- Para el tiempo esperado usamos la fórmula:
		  $Te=(To+4(Tmp)+Tp)/6$
		  Tiempo esperado = (tiempo optimista + tiempo más probable*4 + tiempo pesimista)/6.
	4. Organizamos las actividades a través de módulos y flechas. 
		- Todos los nodos deben conectarse hasta el final. En caso de que no sea posible, se hace una actividad ficticia.

