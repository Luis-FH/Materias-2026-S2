# Solucionario — Listado 4

#certamen1_estadistica

**Fuente:** [[Listado 4 523250 E y P_II_2026.pdf]]  
**Material relacionado:** [[Clase 3 - Variables aleatorias]], [[Clase 4 - Modelos probabilísticos]]

## 1. Extracción de tres monedas

Hay cinco monedas distinguibles por su posición física: dos de $1, dos de $5 y una de $10. Todas las \(\binom53=10\) selecciones son equiprobables. Las posibilidades por tipo son:

| Monedas extraídas | Número de selecciones | Total \(X\) |
|---|---:|---:|
| Dos de $1 y una de $5 | 2 | $7 |
| Una de $1 y dos de $5 | 2 | $11 |
| Dos de $1 y una de $10 | 1 | $12 |
| Una de $1, una de $5 y una de $10 | 4 | $16 |
| Dos de $5 y una de $10 | 1 | $20 |

### a) Distribución de probabilidad de \(X\)

| \(x\) (pesos) | 7 | 11 | 12 | 16 | 20 |
|---|---:|---:|---:|---:|---:|
| \(P(X=x)\) | \(2/10\) | \(2/10\) | \(1/10\) | \(4/10\) | \(1/10\) |

Las probabilidades suman 1.

### b) \(P(X\le10\mid X\le15)\)

Entre los resultados \(X\le15\), los totales posibles son 7, 11 y 12, con probabilidad conjunta \(2/10+2/10+1/10=5/10\). El evento \(X\le10\) dentro de ese conjunto solo incluye 7:

\[
P(X\le10\mid X\le15)=\frac{2/10}{5/10}=\boxed{0,4}.
\]

### c) Extraer las dos monedas de $1, dado \(X\le11\)

El evento \(X\le11\) incluye selecciones con total 7 (dos monedas de $1 y una de $5) o 11 (una de $1 y dos de $5): \(2+2=4\) selecciones. Solo las 2 selecciones de total 7 contienen las dos monedas de $1:

\[
P(\text{dos monedas de } \$1\mid X\le11)=\frac24=\boxed{0,5}.
\]

## 2. Demanda e ingreso del kiosco

La distribución es \(P(X=x)=(7-x)/21\), para \(x=1,\ldots,6\); equivale a las probabilidades \(6/21,5/21,\ldots,1/21\).

\[
E(X)=\frac{1(6)+2(5)+3(4)+4(3)+5(2)+6(1)}{21}
=\frac{56}{21}=\frac83.
\]

\[
E(X^2)=\frac{1^2(6)+2^2(5)+3^2(4)+4^2(3)+5^2(2)+6^2(1)}{21}
=\frac{196}{21}=\frac{28}{3}.
\]

\[
V(X)=E(X^2)-[E(X)]^2=\frac{28}{3}-\frac{64}{9}=\frac{20}{9}.
\]

Para \(Y=200X+300000\):

\[
E(Y)=200E(X)+300000
=\frac{1600}{3}+300000
\approx\boxed{300\,533,33}\text{ u.m.}
\]

\[
V(Y)=200^2V(X)=40\,000\left(\frac{20}{9}\right)
=\boxed{\frac{800\,000}{9}\approx88\,888,89\text{ (u.m.)}^2}.
\]

La desviación estándar del ingreso es \(200\sqrt{20}/3\approx298,14\) u.m. El término fijo 300.000 aumenta el ingreso esperado, pero no cambia su varianza.

## 3. Capacidad de congeladores y precio

### a) \(E(X)\), \(E(X^2)\) y \(V(X)\)

\[
E(X)=13,5(0,2)+15,9(0,5)+19,1(0,3)
=2,70+7,95+5,73=\boxed{16,38\text{ pies}^3}.
\]

\[
E(X^2)=13,5^2(0,2)+15,9^2(0,5)+19,1^2(0,3)
=36,45+126,405+109,443=272,298.
\]

