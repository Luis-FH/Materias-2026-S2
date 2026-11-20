---
seguimiento_certamen2: true
bloque_certamen2: "Pruebas de hipótesis"
progreso_certamen2: false
---

# Solucionario — Listado 9: Pruebas de hipótesis e intervalos

#certamen2_estadistica

**Fuente:** [[Listado 9 523250 E y P_II_2026.pdf]] (única página).

**Recursos directos:** [[Clase5_2026.pdf]], [[Clase6_2026.pdf]], [[Resumen_intervalos_de_confianza.pdf]] y [[Resumen_Prueba_de_Hipótesis.pdf]].

**Clasificación:** Certamen 2, por sus intervalos y pruebas de hipótesis para medias y proporciones.

## 1. Diferencia de sueldos semanales

Sean \(\mu_H\) y \(\mu_M\) los sueldos medios de hombres y mujeres, respectivamente. La afirmación «el promedio de los hombres excede al de las mujeres en más de \$20» se contrasta con

\[
H_0:\mu_H-\mu_M\le20
\qquad\text{vs.}\qquad
H_1:\mu_H-\mu_M>20.
\]

Los datos dan \(\bar x_H-\bar x_M=292{,}50-266{,}10=26{,}40\) dólares por semana. Con muestras grandes, el error estándar estimado de la diferencia es

\[
SE=\sqrt{\frac{15{,}60^2}{60}+\frac{18{,}20^2}{60}}
=3{,}0946.
\]

El estadístico unilateral, evaluado en la frontera nula \(\mu_H-\mu_M=20\), es

\[
z=\frac{26{,}40-20}{3{,}0946}=2{,}0681.
\]

Al nivel \(\alpha=0{,}01\), el valor crítico unilateral es \(z_{0{,}99}=2{,}3263\). Como \(2{,}0681<2{,}3263\) (valor \(p\) aproximado \(0{,}019\)), **no se rechaza \(H_0\)**.

**Conclusión:** aunque la diferencia observada es \$26,40 por semana, al 1 % no hay evidencia suficiente para afirmar que la diferencia poblacional exceda \$20 por semana.

## 2. Comparación de la resistencia media de dos aceros

La diferencia observada es

\[
\bar x_1-\bar x_2=18{,}12-16{,}87=1{,}25\text{ kg/cm}^2.
\]

En ambos incisos se contrasta \(H_0:\mu_1-\mu_2=0\) contra \(H_1:\mu_1-\mu_2\ne0\), con \(\alpha=0{,}01\).

### a) Varianzas poblacionales conocidas

Se conocen \(\sigma_1^2=1{,}6\), \(\sigma_2^2=1{,}4\), \(n_1=40\) y \(n_2=32\). Corresponde una prueba normal de dos muestras:

\[
SE=\sqrt{\frac{1{,}6}{40}+\frac{1{,}4}{32}}
=0{,}28940,\qquad
z=\frac{1{,}25}{0{,}28940}=4{,}3193.
\]

El valor crítico bilateral es \(z_{0{,}995}=2{,}5758\). Como \(|z|>2{,}5758\), **se rechaza \(H_0\)**.

**Conclusión:** al 1 % hay evidencia de que las resistencias medias difieren; la media muestral del acero 1 supera a la del acero 2 en \(1{,}25\text{ kg/cm}^2\).

### b) Solo se conocen las desviaciones estándar muestrales

Ahora \(s_1=1{,}6\) y \(s_2=1{,}4\), por lo que las varianzas poblacionales no son conocidas. Usamos la prueba \(t\) de Welch, sin suponer varianzas iguales:

\[
SE=\sqrt{\frac{1{,}6^2}{40}+\frac{1{,}4^2}{32}}
=0{,}35391,\qquad
t=\frac{1{,}25}{0{,}35391}=3{,}5320.
\]

Los grados de libertad de Welch son aproximadamente 69; el valor crítico bilateral al 1 % es cerca de 2,65. Como \(|t|>2{,}65\), **también se rechaza \(H_0\)**.

**Conclusión:** la respuesta no cambia: existe evidencia, al 1 %, de una diferencia entre las medias. (Si se impusiera igualdad de varianzas, la prueba agrupada daría una conclusión equivalente.)

## 3. Proporción que leyó el anuncio en dos ciudades

Ciudad 1: \(n_1=1000,\ \hat p_1=0{,}18\); ciudad 2: \(n_2=1000,\ \hat p_2=0{,}14\). La diferencia estimada es

\[
\hat p_1-\hat p_2=0{,}04.
\]

### a) Intervalo de confianza del 95 % para \(p_1-p_2\)

Para el intervalo se usa el error estándar no combinado:

\[
SE=\sqrt{\frac{0{,}18(0{,}82)}{1000}+
\frac{0{,}14(0{,}86)}{1000}}
=0{,}0163707.
\]

\[
\begin{aligned}
IC_{95\%}
&=(\hat p_1-\hat p_2)\pm1{,}96SE\\
&=0{,}04\pm1{,}96(0{,}0163707)\\
&=(0{,}00791;\ 0{,}07209).
\end{aligned}
\]

**Respuesta:** el intervalo es aproximadamente **(0,0079; 0,0721)**, o entre **0,79 y 7,21 puntos porcentuales** a favor de la ciudad 1.

### b) Prueba de igualdad de proporciones

\[
H_0:p_1=p_2
\qquad\text{vs.}\qquad
H_1:p_1\ne p_2.
\]

Bajo \(H_0\), la estimación combinada es

\[
\hat p=\frac{180+140}{2000}=0{,}16.
\]

Entonces

\[
SE_0=\sqrt{0{,}16(0{,}84)\left(\frac1{1000}+\frac1{1000}\right)}
=0{,}016394,
\qquad
z=\frac{0{,}04}{0{,}016394}=2{,}4398.
\]

El valor \(p\) bilateral es aproximadamente \(0{,}0147\), menor que 0,05. **Se rechaza \(H_0\) al 5 %**: las proporciones difieren. El intervalo del inciso anterior coincide con esta conclusión, pues no contiene 0.

### c) ¿La diferencia supera 0,1?

La prueba unilateral es

\[
H_0:p_1-p_2\le0{,}1
\qquad\text{vs.}\qquad
H_1:p_1-p_2>0{,}1.
\]

La diferencia observada está muy por debajo del umbral \(0{,}1\). Con el error estándar estimado del inciso (a), el estadístico evaluado en la frontera nula es

\[
z=\frac{(\hat p_1-\hat p_2)-0{,}1}{SE}
=\frac{0{,}04-0{,}1}{0{,}0163707}
=-3{,}6651.
\]

Para una alternativa a la derecha, el valor \(p\) es prácticamente 1. Por tanto, **no se rechaza \(H_0\)** al 5 %.

### d) Conclusión contextual

La muestra estima una diferencia de solo **4 puntos porcentuales**, con una estimación mayor en la ciudad 1. Los datos no respaldan que la proporción de esa ciudad supere a la de la ciudad 2 en más de **10 puntos porcentuales**. No rechazar la hipótesis nula no demuestra que la diferencia sea menor o igual a 0,1; indica que no se obtuvo evidencia para la afirmación planteada.
