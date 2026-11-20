---
tags:
  - Certamen-2-MDS
---

# Ayudantía MDS 8 — Formulación de modelos

## Enfoque

El Listado 5 amplía la práctica de programación matemática con problemas de producción, cobertura de turnos, asignación, selección con condiciones lógicas y transporte. En todos los ejercicios se pide formular el modelo; no se solicita resolverlo numéricamente.

Los patrones principales son:

- **Producción y recursos:** maximizar utilidad respetando capacidades, materias primas y alternativas de proceso.
- **Cobertura de turnos:** satisfacer mínimos de servicio con la menor cantidad de personal.
- **Asignación:** emparejar estudiantes y mentores considerando preferencias y compatibilidad.
- **Selección binaria y lógica:** elegir candidatos y representar condiciones del tipo “si asiste A, también debe asistir B”.
- **Transporte:** satisfacer demandas desde varios orígenes al menor costo.

## Método recomendado

1. Define los índices y las variables antes de escribir restricciones.
2. Da unidades a cada parámetro y variable; en transporte, por ejemplo, especifica litros.
3. Para recursos, suma consumo por unidad y limita por disponibilidad.
4. Para cobertura, suma todas las variables que cubren cada período y exige alcanzar la demanda mínima.
5. Para asignación, usa binarias y restricciones de asignación exacta.
6. Para condiciones lógicas, traduce cuidadosamente cada implicación o incompatibilidad a desigualdades.
7. Termina con los dominios y valida que el modelo permita las combinaciones descritas.

## Práctica recomendada

1. **Ejercicio 1, Dos productos:** una mezcla de productos con horas de trabajo, horas de máquina y producción mínima.
2. **Ejercicio 2, La herrería medieval:** combina varios recursos, dos rutas de producción para hachas y distintos precios de venta.
3. **Ejercicio 3, Turnos de patrullaje:** practica cobertura de períodos consecutivos y minimización de personal.
4. **Ejercicios 4 y 5, Mentores e invitados:** trabaja asignación binaria, compatibilidad e implicaciones lógicas.
5. **Ejercicio 6, Transporte de petróleo:** practica variables por origen–destino, balance de oferta y demanda, y costo unitario.

## Qué priorizar para un certamen de 2 o 3 desarrollos

Practica presentar cada respuesta de forma ordenada: **conjuntos e índices → parámetros → variables → función objetivo → restricciones explicadas → dominios**. En especial:

- En producción, separa recursos de proceso de límites comerciales y explica las rutas alternativas.
- En cobertura, verifica qué turnos contribuyen a cada intervalo, incluido el cruce de medianoche.
- En asignación y selección, identifica qué variables son binarias y qué significa cada combinación prohibida.
- En transporte, revisa que toda demanda se atienda y que ninguna oferta exceda su capacidad.
- Haz una prueba rápida con unidades y casos límite: ¿un recurso se usa más de lo disponible?, ¿una variable puede tomar un valor fraccionario cuando cuenta personas?, ¿una incompatibilidad quedó realmente prohibida?

## Apunte avanzado: matrices para problemas de asignación

Una matriz es especialmente útil cuando cada decisión consiste en emparejar un elemento de un conjunto con uno de otro conjunto: trabajador–tarea, conductor–jornada, estudiante–mentor o equipo–máquina. La matriz **no reemplaza el modelo**; organiza los datos de las parejas posibles y permite calcular el costo o puntaje de cada asignación antes de formular la función objetivo.

### 1. Definir filas, columnas y contenido

Fija primero qué representa cada fila y cada columna. Luego define un parámetro $C_{ij}$ para cada pareja: por ejemplo, horas requeridas, costo, distancia, tiempo o puntaje. Conserva el mismo orden de filas y columnas en todas las matrices y tablas. Un intercambio de orden puede producir un modelo formalmente correcto pero con los datos asociados a las parejas equivocadas.