\[
V(X)=272,298-16,38^2
=272,298-268,3044=\boxed{3,9936\text{ (pies}^3)^2}.
\]

### b) Precio esperado

Para el precio \(P=25X-8,5\):

\[
E(P)=25E(X)-8,5=25(16,38)-8,5=\boxed{401\text{ unidades monetarias}}.
\]

### c) Varianza del precio

\[
V(P)=25^2V(X)=625(3,9936)
=\boxed{2496\text{ unidades monetarias}^2}.
\]

### d) Capacidad real esperada

Con \(h(X)=X-0,01X^2\), por linealidad de la esperanza:

\[
E[h(X)]=E(X)-0,01E(X^2)
=16,38-0,01(272,298)
=\boxed{13,65702\text{ pies}^3}.
\]

## 4. Tres lanzamientos de una moneda

Suponiendo una moneda equilibrada e independiente en cada lanzamiento, \(X\sim\operatorname{Binomial}(3,1/2)\).

### a) Distribución de probabilidad

| Caras \(x\) | 0 | 1 | 2 | 3 |
|---|---:|---:|---:|---:|
| \(P(X=x)=\binom3x/2^3\) | \(1/8\) | \(3/8\) | \(3/8\) | \(1/8\) |

### b) Función de distribución y representación

La función acumulada \(F(x)=P(X\le x)\) es:

\[
F(x)=
\begin{cases}
0,&x<0,\\
1/8,&0\le x<1,\\
4/8=1/2,&1\le x<2,\\
7/8,&2\le x<3,\\
1,&x\ge3.
\end{cases}
\]

Es una función escalonada, continua por la derecha; sus saltos están en \(0,1,2,3\), con alturas \(1/8,3/8,3/8,1/8\).

```text
F(x)
1       ───────────────────────────●──
7/8                   ─────────●──
1/2           ───────●
1/8   ───────●
0  ──●───────────────────────────────── x
      0       1       2        3
```

### c) Esperanza, varianza y desviación estándar

\[
E(X)=np=3(1/2)=\boxed{1,5\text{ caras}},
\quad V(X)=np(1-p)=3(1/2)(1/2)=\boxed{0,75\text{ caras}^2},
\]
\[
\sigma_X=\sqrt{0,75}=\frac{\sqrt3}{2}\approx\boxed{0,866\text{ caras}}.
\]

### d) A lo más dos caras

\[
P(X\le2)=1-P(X=3)=1-\frac18=\boxed{\frac78}.
\]

### e) Al menos dos caras

\[
P(X\ge2)=P(X=2)+P(X=3)=\frac38+\frac18=\boxed{\frac12}.
\]

## 5. Esperanza y varianza desde una función de distribución

La función transcrita en el PDF indica:

\[
F(x)=
\begin{cases}
0,&x<2,\\
0,2,&2\le x<4,\\
0,55,&4\le x<5,\\
0,85,&6\le x<8,\\
1,&x\ge8.
\end{cases}
\]

**Limitación del enunciado:** no se especifica \(F(x)\) para \(5\le x<6\). Por ello no queda determinada la distribución en ese tramo ni, en general, \(E(X)\) y \(V(X)\). No se puede afirmar una respuesta única a partir de la función tal como está impresa.

Si se supone que falta el tramo \(0,55\) para \(5\le x<6\), de modo que la función sea escalonada constante desde 4 hasta 6, las masas serían:

| Valor | Probabilidad |
|---:|---:|
| 2 | \(0,20\) |
| 4 | \(0,55-0,20=0,35\) |
| 6 | \(0,85-0,55=0,30\) |
| 8 | \(1-0,85=0,15\) |

Bajo **esa suposición adicional**:

\[
E(X)=2(0,20)+4(0,35)+6(0,30)+8(0,15)=4,8,
\]
\[
E(X^2)=2^2(0,20)+4^2(0,35)+6^2(0,30)+8^2(0,15)=26,8,
\]
\[
V(X)=26,8-4,8^2=\boxed{3,76}.
\]

