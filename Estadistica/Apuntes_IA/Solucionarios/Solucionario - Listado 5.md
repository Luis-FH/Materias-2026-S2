# Solucionario — Listado 5: Modelos de probabilidades discretos

#certamen1_estadistica

**Fuente:** [[Listado 5 523250 E y P_II_2026.pdf]] (única página).

**Recursos directos:** [[Clase4_2026 (1).pdf]], [[Resumen_modelos_discretos.pdf]] y [[Ejercicio_modelos_discretos.pdf]].

**Clasificación:** Certamen 1, por su contenido de distribuciones discretas y modelos probabilísticos.

## 1. La novena persona es la cuarta compradora de Kino

Sea «éxito» que una persona compre Kino, con \(p=0{,}3\) y \(q=0{,}7\). Para que la novena persona sea la cuarta compradora, entre las primeras ocho debe haber exactamente tres compradores y la novena debe comprar.

\[
P=\binom{8}{3}(0{,}3)^3(0{,}7)^5(0{,}3)
 =\binom{8}{3}(0{,}3)^4(0{,}7)^5.
\]

\[
P=56(0{,}0081)(0{,}16807)=0{,}0762366.
\]

**Respuesta:** la probabilidad es aproximadamente **0,0762 (7,62 %)**. Es una probabilidad binomial negativa: se fija el número de éxitos y la posición del éxito final.

## 2. Selección de televisores sin reemplazo

Hay \(N=300\) televisores, de los cuales \(K=100\) son del proveedor A y 200 del B. Sea \(X\) el número de televisores A entre los cuatro elegidos. Como se extrae sin reemplazo,

\[
P(X=k)=\frac{\binom{100}{k}\binom{200}{4-k}}{\binom{300}{4}},\qquad k=0,1,2,3,4.
\]

El denominador es \(\binom{300}{4}=330\,791\,175\).

### i) Los cuatro son del proveedor A

\[
P(X=4)=\frac{\binom{100}{4}}{\binom{300}{4}}
=\frac{3\,921\,225}{330\,791\,175}
=0{,}0118541.
\]

**Respuesta:** \(0{,}01185\), aproximadamente **1,19 %**.

### ii) Dos o más son del proveedor A

\[
\begin{aligned}
P(X\ge2)
&=P(X=2)+P(X=3)+P(X=4)\\
&=\frac{\binom{100}{2}\binom{200}{2}
+\binom{100}{3}\binom{200}{1}
+\binom{100}{4}}{\binom{300}{4}}\\
&=0{,}2977861+0{,}0977656+0{,}0118541\\
&=0{,}4074057.
\end{aligned}
\]

**Respuesta:** aproximadamente **0,4074 (40,74 %)**.

### iii) A lo más uno es del proveedor B

Esto significa que al menos tres de los cuatro son A, es decir, \(X\ge3\):

\[
\begin{aligned}
P(X\ge3)
&=P(X=3)+P(X=4)\\
&=\frac{\binom{100}{3}\binom{200}{1}+\binom{100}{4}}{\binom{300}{4}}\\
&=0{,}0977656+0{,}0118541\\
&=0{,}1096197.
\end{aligned}
\]

**Respuesta:** aproximadamente **0,1096 (10,96 %)**.

## 3. Llegadas de automóviles

Se modelan las llegadas con una distribución de Poisson. La tasa es 9 automóviles cada media hora, equivalente a 18 por hora.

### i) A lo más dos vehículos en un cuarto de hora

En 15 minutos, la media es \(\lambda=9(15/30)=4{,}5\). Si \(N\sim\operatorname{Poisson}(4{,}5)\),

\[
\begin{aligned}
P(N\le2)
&=\sum_{k=0}^{2}e^{-4{,}5}\frac{4{,}5^k}{k!}\\
&=e^{-4{,}5}\left(1+4{,}5+\frac{4{,}5^2}{2}\right)\\
&=0{,}1735781.
\end{aligned}
\]

**Respuesta:** aproximadamente **0,1736 (17,36 %)**.

### ii) Exactamente tres de 13 horas tienen 15 llegadas

Para una hora, \(N\sim\operatorname{Poisson}(18)\). La probabilidad de exactamente 15 llegadas en una hora es

\[
p=P(N=15)=e^{-18}\frac{18^{15}}{15!}=0{,}0785755.
\]

Sea \(Y\) el número, entre los 13 intervalos horarios, que tienen exactamente 15 llegadas. Bajo el supuesto de intervalos independientes, \(Y\sim\operatorname{Binomial}(13,p)\). Por tanto,

\[
\begin{aligned}
P(Y=3)
&=\binom{13}{3}p^3(1-p)^{10}\\
&=\binom{13}{3}(0{,}0785755)^3(0{,}9214245)^{10}\\
&=0{,}0612104.
\end{aligned}
\]

**Respuesta:** aproximadamente **0,0612 (6,12 %)**.

## 4. Páginas con al menos tres errores

El promedio es \(3\) errores por cada 10 páginas, o \(\lambda=0{,}3\) errores por página. Se supone un modelo de Poisson independiente por página. Para una página,

\[
\begin{aligned}
q=P(N\ge3)
&=1-\left[P(N=0)+P(N=1)+P(N=2)\right]\\
&=1-e^{-0{,}3}\left(1+0{,}3+\frac{0{,}3^2}{2}\right)\\
&=0{,}00359949.
\end{aligned}
\]

Sea \(Y\) el número de páginas, de las 500, con al menos tres errores. Entonces \(Y\sim\operatorname{Binomial}(500,q)\). Se pide \(P(Y>1)\), por lo que conviene usar el complemento:

\[
\begin{aligned}
P(Y>1)
&=1-P(Y=0)-P(Y=1)\\
&=1-(1-q)^{500}-\binom{500}{1}q(1-q)^{499}\\
&=0{,}5375168.
\end{aligned}
\]

**Respuesta:** aproximadamente **0,5375 (53,75 %)**.

> **Supuesto del modelo:** el enunciado entrega un promedio, no una distribución explícita de errores ni independencia entre páginas. El resultado usa el modelo de Poisson homogéneo habitual para conteos de errores; sin ese supuesto, el promedio por sí solo no determina la probabilidad pedida.
