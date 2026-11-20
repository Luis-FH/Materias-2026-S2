---
tags:
  - Certamen-2-MDS
---

# Solucionario — Listado 5: Formulación de Modelos

El listado pide formular los modelos, no resolverlos numéricamente. Por ello, las respuestas siguientes especifican las variables, los objetivos, las restricciones y los dominios. Después de cada modelo se explica la lógica de formulación y qué conviene comprobar en un certamen.

## 1. Dos productos

### Modelo

Sean $x_1,x_2$ las unidades de los productos 1 y 2.

$$
\max\quad 300\,000x_1+500\,000x_2
$$

sujeto a:

$$
\begin{aligned}
25x_1+15x_2&\le1\,900
&&\text{horas de trabajo},\\
7x_1+12x_2&\le940
&&\text{horas de máquina},\\
x_1&\ge20,\\
x_2&\ge20,\\
x_1,x_2&\in\mathbb Z_{\ge0}.
\end{aligned}
$$

### Por qué funciona y qué revisar

Cada producto consume horas de trabajo y de máquina, así que se construye una restricción distinta para cada recurso. El beneficio por unidad forma la función objetivo. Los mínimos técnicos se escriben como cotas inferiores. Revisa que no se intercambien los consumos de las dos máquinas ni los beneficios.

## 2. La herrería medieval

### Modelo

Sean:

- $s_T$: espadas templadas.
- $s_N$: espadas no templadas.
- $h_1$: hachas fabricadas solo en la máquina 1.
- $h_{12}$: hachas fabricadas en ambas máquinas.

Definimos $s=s_T+s_N$ y $h=h_1+h_{12}$. El costo de metales es \$65 por espada (\$15 de plata y \$50 de oro) y \$55 por hacha (\$30 de plata y \$25 de oro). Por tanto, las utilidades unitarias netas especificadas son \$135 por espada templada, \$85 por espada no templada y \$125 por hacha.

$$
\max\quad 135s_T+85s_N+125(h_1+h_{12})
$$

sujeto a:

$$
\begin{aligned}
\frac{s_T+s_N}{200}+\frac{h_1+h_{12}}{220}
&\le1 &&\text{capacidad mensual compartida},\\
3(s_T+s_N)+6h_1+2h_{12}
&\le480 &&\text{horas de máquina 1},\\
2(s_T+s_N)+3h_{12}
&\le480 &&\text{horas de máquina 2},\\
(s_T+s_N)+2(h_1+h_{12})
&\le600 &&\text{plata (kg)},\\
2(s_T+s_N)+(h_1+h_{12})
&\le500 &&\text{oro (kg)},\\
s_T&\le25 &&\text{máximo de espadas templadas},\\
s_T,s_N,h_1,h_{12}&\in\mathbb Z_{\ge0}.
\end{aligned}
$$

La restricción de capacidad compartida interpreta “200 espadas o 220 hachas” como la capacidad mensual total expresada en fracciones de producción pura. Se separan las dos rutas de hachas porque sus tiempos de máquina son distintos.

### Por qué funciona y qué revisar

La primera tarea es separar productos que tienen precios o procesos distintos: espada templada y no templada, y hacha por cada ruta. Luego se arma el costo neto con los precios de venta menos el costo de los metales. Cada recurso tiene su propia restricción: capacidad de producción, tiempo de cada máquina y disponibilidad de plata y oro. Comprueba que la ruta $h_1$ no consuma tiempo en la máquina 2 y que $h_{12}$ use ambas. La formulación supone que los costos de metales son los únicos costos de producción indicados.

## 3. Turnos de patrullaje

### Modelo

Sean $x_1,\ldots,x_6$ los policías asignados a turnos que comienzan, respectivamente, a las 12:00, 16:00, 20:00, 00:00, 04:00 y 08:00. Cada turno cubre ocho horas consecutivas.

$$
\min\quad x_1+x_2+x_3+x_4+x_5+x_6
$$

sujeto a:

$$
\begin{aligned}
x_1+x_6&\ge100 &&12{:}00\text{–}16{:}00,\\
x_1+x_2&\ge250 &&16{:}00\text{–}20{:}00,\\
x_2+x_3&\ge400 &&20{:}00\text{–}24{:}00,\\
x_3+x_4&\ge500 &&00{:}00\text{–}04{:}00,\\
x_4+x_5&\ge200 &&04{:}00\text{–}08{:}00,\\
x_5+x_6&\ge150 &&08{:}00\text{–}12{:}00,\\
x_i&\in\mathbb Z_{\ge0} &&i=1,\ldots,6.
\end{aligned}
$$

### Por qué funciona y qué revisar