Estos dos resultados son condicionales a la reparación indicada; el PDF no permite verificarlos como solución única.

## 6. Distancia del dardo al centro de la diana

### a) Constante \(k\) y densidad

La integral de una densidad debe ser 1:

\[
\int_0^{10}k\,dx=10k=1\quad\Longrightarrow\quad k=\frac1{10}=0,1.
\]

\[
f(x)=
\begin{cases}
0,1,&0<x<10,\\
0,&\text{en otro caso}.
\end{cases}
\]

Gráficamente es un rectángulo de altura \(0,1\) desde 0 hasta 10 cm y cero fuera de ese intervalo.

```text
f(x)
0,1       ┌──────────────────┐
          │                  │
0 ────────┘                  └──────── x
          0                 10
```

### b) Función de distribución

\[
F(x)=
\begin{cases}
0,&x\le0,\\
x/10,&0<x<10,\\
1,&x\ge10.
\end{cases}
\]

La gráfica sube linealmente desde \((0,0)\) hasta \((10,1)\) y permanece en 0 antes de 0 y en 1 después de 10.

```text
F(x)
1                            ─────────
                         /
                     /
                 /
0 ────────────/─────────────────────── x
              0                    10
```

### c) Esperanza y varianza

Para \(X\sim U(0,10)\):

\[
E(X)=\frac{0+10}{2}=\boxed{5\text{ cm}},\qquad
V(X)=\frac{(10-0)^2}{12}=\boxed{\frac{25}{3}\text{ cm}^2}.
\]

### d) \(P(X\le1)\)

\[
P(X\le1)=F(1)=\boxed{0,1}.
\]

### e) Probabilidad de acertar en la diana

Si “acertar” significa que la distancia al centro es exactamente cero, \(P(X=0)=0\), porque \(X\) es continua. Si la diana tiene un radio positivo y acertar significa caer dentro de ese radio, el enunciado no entrega el radio necesario para calcular esa probabilidad.

## 7. Densidad exponencial

\[
f(x)=
\begin{cases}
ke^{-kx},&x>0,\\
0,&\text{en otro caso},
\end{cases}\qquad k>0.
\]

### a) Valores posibles de \(k\)

\[
\int_0^\infty ke^{-kx}\,dx=1
\]
si y solo si \(k>0\). Así, \(k\) puede ser cualquier valor positivo, no cero ni un valor negativo.

### b) Densidad y distribución para \(k=0,1\)

El PDF usa coma decimal: \(k=0,1=0.1\). Entonces:

\[
f(x)=0,1e^{-0,1x}\ (x>0),\qquad
F(x)=
\begin{cases}
0,&x\le0,\\
1-e^{-0,1x},&x>0.
\end{cases}
\]

La densidad parte en \(0,1\) para \(x=0\) y decrece hacia 0. La función acumulada parte en 0 y crece hacia 1.

| \(x\) | 0 | 10 | 20 | 50 |
|---:|---:|---:|---:|---:|
| \(f(x)\) | 0,1000 | 0,0368 | 0,0135 | 0,0007 |
| \(F(x)\) | 0 | 0,6321 | 0,8647 | 0,9933 |

```text
f(x)                         F(x)
0,1 ┐                        1 ───────────────
    │\                            _________/
    │ \                       ___/
    │  \                  ___/
0 ──┴───\──────── x       0 ───────────────── x
    0                         0
```

### c) \(P(X>10)\)

\[
P(X>10)=e^{-0,1(10)}=e^{-1}\approx\boxed{0,3679}.
\]

### d) \(P(50<X\le100)\)

Como la distribución es continua:

\[
P(50<X\le100)=F(100)-F(50)
=e^{-5}-e^{-10}\approx\boxed{0,006693}.
\]

## 8. Densidad cuadrática en \((0,2)\)

\[
f(x)=ax^2+b,\quad 0<x<2.
\]

La normalización exige:

\[
\int_0^2(ax^2+b)\,dx=\frac{8a}{3}+2b=1.
\]