Para el problema de los conductores, las filas representan los viajes $A_i$ y las columnas los viajes $B_j$. El elemento $C_{ij}$ mide las horas de inactividad si esos dos viajes forman la jornada de un conductor.

### 2. Calcular el costo por pareja antes de llenar la matriz

No siempre basta con copiar un dato del enunciado. Si el costo depende de una secuencia, calcula cada alternativa respetando duración, descanso y periodicidad. Para un horario diario, trabaja con horas entre 0 y 24 y usa el módulo para incluir el día siguiente:

$$
\text{espera}=(\text{salida siguiente}-\text{salida inicial}-\text{duración del viaje})\bmod24.
$$

Descarta una secuencia que no cumpla el descanso mínimo. A las restantes réstales el descanso obligatorio; el menor excedente es el costo de esa pareja. Así, con salidas A1 a las 06:00 y B3 a las 15:00, y viajes de 6 horas, el orden A1→B3 deja 3 horas de espera y no es admisible. El orden B3→A1 del día siguiente deja 9 horas; luego de las 4 horas de descanso, quedan 5 horas de inactividad. Por tanto, $C_{1,3}=5$.

En general, si $R$ es el descanso mínimo y $W^{AB}_{ij},W^{BA}_{ij}$ son las esperas de los dos órdenes, entonces:

$$
C_{ij}=\min\Big(
\{W^{AB}_{ij}-R:W^{AB}_{ij}\ge R\}
\cup
\{W^{BA}_{ij}-R:W^{BA}_{ij}\ge R\}
\Big).
$$

Al terminar, revisa las unidades y clasifica cada pareja como factible o no factible. Una matriz con costos no significa que todas las combinaciones estén permitidas.

### 3. Crear la matriz de decisión

Define $x_{ij}=1$ si se elige la pareja $(i,j)$ y $0$ si no. En un emparejamiento uno a uno, las filas y columnas deben cubrirse exactamente una vez:

$$
\sum_jx_{ij}=1\quad\text{para cada elemento de la primera lista},\qquad
\sum_ix_{ij}=1\quad\text{para cada elemento de la segunda lista}.
$$

Si hay parejas prohibidas, excluye sus variables del modelo o impón $x_{ij}=0$. No las trates como costos ordinarios ni olvides comprobar que las demás parejas todavía permiten una asignación completa.

### 4. Escribir la función objetivo sin ambigüedad

Para costos, minimiza:

$$
\min\sum_i\sum_j C_{ij}x_{ij}.
$$

Cada término aporta el costo de una pareja solo cuando esa pareja se selecciona. Para puntajes o preferencias, normalmente se maximiza la misma suma. La formulación con sumatorias es clara y segura; si se usa notación matricial, el producto debe ser entrada por entrada seguido de la suma, no una multiplicación matricial ordinaria.

### 5. Cuándo conviene este método

- **Conviene** cuando hay muchas parejas posibles, varias alternativas por pareja o cálculos repetitivos; la matriz permite auditar cada coeficiente $C_{ij}$ por separado.
- **También conviene** para comprobar la estructura: cada fila y columna debe corresponder al elemento esperado, y cada decisión seleccionada debe aparecer una sola vez.
- **No basta por sí sola** cuando hay capacidades adicionales, decisiones de apertura, incompatibilidades complejas o varias tareas por trabajador; esas condiciones requieren restricciones adicionales.
- Si la matriz es cuadrada y solo hay asignación uno a uno con costos, se puede aplicar un algoritmo clásico de asignación. La matriz de costos es el insumo de ese método; las restricciones del modelo explican qué significa una solución factible.

En un certamen, presenta primero la interpretación de $C_{ij}$ y sus unidades; después define $x_{ij}$, la función objetivo, las restricciones por fila y columna, y el dominio binario. Comprueba al menos una celda a mano —incluyendo una que cruce medianoche, si corresponde— antes de confiar en toda la matriz.
