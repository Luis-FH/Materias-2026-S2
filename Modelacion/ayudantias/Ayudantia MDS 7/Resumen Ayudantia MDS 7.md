---
tags:
  - Certamen-2-MDS
---

# Ayudantía MDS 7 — Programación lineal

## Enfoque

El Listado 4 practica la formulación de modelos de programación lineal. La tarea en cada ejercicio es traducir una situación a variables, una función objetivo, restricciones y dominios; el enunciado indica que no se pide resolver numéricamente los modelos.

La ayudantía recorre varios patrones que suelen aparecer en un certamen:

- **Mezcla de productos y recursos limitados:** carpintería, zapatos promocionales, automóviles y café.
- **Asignación uno a uno:** elegir un equipo de mantenimiento para cada máquina.
- **Elección de cantidades enteras:** cuando las decisiones representan personas, equipos o productos indivisibles.

## Método recomendado

1. Define qué significa cada variable y su unidad.
2. Escribe la función objetivo en las mismas unidades que el beneficio o costo del enunciado.
3. Convierte cada recurso disponible en una restricción; comprueba que las unidades coincidan.
4. Distingue restricciones de capacidad (`≤`), mínimos (`≥`), requerimientos exactos (`=`) y límites de demanda.
5. Especifica el dominio: no negatividad y, cuando corresponda, integralidad o variables binarias.
6. Lee el modelo junto con el enunciado y verifica que cada condición esté representada una sola vez y con el sentido correcto.

## Práctica recomendada

1. **Ejercicio 1, Carpintería:** practicar mezcla de productos, uso de madera y horas de trabajo.
2. **Ejercicio 3, Compañía de automotores:** expresar capacidades dadas como producción máxima de un solo tipo en términos de fracciones de capacidad; repetir con los mínimos de la parte (b).
3. **Ejercicio 4, Café Baqué:** combinar dos insumos, utilidades y límites de demanda.
4. **Ejercicio 2, The Really Big Shoe:** modelar cantidades de equipos patrocinados, presupuesto y material por equipo.
5. **Ejercicio 5, Asignación de mantenimiento:** practicar variables binarias, asignación uno a uno y minimización de costo.

Para prepararte para un certamen de 2 o 3 desarrollos, intenta formular primero cada problema sin mirar el solucionario. Después revisa, para cada restricción, qué frase del enunciado representa y qué unidad tiene cada término.

## Lista rápida para el certamen

- ¿La variable representa una cantidad de producto, una asignación o una decisión sí/no?
- ¿La función objetivo maximiza beneficio o minimiza costo?
- ¿Se incluyeron todos los recursos y sus disponibilidades?
- ¿Los límites de demanda son máximos, mínimos o igualdades?
- ¿Una asignación exige exactamente una opción por elemento y evita reutilizar recursos?
- ¿Las variables necesitan ser enteras o binarias?