La probabilidad indicada produce una segunda ecuación:

\[
\int_{1/2}^{1}(ax^2+b)\,dx
=a\left[\frac{x^3}{3}\right]_{1/2}^{1}+b\left[x\right]_{1/2}^{1}
=\frac{7a}{24}+\frac b2=\frac16,
\]

ya que \(0,1\overline6=1/6\). Multiplicando las ecuaciones por 12 y 48, respectivamente:

\[
32a+24b=12,\qquad 14a+24b=8.
\]

Al restar, \(18a=4\), por lo que:

\[
\boxed{a=\frac29},\qquad
\frac{8}{3}\frac29+2b=1
\ \Longrightarrow\ 
\boxed{b=\frac{11}{54}}.
\]

Ambos coeficientes son positivos, de modo que \(f(x)\ge0\) en el soporte.

## 9. Precipitación y cortes de agua

Para \(0<x\le30\), \(f(x)=Kxe^{-0,25x}\). Fuera de ese intervalo, la densidad es cero.

### a) Constante y densidad normalizada

\[
1=K\int_0^{30}xe^{-x/4}\,dx
=K\left(16-136e^{-7,5}\right).
\]

\[
K=\frac{1}{16-136e^{-7,5}}\approx\boxed{0,0627952}.
\]

Por tanto:

\[
f(x)=
\begin{cases}
0,0627952\,x e^{-0,25x},&0<x\le30,\\
0,&\text{en otro caso}.
\end{cases}
\]

### b) Probabilidad de corte de agua

La probabilidad de precipitación en cada rango es:

\[
p_1=P(0<X<10)=K(16-56e^{-2,5})\approx0,7160689,
\]
\[
p_2=P(10\le X\le20)=K(56e^{-2,5}-96e^{-5})\approx0,2480359,
\]
\[
p_3=P(20<X\le30)=K(96e^{-5}-136e^{-7,5})\approx0,0358952.
\]

Las tres probabilidades suman 1. Usando las probabilidades condicionales de corte que entrega el enunciado:

\[
P(C)=0,15p_1+0,25p_2+0,55p_3
\approx0,1074103+0,0620090+0,0197424
=\boxed{0,18916}.
\]

La probabilidad de corte es aproximadamente 18,92 %.

### c) Hasta 10 ml, dado que hubo corte

Por Bayes, y como \(X\) es continua, \(P(X\le10,C)=P(C\mid X<10)P(X<10)=0,15p_1\):

\[
P(X\le10\mid C)
=\frac{0,15p_1}{P(C)}
=\frac{0,15(0,7160689)}{0,1891617}
\approx\boxed{0,56782}.
\]

La probabilidad pedida es aproximadamente 56,78 %.

## 10. Desigualdades de Markov y Chebyshev

### a) Desigualdad de Markov

Sea \(X\ge0\) y \(a>0\). Para cada resultado:

\[
X\ge a\,\mathbf 1_{\{X\ge a\}},
\]

donde \(\mathbf 1_{\{X\ge a\}}\) vale 1 si \(X\ge a\), y 0 en otro caso. Tomando esperanza en ambos lados:

\[
E(X)\ge aE[\mathbf 1_{\{X\ge a\}}]
=aP(X\ge a).
\]

Al dividir por \(a>0\):

\[
\boxed{P(X\ge a)\le\frac{E(X)}{a}}.
\]

### b) Desigualdad de Chebyshev

Aplicamos Markov a la variable no negativa \(Y=(X-\mu)^2\) y al umbral \(a^2\), con \(a>0\):

\[
P(|X-\mu|\ge a)
=P((X-\mu)^2\ge a^2)
\le\frac{E[(X-\mu)^2]}{a^2}
=\boxed{\frac{\sigma^2}{a^2}}.
\]

El enunciado escribe la letra \(x\) tanto como variable aleatoria como desviación respecto de \(\mu\); aquí se interpreta con \(X\) para la variable y \(a>0\) para el umbral.
