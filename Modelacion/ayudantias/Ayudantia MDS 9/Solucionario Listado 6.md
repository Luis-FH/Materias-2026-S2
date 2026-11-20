---
tags:
  - Certamen-2-MDS
---

# Solucionario — Listado 6: Repaso de Formulación de Modelos

El listado solicita formular modelos, no resolverlos numéricamente. Las expresiones siguientes detallan conjuntos, parámetros, variables, objetivo, restricciones y dominios. En los problemas que dependen de tablas o decisiones discretas, se indican las unidades y la interpretación necesarias para evitar errores de modelación.

## 1. Selección de proyectos

### Modelo

Sea $I=\{1,\ldots,N\}$ el conjunto de proyectos. Para cada proyecto $i$, $b_i$ es el beneficio si se realiza. El listado declara mutuamente excluyentes los proyectos 1 y 2, por lo que $P=\{(1,2)\}$.

Definimos $x_i=1$ si se elige el proyecto $i$, y $x_i=0$ en caso contrario.

$$
\max\quad \sum_{i\in I} b_i x_i
$$

sujeto a:

$$
\begin{aligned}
\sum_{i\in I}x_i&\le E
&&\text{límite de equipos de trabajo},\\
x_i+x_j&\le1
&&\forall (i,j)\in P,\\
x_i&\in\{0,1\}
&&\forall i\in I.
\end{aligned}
$$

### Por qué funciona y qué revisar

La variable binaria representa la decisión de ejecutar o no cada proyecto. El beneficio se obtiene solo si $x_i=1$. La primera restricción limita la cantidad total de proyectos seleccionados al número de equipos disponibles; cada par excluyente se limita a, como máximo, un proyecto. Revisa que $P$ contenga solamente los pares que el enunciado declara incompatibles.

## 2. Compañía de buses

### Datos

Cada viaje dura 6 horas. Los conductores deben descansar 4 horas entre los dos viajes de su jornada, que comprende un viaje A→B y uno B→A. Denotamos por $A_i$, $i=1,\ldots,5$, los viajes que parten de A y por $B_j$, $j=1,\ldots,5$, los viajes que parten de B. Las horas de salida en el horario son:

| Viaje | Salida | Viaje | Salida |
|---|---:|---|---:|
| A1 | 06:00 | B1 | 05:30 |
| A2 | 07:30 | B2 | 09:00 |
| A3 | 11:30 | B3 | 15:00 |
| A4 | 19:00 | B4 | 18:30 |
| A5 | 00:30 | B5 | 00:00 |

### Modelo de asignación de jornadas

Para cada par de salidas $A_i,B_j$, sea $c_{ij}$ el tiempo de inactividad del conductor entre sus dos viajes, excluidas las 4 horas de descanso obligatorio. Se consideran los horarios periódicos de 24 horas y ambos órdenes. Si $a_i,b_j\in[0,24)$ son las horas de salida en horas, el tiempo entre la llegada del primer viaje y la salida siguiente es:

$$
w_{ij}^{AB}=(b_j-a_i-6)\bmod 24,\qquad
w_{ij}^{BA}=(a_i-b_j-6)\bmod 24,
$$

donde el módulo representa el tiempo hasta la siguiente salida programada, incluyendo el siguiente día. Un orden es factible si su espera es al menos 4 horas. Definimos $F$ como los pares que tienen al menos un orden factible y:

$$
c_{ij}=\min\Big(
\{w_{ij}^{AB}-4:w_{ij}^{AB}\ge4\}
\cup
\{w_{ij}^{BA}-4:w_{ij}^{BA}\ge4\}
\Big),
$$

tomando el mínimo solo entre las esperas que sí cumplen el descanso. Así, $c_{ij}$ es el menor tiempo inactivo posible para ese par.

Definimos $x_{ij}=1$ si un conductor hace el viaje $A_i$ y el viaje $B_j$, y 0 de lo contrario.

$$
\min\quad \sum_{(i,j)\in F}c_{ij}x_{ij}
$$

sujeto a:

$$
\begin{aligned}
\sum_{j:(i,j)\in F}x_{ij}&=1 &&i=1,\ldots,5,\\
\sum_{i:(i,j)\in F}x_{ij}&=1 &&j=1,\ldots,5,\\
x_{ij}&\in\{0,1\} &&(i,j)\in F.
\end{aligned}
$$