Se minimiza la dotación total. Cada período de cuatro horas queda cubierto por los dos turnos consecutivos que lo atraviesan. En particular, el período de medianoche se cubre con los turnos que empiezan a las 20:00 y a las 00:00. Revisa el ciclo completo de seis intervalos para no omitir el cruce de día.

## 4. Asignación de mentores

### Modelo

Sean $I$ los estudiantes de primer año y $J$ los mentores de segundo año, con $|I|=|J|=M$. Para cada pareja $i,j$, $P_{ij}$ y $F_{ij}$ son los puntajes de preferencia del estudiante y del mentor, y $C_{ij}\in\{0,1\}$ indica compatibilidad.

Sea $x_{ij}=1$ si se asigna el mentor $j$ al estudiante $i$, y 0 en caso contrario.

$$
\max\quad \sum_{i\in I}\sum_{j\in J}(P_{ij}+F_{ij})x_{ij}
$$

sujeto a:

$$
\begin{aligned}
\sum_{j\in J}x_{ij}&=1 &&i\in I,\\
\sum_{i\in I}x_{ij}&=1 &&j\in J,\\
x_{ij}&\le C_{ij} &&i\in I,\ j\in J,\\
x_{ij}&\in\{0,1\} &&i\in I,\ j\in J.
\end{aligned}
$$

### Por qué funciona y qué revisar

Se suman las dos preferencias para favorecer parejas valoradas por ambas partes. Cada estudiante recibe exactamente un mentor y cada mentor queda asignado exactamente a una persona. La condición $x_{ij}\le C_{ij}$ prohíbe asignar parejas incompatibles. Revisa que maximizar puntaje no permita asignaciones múltiples; eso lo evitan las dos familias de igualdades.

## 5. La lista de invitados

### Modelo

Sean binarias $p,s,m,l,j$, que valen 1 si asisten Paolo Toth, Peter Sellers, Matt Groening, Linus Torvalds y Jorge Jiménez, respectivamente. Sus contribuciones netas están expresadas en miles de unidades monetarias.

$$
\max\quad 120p+500s+200m+100l+250j
$$

sujeto a:

$$
\begin{aligned}
p&\le l
&&\text{Paolo requiere la asistencia de Linus},\\
p+s+m&\le2
&&\text{no asisten juntos Paolo, Peter y Matt},\\
s+j&\le1
&&\text{Peter y Jorge son incompatibles},\\
s&\le m,\\
s&\le l
&&\text{Peter requiere a Matt y Linus},\\
p,s,m,l,j&\in\{0,1\}.
\end{aligned}
$$

### Por qué funciona y qué revisar

Una decisión de asistencia es binaria. La implicación “si asiste A, también debe asistir B” se escribe $x_A\le x_B$; una pareja incompatible se expresa $x_A+x_B\le1$. La condición que prohíbe la asistencia simultánea de tres personas se representa limitando la suma de sus variables a 2. Comprueba cada regla con un caso de prueba: si la persona condicionante vale 1, ¿las demás restricciones fuerzan o prohíben exactamente lo que dice el texto?

## 6. Transporte de petróleo

### Modelo

Sean $x_{ij}\ge0$ los litros enviados desde depósito $i\in\{A,B\}$ a bomba $j\in\{D,E,F\}$. Las distancias (km) son $d_{AD}=7$, $d_{AE}=6$, $d_{AF}=3$, $d_{BD}=3$, $d_{BE}=4$ y $d_{BF}=2$.

$$
\min\quad 0{,}5(7x_{AD}+6x_{AE}+3x_{AF}+3x_{BD}+4x_{BE}+2x_{BF})
$$

sujeto a:

$$
\begin{aligned}
x_{AD}+x_{AE}+x_{AF}&\le7\,000 &&\text{oferta de A},\\
x_{BD}+x_{BE}+x_{BF}&\le4\,000 &&\text{oferta de B},\\
x_{AD}+x_{BD}&=4\,500 &&\text{demanda de D},\\
x_{AE}+x_{BE}&=3\,000 &&\text{demanda de E},\\
x_{AF}+x_{BF}&=3\,500 &&\text{demanda de F},\\
x_{ij}&\ge0 &&i\in\{A,B\},\ j\in\{D,E,F\}.
\end{aligned}
$$

El factor 0,5 es el costo en dólares por litro-kilómetro. Como la demanda total coincide con la oferta total, ambas ofertas se utilizarán por completo en cualquier plan factible.

### Por qué funciona y qué revisar

Cada variable representa un flujo por una ruta concreta. Las restricciones de oferta limitan lo que sale de cada depósito y las igualdades de demanda aseguran que cada bomba reciba exactamente lo requerido. El costo de una ruta es la distancia multiplicada por el costo por litro-kilómetro. Verifica que la tabla se lea con el origen en la fila y el destino en la columna, y que no se confundan litros con kilómetros.
