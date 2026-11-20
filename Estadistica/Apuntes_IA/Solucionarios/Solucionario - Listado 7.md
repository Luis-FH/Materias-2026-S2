---
seguimiento_certamen2: true
bloque_certamen2: "Intervalos"
progreso_certamen2: false
---

# Solucionario — Listado 7: Intervalos de confianza

#certamen2_estadistica

**Fuente:** [[Ayudantia_Intervalos_de_Confianza.pdf]].

**Recursos directos:** [[Clase5_2026.pdf]], [[Resumen_intervalos_de_confianza.pdf]] y [[Tablas Estadísticas.pdf]].

**Nota de identificación:** el encabezado interno del PDF dice «Listado 6»; se registra aquí como Listado 7 de acuerdo con la identificación entregada para esta ayudantía.

## 1. Duración de cuentas de crédito

La población de duraciones es normal y se conoce \(\sigma=1500\) horas.

### a) Intervalo del 95 % para la media

Con \(n=100\), \(\bar x=9900\) y \(z_{0{,}975}=1{,}96\), el error estándar es

\[
\frac{\sigma}{\sqrt n}=\frac{1500}{\sqrt{100}}=150\text{ horas}.
\]

El margen de error es \(1{,}96(150)=294\) horas. Por tanto,

\[
\bar x\pm z_{0{,}975}\frac{\sigma}{\sqrt n}
=9900\pm294
=(9606,\ 10194)\text{ horas}.
\]

**Respuesta:** el intervalo de confianza del 95 % para la duración media es **(9.606; 10.194) horas**.

### b) Tamaño para un error máximo de 772,5 horas

Con confianza del 99 %, \(z_{0{,}995}=2{,}575829\). El margen requerido cumple

\[
E=z_{0{,}995}\frac{\sigma}{\sqrt n}
\quad\Longrightarrow\quad
n=\left(\frac{z_{0{,}995}\sigma}{E}\right)^2
=\left(\frac{2{,}575829(1500)}{772{,}5}\right)^2
\approx25{,}016.
\]

El tamaño debe ser entero y se redondea **hacia arriba** para que el error no exceda el máximo solicitado: **\(n=26\) clientes**. Con el cuantil de tabla redondeado a \(2{,}575\), se obtiene \(n=25\) exactamente; sin embargo, usando el cuantil más preciso, \(n=25\) da un margen de aproximadamente 772,75 horas, ligeramente mayor que 772,5.

## 2. Puntaje promedio de establecimientos

Se conoce \(n=42\), \(\bar x=107{,}6\) puntos y \(\sigma=1{,}3\) puntos. Para un intervalo del 95 %, el error estándar y el margen son

\[
SE=\frac{1{,}3}{\sqrt{42}}=0{,}2006,\qquad
E=1{,}96(0{,}2006)=0{,}3932.
\]

Así,

\[
\mu\in(107{,}6-0{,}3932,\ 107{,}6+0{,}3932)
=(107{,}2068,\ 107{,}9932)\text{ puntos}.
\]

**Conclusión:** no se puede afirmar que la media sea 110 puntos. El valor 110 queda fuera del intervalo. Al nivel asociado al intervalo, los datos son incompatibles con \(\mu=110\) bajo el modelo; esto no identifica por sí solo cuál es el valor verdadero de la media.

Como contraste bilateral equivalente, \(H_0:\mu=110\) frente a \(H_1:\mu\ne110\), el estadístico es
\[
z=\frac{107{,}6-110}{1{,}3/\sqrt{42}}=-11{,}96.
\]
Como \(|z|>1{,}96\), se rechaza \(H_0\) al 5 %.

## 3. Precios en ocho comercios

Datos: \(132,125,130,139,126,138,124,140\). Se supone una muestra aleatoria independiente de una población normal, especialmente necesario para el intervalo exacto de varianza con \(n=8\).

### a) Intervalo del 95 % para la varianza poblacional

La media muestral es

\[
\bar x=\frac{1054}{8}=131{,}75.
\]

La suma de cuadrados respecto de la media es

\[
\sum_{i=1}^{8}(x_i-\bar x)^2=301{,}5,
\qquad
s^2=\frac{301{,}5}{8-1}=43{,}0714.
\]

Con \(7\) grados de libertad, \(\chi^2_{0{,}025;7}=1{,}6899\) y \(\chi^2_{0{,}975;7}=16{,}0128\). El intervalo para \(\sigma^2\) es

\[
\left(
\frac{(n-1)s^2}{\chi^2_{0{,}975;7}},
\frac{(n-1)s^2}{\chi^2_{0{,}025;7}}
\right)
=\left(
\frac{301{,}5}{16{,}0128},
\frac{301{,}5}{1{,}6899}
\right)
\approx(18{,}83,\ 178{,}42).
\]

**Respuesta:** IC del 95 % para la varianza: **(18,83; 178,42) unidades de precio al cuadrado**. El enunciado no especifica la moneda o unidad de los precios.

### b) Proporción de precios menores o iguales a 130

Hay \(4\) precios que cumplen \(x_i\le130\) (125, 130, 126 y 124), de modo que

\[
\hat p=\frac{4}{8}=0{,}5.
\]

Usando el intervalo normal aproximado de Wald que se enseña para proporciones,

\[
\hat p\pm z_{0{,}975}\sqrt{\frac{\hat p(1-\hat p)}{n}}
=0{,}5\pm1{,}96\sqrt{\frac{0{,}5(0{,}5)}8}
=0{,}5\pm0{,}3465.
\]

El intervalo aproximado es **(0,1535; 0,8465)**, es decir, de **15,35 % a 84,65 %**.

**Limitación:** hay solo 4 observaciones en cada categoría; la aproximación normal de Wald es débil para este tamaño y el intervalo debe leerse con cautela. Como alternativa para una muestra pequeña, el intervalo binomial exacto de Clopper–Pearson es aproximadamente **(0,157; 0,843)**. Ambos intervalos son amplios, reflejo de la poca información aportada por ocho comercios.
