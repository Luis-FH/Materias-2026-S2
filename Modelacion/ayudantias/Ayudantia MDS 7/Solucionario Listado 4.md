---
tags:
  - Certamen-2-MDS
---

# Solucionario — Listado 4: Modelos de Programación Lineal

El listado solicita formular los modelos, no calcular sus soluciones óptimas. A continuación se explicita la respuesta de modelación para cada ejercicio, seguida de una explicación del método y de los aspectos que conviene revisar en un certamen. Las variables que cuentan objetos o personas se declaran enteras para representar decisiones indivisibles; si el curso pide la relajación lineal, se reemplazan esos dominios por variables reales no negativas.

## 1. Carpintería

### Modelo

Sean:

- $s$: sillas que se producirán mañana.
- $m$: mesas que se producirán mañana.

Maximizar el beneficio:

$$
\max\quad 4s+8{,}5m
$$

sujeto a:

$$
\begin{aligned}
4s+9{,}5m &\le 38 &&\text{madera (m²)},\\
s+m &\le 7{,}5 &&\text{horas-persona},\\
s,m &\in \mathbb{Z}_{\ge 0}.
\end{aligned}
$$

### Por qué funciona y qué revisar

Cada silla y mesa aporta su beneficio correspondiente, por eso esos valores van en la función objetivo. La madera y el trabajo son recursos disponibles, así que sus consumos no pueden superar la disponibilidad. Revisa especialmente que cada coeficiente corresponda al consumo **por unidad** y que ambos lados de cada restricción usen la misma unidad.

## 2. The Really Big Shoe

### Modelo

Sean:

- $f$: equipos de fútbol patrocinados.
- $b$: equipos de básquetbol patrocinados.

Cada equipo de fútbol requiere 120 pares y cada equipo de básquetbol 32 pares. Se desea maximizar la cantidad de equipos:

$$
\max\quad f+b
$$

sujeto a:

$$
\begin{aligned}
300\,000f+1\,000\,000b &\le 30\,000\,000
&&\text{presupuesto de patrocinio},\\
120f+3(32b) &\le 4\,000
&&\text{flubber (cc)},\\
f,b &\in \mathbb{Z}_{\ge 0}.
\end{aligned}
$$

### Por qué funciona y qué revisar

La decisión es cuántos equipos de cada deporte patrocinar, no cuántos pares fabricar directamente. Por eso cada restricción calcula el recurso consumido **por equipo**: el presupuesto indicado para ese deporte y los pares requeridos por equipo multiplicados por el flubber de cada par. En la segunda restricción, comprueba el factor $32\cdot3$ para básquetbol y $120\cdot1$ para fútbol. Los equipos deben ser cantidades enteras.

## 3. Compañía de automotores

### Modelo

Sean:

- $c$: camiones fabricados por día.
- $a$: automóviles fabricados por día.

La utilidad diaria a maximizar es:

$$
\max\quad 300c+200a
$$

sujeto a las capacidades de pintura y ensamble:

$$
\begin{aligned}
\frac{c}{40}+\frac{a}{60} &\le 1
&&\text{pintura},\\
\frac{c}{50}+\frac{a}{50} &\le 1
&&\text{ensamble},\\
c,a &\in \mathbb{Z}_{\ge 0}.
\end{aligned}
$$

Para la parte (b), agregar:

$$
c\ge 30,\qquad a\ge 20.
$$

### Por qué funciona y qué revisar

Las capacidades se describen mediante la producción máxima de cada tipo si el taller se dedicara exclusivamente a ese tipo. La fracción $c/40$, por ejemplo, es la proporción de la capacidad de pintura consumida por los camiones. La suma de fracciones no puede superar 1. En ensamble, ambos máximos son 50, lo que también puede escribirse $c+a\le 50$. En la parte (b), “al menos” exige restricciones $\ge$, no $\le$.

## 4. Café Baqué

### Modelo

Sean:

- $l$: unidades de Latte especial preparadas y vendidas al día.
- $c$: unidades de Cappuccino de la casa preparadas y vendidas al día.

$$
\max\quad 1\,200l+900c
$$

sujeto a:

$$
\begin{aligned}
11l+7c &\le 200 &&\text{leche 1 (oz)},\\
9l+10c &\le 230 &&\text{leche 2 (oz)},\\
l &\le 45 &&\text{demanda de Latte},\\
c &\le 130 &&\text{demanda de Cappuccino},\\
l,c &\ge 0.
\end{aligned}
$$

Si las unidades representan bebidas indivisibles, se puede añadir $l,c\in\mathbb Z$.

### Por qué funciona y qué revisar

Cada tipo de café consume una cantidad distinta de cada leche; por eso hay una restricción por insumo. La demanda máxima limita las ventas, aunque queden ingredientes disponibles. No confundas esos topes con requisitos mínimos. Comprueba que las utilidades estén asociadas al tipo correcto y que los consumos de la tabla estén en onzas.

## 5. Asignación de mantenimiento

### Modelo

Sean $x_{ij}$ binarias, con $x_{ij}=1$ si el equipo $i$ se asigna a la máquina $j$, y 0 en caso contrario. Hay tres equipos y tres máquinas. Los costos son:

$$
C=
\begin{pmatrix}
10&9&5\\
9&8&3\\
6&4&7
\end{pmatrix},
$$

donde filas son equipos 1–3 y columnas máquinas 1–3.

$$
\min\quad \sum_{i=1}^{3}\sum_{j=1}^{3} C_{ij}x_{ij}
$$

sujeto a:

$$
\begin{aligned}
\sum_{i=1}^{3}x_{ij}&=1 &&j=1,2,3
&&\text{cada máquina recibe un equipo},\\
\sum_{j=1}^{3}x_{ij}&=1 &&i=1,2,3
&&\text{cada equipo se asigna una vez},\\
x_{ij}&\in\{0,1\} &&i,j=1,2,3.
\end{aligned}
$$

### Por qué funciona y qué revisar

Una matriz binaria representa las parejas posibles equipo–máquina. Las sumas por máquina garantizan cobertura; las sumas por equipo impiden asignar un mismo equipo a más de una máquina. Como se busca el costo total mínimo, se minimiza la suma de costos de las parejas seleccionadas. Revisa con cuidado el orden de filas y columnas al copiar la matriz.