Cada igualdad asegura que cada salida programada se cubra exactamente una vez. La cantidad de conductores es 5, dado que hay cinco salidas en cada sentido y cada jornada de conductor incluye una de cada dirección.

### Cómo calcular $c_{ij}$

Para un par factible, se evalúan los dos órdenes posibles: A→B seguido de B→A, o B→A seguido de A→B, incluyendo el siguiente día cuando corresponda. En cada orden, el tiempo entre la llegada del primer viaje y la salida del segundo debe ser al menos 4 horas; el exceso sobre esas 4 horas es tiempo inactivo. $c_{ij}$ es el menor exceso entre los órdenes factibles. Por ejemplo, el viaje B3 que sale a las 15:00 llega a A a las 21:00; combinado con A1 a las 06:00 del día siguiente, la espera es de 9 horas, de las cuales 4 son descanso y 5 inactividad.

### Por qué funciona y qué revisar

El problema es un emparejamiento entre salidas de sentidos opuestos. Las variables binarias escogen las parejas; las restricciones de cobertura impiden dejar viajes sin conductor o asignar una salida a dos conductores. El costo de cada pareja no es simplemente la diferencia entre horas de partida: hay que sumar las 6 horas de viaje, exigir las 4 horas de descanso y considerar el cambio de día. Antes de resolver, construye una tabla $c_{ij}$ y marca explícitamente los pares factibles.

### Segunda solución: calcular $C_{ij}$ con matrices

El mismo modelo puede presentarse calculando primero la matriz de costos. Este método organiza las 25 combinaciones y reduce errores al considerar el cambio de día.

Escribimos las salidas como horas desde la medianoche:

$$
\mathbf{a}=(6,\ 7{,}5,\ 11{,}5,\ 19,\ 0{,}5),\qquad
\mathbf{b}=(5{,}5,\ 9,\ 15,\ 18{,}5,\ 0).
$$

Construimos la matriz de diferencias de salida
$D_{ij}=(b_j-a_i)\bmod 24$, tomando cada entrada entre 0 y 24:

$$
D=
\begin{pmatrix}
23{,}5&3&9&12{,}5&18\\
22&1{,}5&7{,}5&11&16{,}5\\
18&21{,}5&3{,}5&7&12{,}5\\
10{,}5&14&20&23{,}5&5\\
5&8{,}5&14{,}5&18&23{,}5
\end{pmatrix}.
$$

Cada entrada de $D$ es el tiempo desde la salida $A_i$ hasta la siguiente salida $B_j$, con periodicidad de 24 horas. Como cada viaje dura 6 horas, las matrices de espera entre la llegada del primer viaje y la salida del segundo son:

$$
W^{AB}=(D-6)\bmod 24,\qquad
W^{BA}=(24-D-6)\bmod 24.
$$

Para obtener $C_{ij}$, se consideran las entradas de ambas matrices de espera que sean al menos 4 horas, se les resta el descanso obligatorio y se elige el menor excedente. El resultado es:

$$
C_{ij}=\min\Big(
\{W^{AB}_{ij}-4:W^{AB}_{ij}\ge4\}
\cup
\{W^{BA}_{ij}-4:W^{BA}_{ij}\ge4\}
\Big),
$$

$$
C=
\begin{pmatrix}
13{,}5&11&5&1{,}5&8\\
12&12{,}5&6{,}5&1&6{,}5\\
8&11{,}5&10{,}5&7&1{,}5\\
0{,}5&0&10&13{,}5&9\\
9&5{,}5&4{,}5&8&13{,}5
\end{pmatrix}
\quad\text{(horas de inactividad).}
$$

Por ejemplo, para $(A_1,B_3)$, $D_{13}=9$. Las esperas posibles son $(9-6)\bmod24=3$ horas en el orden A→B y $(24-9-6)\bmod24=9$ horas en el orden B→A. El primer orden no cumple las 4 horas de descanso; el segundo sí, y deja $9-4=5$ horas inactivas. Por eso $C_{13}=5$. En esta instancia las 25 parejas tienen al menos un orden factible, así que no hace falta excluir ninguna.

Sea $X=(x_{ij})$ la matriz binaria de asignación. El modelo queda:

$$
\min\quad \sum_{i=1}^{5}\sum_{j=1}^{5}C_{ij}x_{ij}
$$

sujeto a:

$$
\begin{aligned}
\sum_{j=1}^{5}x_{ij}&=1 &&i=1,\ldots,5,\\
\sum_{i=1}^{5}x_{ij}&=1 &&j=1,\ldots,5,\\
x_{ij}&\in\{0,1\} &&i,j=1,\ldots,5.
\end{aligned}
$$

Esta formulación es equivalente a la anterior: cambia la forma de calcular y presentar los coeficientes, no las decisiones ni las condiciones de cobertura. Para minimizar el costo de asignación también se puede resolver como un problema clásico de asignación; primero se debe construir correctamente $C$.

## 3. Centros de distribución

### Datos y variables

Los centros candidatos son $K=\{\text{Concepción},\text{Chillán},\text{Los Ángeles}\}$ y las provincias de destino son $J=\{\text{Diguillín},\text{Punilla},\text{Itata},\text{Arauco},\text{Biobío},\text{Concepción}\}$.

La demanda mensual en cajas es:

$$
(d_j)=(120,80,90,110,140,160).
$$

Sea $f_k$ el costo fijo de apertura en millones de pesos para el candidato $k$: $f=(80,90,70)$. Sea $q=80$ pesos por caja-kilómetro, y $r_{kj}$ la distancia en kilómetros de candidato $k$ a provincia $j$:

$$
\begin{array}{c|rrrrrr}
 & \text{Diguillín}&\text{Punilla}&\text{Itata}&\text{Arauco}&\text{Biobío}&\text{Concepción}\\\hline
\text{Concepción}&85&120&110&60&150&0\\
\text{Chillán}&0&35&55&190&130&110\\
\text{Los Ángeles}&130&165&155&150&0&120
\end{array}
$$

Sea $y_k=1$ si se abre el centro $k$, y 0 si no. Sea $x_{kj}$ la fracción de la demanda mensual de $j$ servida desde $k$. Si se requiere asignar cada provincia íntegramente a un centro, se usan variables binarias $x_{kj}$; si se permite dividir los despachos, basta $x_{kj}\ge0$. El modelo usa la versión divisible, que corresponde a una cantidad de cajas transportadas.

### (a) Costo total de instalación y despacho mensual

$$
\min\quad
10^6\sum_{k\in K} f_k y_k
+80\sum_{k\in K}\sum_{j\in J} d_j r_{kj}x_{kj}
$$

sujeto a:

$$
\begin{aligned}
\sum_{k\in K}x_{kj}&=1 &&j\in J
&&\text{se satisface toda la demanda mensual},\\
x_{kj}&\le y_k &&k\in K,\ j\in J
&&\text{solo se despacha desde centros abiertos},\\
\sum_{k\in K}y_k&=2
&&\text{se abren dos centros},\\
x_{kj}&\ge0 &&k\in K,\ j\in J,\\
y_k&\in\{0,1\} &&k\in K.
\end{aligned}
$$

El factor $10^6$ convierte los costos fijos —entregados en millones de pesos— a pesos, para que sean comparables con el costo de transporte.

### (b) Proyección de 10 años

Si las demandas y despachos mensuales se repiten durante 120 meses y la apertura se paga una sola vez, el objetivo pasa a ser:

$$
\min\quad
10^6\sum_{k\in K} f_k y_k
+120\cdot80\sum_{k\in K}\sum_{j\in J}d_j r_{kj}x_{kj}.
$$

Las restricciones de apertura y asignación no cambian. Se multiplica solo el costo mensual recurrente por 120; no se multiplica el costo fijo de construcción.

### (c) Cambio en el número de centros

Sí, cambiar la cantidad de centros puede cambiar las variables óptimas. Para planificar $p$ centros, se reemplaza $\sum_k y_k=2$ por:

$$
\sum_{k\in K}y_k=p.
$$

Luego se vuelve a resolver el modelo. El nuevo óptimo puede asignar provincias a centros distintos; no se puede afirmar qué variables cambian sin especificar $p$ y resolver la instancia.

### Por qué funciona y qué revisar

