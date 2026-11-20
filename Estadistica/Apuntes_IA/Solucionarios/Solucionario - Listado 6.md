# Solucionario — Listado 6: Modelos continuos

#certamen1_estadistica

**Fuente:** [[Listado 6 523250 E y P_II_2026.pdf]] (dos páginas).

**Recursos directos:** [[Clase4_2026 (1).pdf]], [[resumen_variable_aleatoria.pdf]] y [[Tablas Estadísticas.pdf]].

**Clasificación:** Certamen 1, por su contenido de distribuciones normal, uniforme y exponencial dentro de modelos probabilísticos.

## 1. Especificaciones de tornillos

### a) Cumplir simultáneamente longitud y diámetro

Sea \(L\sim N(8{,}55;\,0{,}05^2)\) la longitud en cm y \(D\sim N(1{,}58;\,0{,}01^2)\) el diámetro en cm. La probabilidad de cumplir las especificaciones de longitud es

\[
\begin{aligned}
P(8{,}45\le L\le8{,}65)
&=P\left(-2\le\frac{L-8{,}55}{0{,}05}\le2\right)\\
&=\Phi(2)-\Phi(-2)=0{,}9544997.
\end{aligned}
\]

Para el diámetro,

\[
\begin{aligned}
P(1{,}55\le D\le1{,}60)
&=P\left(-3\le\frac{D-1{,}58}{0{,}01}\le2\right)\\
&=\Phi(2)-\Phi(-3)=0{,}9759000.
\end{aligned}
\]

Por la independencia indicada,

\[
P(\text{ambas especificaciones})
=0{,}9544997(0{,}9759000)=0{,}9314963.
\]

**Respuesta:** **0,9315 (93,15 %)**.

### b) A lo más dos de seis cumplen la longitud

Para cada tornillo, la probabilidad de cumplir la longitud es \(p=0{,}9544997\). Suponiendo tornillos independientes, si \(X\) cuenta los que cumplen la longitud, \(X\sim\operatorname{Binomial}(6,p)\):

\[
\begin{aligned}
P(X\le2)
&=\sum_{k=0}^{2}\binom{6}{k}p^k(1-p)^{6-k}\\
&=0{,}00005970.
\end{aligned}
\]

**Respuesta:** aproximadamente \(5{,}97\times10^{-5}\), es decir, **0,00597 %**. La probabilidad es pequeña porque la longitud especificada cubre el 95,45 % de la distribución de cada tornillo.

### c) Número esperado hasta encontrar un diámetro fuera de especificación

La probabilidad de que un tornillo no cumpla el diámetro es

\[
q=1-0{,}9759000=0{,}0241000.
\]

El número de tornillos seleccionados hasta el primer incumplidor tiene distribución geométrica (contando también al que incumple), con esperanza \(1/q\):

\[
E(T)=\frac{1}{q}=\frac{1}{0{,}0241000}=41{,}49.
\]

**Respuesta:** se espera seleccionar **aproximadamente 41,5 tornillos** para encontrar el primero que no cumple el diámetro (unos 42 en promedio).

## 2. Duración de un láser semiconductor

Sea \(T\sim N(7000;\,600^2)\), en horas.

### a) Fallar antes de 5.000 horas

\[
z=\frac{5000-7000}{600}=-3{,}3333,\qquad
P(T<5000)=\Phi(-3{,}3333)=0{,}0004291.
\]

**Respuesta:** aproximadamente **0,000429 (0,0429 %)**.

### b) Percentil 95 de la duración

El valor que no excede el 95 % de las duraciones es el percentil 95:

\[
t_{0{,}95}=\mu+z_{0{,}95}\sigma
=7000+(1{,}644854)(600)=7986{,}91\text{ horas}.
\]

**Respuesta:** aproximadamente **7.987 horas**.

### c) Tres láseres siguen funcionando después de 7.000 horas

Por simetría de la normal, \(P(T>7000)=0{,}5\). Suponiendo independencia entre los tres,

\[
P(\text{los tres sobreviven})=(0{,}5)^3=0{,}125.
\]

**Respuesta:** **0,125 (12,5 %)**.

## 3. Concentración uniforme de contaminante

Sea \(X\sim U(0,20)\), en partes por millón (ppm).

### a) Concentración tóxica

El nivel tóxico corresponde a \(X\ge8\). Para una uniforme, la probabilidad es la longitud del subintervalo dividida por la longitud total:

\[
P(X\ge8)=\frac{20-8}{20-0}=\frac{12}{20}=0{,}6.
\]

**Respuesta:** **0,60 (60 %)**.

### b) Media y varianza

Para \(U(a,b)\),

\[
E(X)=\frac{a+b}{2}=\frac{0+20}{2}=10\text{ ppm},
\qquad
\operatorname{Var}(X)=\frac{(b-a)^2}{12}
=\frac{20^2}{12}=33{,}3333\text{ ppm}^2.
\]

**Respuesta:** media **10 ppm**; varianza **33,33 ppm²**.

### c) Concentración exactamente igual a 10

Una variable continua tiene probabilidad cero en cualquier punto individual:

\[
P(X=10)=0.
\]

**Respuesta:** **0**.

## 4. Tiempo exponencial de reparación

La media es 22 minutos, por lo que la tasa es \(\lambda=1/22\) por minuto y

\[
P(T>t)=e^{-t/22},\qquad t\ge0.
\]

### a) Reparación menor que 10 minutos

\[
P(T<10)=1-P(T\ge10)=1-e^{-10/22}=0{,}3652636.
\]

**Respuesta:** aproximadamente **0,3653 (36,53 %)**.

### b) Que la reparación cueste 4.000 pesetas

Al cobrarse 2.000 pesetas por cada media hora o fracción, un costo de 4.000 corresponde a \(30<T\le60\) minutos (los extremos no afectan la probabilidad continua):

\[
\begin{aligned}
P(30<T\le60)
&=P(T>30)-P(T>60)\\
&=e^{-30/22}-e^{-60/22}\\
&=0{,}1903318.
\end{aligned}
\]

**Respuesta:** aproximadamente **0,1903 (19,03 %)**.

### c) Tiempo de programación con 10 % de probabilidad de excederlo

Se busca \(t\) tal que \(P(T>t)=0{,}1\):

\[
e^{-t/22}=0{,}1
\quad\Longrightarrow\quad
t=-22\ln(0{,}1)=50{,}6569\text{ minutos}.
\]

**Respuesta:** asignar aproximadamente **50,66 minutos** por reparación.