Las $y_k$ deciden la ubicación de los centros y las $x_{kj}$ distribuyen la demanda. Cada provincia recibe el 100% de sus cajas; las restricciones de enlace impiden enviar desde una ubicación cerrada. La unidad de transporte es cajas × kilómetros × pesos por caja-kilómetro. Mantén en unidades comparables los costos fijos y los costos de operación; en el horizonte de 10 años, solo la operación mensual se repite.

## 4. Desarrollo habitacional

### Modelo

Sean $T=\{C,D,K\}$ los tipos de unidad: casas, departamentos y condominios; y $R=\{B,E,L\}$ los tipos de precio: bajo, estándar y de lujo. Definimos $x_{tr}$ como el número de unidades del tipo $t$ y nivel $r$.

Las áreas $a_{tr}$ en m² y beneficios $p_{tr}$ en millones de pesos son:

$$
\begin{array}{c|rrr|rrr}
&\multicolumn{3}{c|}{a_{tr}\text{ (m²)}}&
\multicolumn{3}{c}{p_{tr}\text{ (millones \$)}}\\
&B&E&L&B&E&L\\\hline
C&180&220&300&5&12&25\\
D&74&160&223&4&10&18\\
K&\text{no permitido}&100&150&\text{no permitido}&9&16
\end{array}
$$

La meta de casas de bajo costo se representa por $\sum_t x_{tB}$, y el total de viviendas por $\sum_{t,r}x_{tr}$. Definimos el área construida total $A_T=\sum_{t,r}a_{tr}x_{tr}$, y las áreas por tipo $A_C=\sum_r a_{Cr}x_{Cr}$, $A_D=\sum_r a_{Dr}x_{Dr}$, $A_K=\sum_r a_{Kr}x_{Kr}$. El terreno disponible es de $100\,000$ m².

$$
\max\quad \sum_{t\in T}\sum_{r\in R}p_{tr}x_{tr}
$$

sujeto a:

$$
\begin{aligned}
\sum_{t\in T}\sum_{r\in R}a_{tr}x_{tr}&\le100\,000
&&\text{terreno disponible},\\
0.25A_T&\le A_C\le0.40A_T
&&\text{proporción del área para casas},\\
0.25A_T&\le A_D\le0.40A_T
&&\text{proporción del área para departamentos},\\
0.10A_T&\le A_K\le0.25A_T
&&\text{proporción del área para condominios},\\
\sum_{t\in T}x_{tB}&\ge0.25\sum_{t\in T}\sum_{r\in R}x_{tr}
&&\text{al menos 25\% de las unidades de bajo costo},\\
x_{KB}&=0
&&\text{no se ofrece condominio de bajo costo},\\
x_{tr}&\in\mathbb Z_{\ge0} &&t\in T,\ r\in R.
\end{aligned}
$$

Las proporciones se aplican al área total construida del proyecto, no al terreno disponible. La combinación de condominio de bajo costo no existe en la tabla, por lo que se fija en cero.

### Por qué funciona y qué revisar

La función objetivo suma beneficios por vivienda y nivel. El terreno se limita por su disponibilidad; las proporciones de área se expresan como porcentajes del área total construida, no como porcentajes del terreno disponible. El requisito del estado se refiere al número de viviendas de bajo costo, no a los metros cuadrados. Las viviendas son indivisibles, por lo que las variables son enteras. No se debe asignar área ni beneficio a la combinación de condominio de bajo costo si esa alternativa no existe en la tabla.

## 5. Central eléctrica de biomasas

### Modelo

Sean $I=\{1,\ldots,n\}$ las calderas y $J=\{1,\ldots,m\}$ las turbinas. Para la caldera $i$, $c_i,d_i$ son la producción mínima y máxima de vapor (toneladas), $f_i$ el costo fijo y $p_i$ el costo por tonelada. Para la turbina $j$, $t_j,u_j$ son el caudal mínimo y máximo de vapor, $g_j$ el costo fijo de uso, $l_j$ los kWh obtenidos por tonelada y $q_j$ el costo por kWh. Sea $D$ la demanda eléctrica.

Definimos $x_i$ como vapor producido por la caldera $i$, $y_i$ binaria que indica su uso, $z_j$ como vapor enviado a la turbina $j$, $v_j$ binaria que indica su uso, y $e_j$ como energía producida. Sean $r_3$ la cantidad de derechos de emisión requeridos y $\tau_3=0.5c_3$ el umbral que activa la compra, tal como aparece en el listado. $h_3$ es el costo unitario de esos derechos.

$$
\min\quad
\sum_{i\in I}(f_i y_i+p_i x_i)
+\sum_{j\in J}(g_j v_j+q_j e_j)+h_3r_3
$$

sujeto a:

$$
\begin{aligned}
c_i y_i&\le x_i\le d_i y_i &&i\in I
&&\text{producción mínima y máxima de caldera},\\
\sum_{j\in J}z_j&=\sum_{i\in I}x_i
&&\text{balance de vapor},\\
t_jv_j&\le z_j\le u_jv_j &&j\in J
&&\text{uso y límites de cada turbina},\\
e_j&=l_jz_j &&j\in J
&&\text{conversión a kWh},\\
\sum_{j\in J}e_j&\ge D
&&\text{demanda eléctrica},\\
r_3&\ge x_3-\tau_3,\quad r_3\ge0
&&\text{derechos para producción sobre el umbral},\\
\sum_{j\in J,\ j\ne3}z_j&\ge0.10z_3
&&\text{uso de las otras turbinas junto con la 3},\\
y_i&\in\{0,1\} &&i\in I,\\
v_j&\in\{0,1\} &&j\in J,\\
x_i,z_j,e_j&\ge0 &&i\in I,\ j\in J.
\end{aligned}
$$

En la condición de emisión, $r_3$ representa vapor sujeto a derechos por encima del umbral. La desigualdad de las turbinas interpreta el requisito como usar en las demás turbinas, en conjunto, al menos 10% del vapor de la turbina 3.

### Por qué funciona y qué revisar

Las variables $y_i$ y $v_j$ activan los costos fijos y los límites mínimo-máximo de calderas y turbinas. El balance asegura que todo el vapor producido se distribuya. La producción total debe cubrir la demanda; si se supera el umbral de la caldera 3, $r_3$ contabiliza el exceso sujeto a derechos. Revisa que el costo unitario de derechos y los demás costos estén en unidades compatibles.

## 6. Cadena de heladerías

### Modelo

Sea $T=\{1,2,3,4\}$ el conjunto de trimestres y $d_t$ el requerimiento de trabajadores del trimestre $t$. Los tipos de trabajador disponibles son:

- anuales: trabajan los cuatro trimestres;
- de verano: trabajan Dic–Ene–Feb (trimestre 1);
- de invierno: trabajan Jun–Jul–Ago (trimestre 3);
- de medio año: trabajan los trimestres 2 y 4.

Sean $x_A,x_V,x_I,x_M$ las cantidades contratadas de trabajadores anuales, de verano, de invierno y de medio año, respectivamente. Hasta $u_1$ trabajadores anuales pueden contratarse. Se paga por trimestre trabajado: $c_1$ a cada trabajador anual, $c_2$ a cada trabajador de verano, $c_3$ a cada trabajador de invierno y $c_4$ a cada trabajador de medio año. Además, los trabajadores anuales y de medio año reciben $c_5$ por trabajador durante el trimestre de verano. Las variables son enteras no negativas.

$$
\min\quad (4c_1+c_5)x_A+c_2x_V+c_3x_I+(2c_4+c_5)x_M
$$

sujeto a:

$$
\begin{aligned}
x_A+x_V&\ge d_1 &&\text{Dic–Ene–Feb},\\
x_A+x_M&\ge d_2 &&\text{Mar–Abr–May},\\
x_A+x_I&\ge d_3 &&\text{Jun–Jul–Ago},\\
x_A+x_M&\ge d_4 &&\text{Sep–Oct–Nov},\\
x_A&\le u_1 &&\text{máximo de trabajadores anuales},\\
x_A,x_V,x_I,x_M&\in\mathbb Z_{\ge0}.
\end{aligned}
$$

### Por qué funciona y qué revisar

Cada restricción suma solamente los trabajadores activos en ese trimestre. Los anuales cubren todos; los de verano aparecen solo en el primero; los de invierno, solo en el tercero; y los de medio año, en los trimestres segundo y cuarto. El objetivo incorpora el pago trimestral de cada tipo y el extra $c_5$ que reciben los anuales y los de medio año durante el trimestre de verano. Las cantidades de trabajadores son enteras.
