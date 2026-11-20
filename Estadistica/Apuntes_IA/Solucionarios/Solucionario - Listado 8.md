---
seguimiento_certamen2: true
bloque_certamen2: "Intervalos"
progreso_certamen2: false
---

# Solucionario — Listado 8: Intervalos para comparar grupos

#certamen2_estadistica

**Fuente:** [[Ayudantia_Intervalos_de_Confianza_2.pdf]] (dos páginas; se resolvieron los cuatro ejercicios).

**Recursos directos:** [[Clase5_2026.pdf]], [[Resumen_intervalos_de_confianza.pdf]] y [[Tablas Estadísticas.pdf]].

## 1. Permeabilidad del concreto con dos contenidos de asfalto

Definimos la diferencia como media con 3 % menos media con 7 % de asfalto. Los datos son:

- 3 %: \(1189,840,1020,980\), \(n_1=4\).
- 7 %: \(853,900,733,785\), \(n_2=4\).

Las medias y varianzas muestrales son

\[
\bar x_1=\frac{4029}{4}=1007{,}25,\qquad
s_1^2=\frac{61910{,}75}{3}=20636{,}92,
\]
\[
\bar x_2=\frac{3271}{4}=817{,}75,\qquad
s_2^2=\frac{16262{,}75}{3}=5420{,}92.
\]

La diferencia observada es \(189{,}50\) pulg/hora. Como no se especifica igualdad de varianzas, usamos el intervalo de Welch:

\[
SE=\sqrt{\frac{s_1^2}{n_1}+\frac{s_2^2}{n_2}}
=\sqrt{\frac{20636{,}92}{4}+\frac{5420{,}92}{4}}
=80{,}7122.
\]

Los grados de libertad aproximados de Welch son

\[
\nu=
\frac{(s_1^2/n_1+s_2^2/n_2)^2}
{(s_1^2/n_1)^2/(n_1-1)+(s_2^2/n_2)^2/(n_2-1)}
\approx4{,}474.
\]

Para un intervalo bilateral del 90 %, \(t_{0{,}95;\,4{,}474}\approx2{,}0685\). Entonces

\[
\begin{aligned}
(\mu_{3\%}-\mu_{7\%})
&\in(\bar x_1-\bar x_2)\pm tSE\\
&=189{,}50\pm2{,}0685(80{,}7122)\\
&\approx(22{,}54,\ 356{,}46)\text{ pulg/hora}.
\end{aligned}
\]

**Interpretación:** el intervalo estima que la permeabilidad media del concreto con 3 % de asfalto supera la del concreto con 7 % entre aproximadamente 22,5 y 356,5 pulg/hora. El intervalo no contiene cero.

### b) Supuestos necesarios

- Los dos grupos son independientes entre sí y las observaciones son independientes dentro de cada grupo.
- Las muestras representan aleatoriamente sus poblaciones o tratamientos.
- Dado que solo hay cuatro especímenes por grupo, se requiere que las permeabilidades de cada grupo provengan de poblaciones aproximadamente normales y que no haya valores atípicos graves.
- El intervalo empleado es Welch: **no** requiere suponer varianzas poblacionales iguales.

El enunciado no informa el procedimiento de selección/asignación ni permite verificar normalidad; son supuestos requeridos, no hechos establecidos por el PDF.

## 2. Proporción de propietarios con al menos un accidente

Tomamos la diferencia \(p_R-p_B\), rojo menos blanco:

\[
\hat p_R=\frac{45}{100}=0{,}45,\qquad
\hat p_B=\frac{70}{200}=0{,}35,\qquad
\hat p_R-\hat p_B=0{,}10.
\]

Para un intervalo del 90 % de diferencia de proporciones se usa el error estándar no combinado:

\[
\begin{aligned}
SE
&=\sqrt{\frac{0{,}45(0{,}55)}{100}
+\frac{0{,}35(0{,}65)}{200}}\\
&=\sqrt{0{,}0036125}=0{,}06010.
\end{aligned}
\]

Con \(z_{0{,}95}=1{,}6449\), el margen es \(1{,}6449(0{,}06010)=0{,}09884\). Por tanto,

\[
IC_{90\%}(p_R-p_B)=0{,}10\pm0{,}09884
=(0{,}00116,\ 0{,}19884).
\]

**Respuesta e interpretación:** el intervalo aproximado es **(0,0012; 0,1988)**, o entre **0,12 y 19,88 puntos porcentuales** más de probabilidad en propietarios de autos rojos. Al 90 %, el intervalo queda apenas por encima de cero. La aproximación normal es razonable en conteos (45 y 55 para rojos; 70 y 130 para blancos). Se supone que las muestras son independientes y que las respuestas son observaciones Bernoulli independientes.

## 3. Tiempo de traslado según el medio de transporte

Definimos la diferencia como automóvil menos transporte público:

\[
n_1=35,\quad\bar x_1=32,\quad s_1=5;\qquad
n_2=27,\quad\bar x_2=38,\quad s_2=8.
\]

Las varianzas poblacionales son desconocidas y no se indica que sean iguales; usamos el intervalo de Welch. La diferencia observada es \(32-38=-6\) minutos, y

\[
SE=\sqrt{\frac{5^2}{35}+\frac{8^2}{27}}
=\sqrt{3{,}08466}=1{,}75632\text{ minutos}.
\]

Los grados de libertad de Welch son

\[
\nu=
\frac{(25/35+64/27)^2}
{(25/35)^2/34+(64/27)^2/26}
\approx41{,}17.
\]

Para un intervalo bilateral del 95 %, \(t_{0{,}975;\,41{,}17}\approx2{,}0193\):

\[
\begin{aligned}
IC_{95\%}(\mu_{\rm auto}-\mu_{\rm público})
&=-6\pm2{,}0193(1{,}75632)\\
&=(-9{,}55,\ -2{,}45)\text{ minutos}.
\end{aligned}
\]

**Conclusión:** sí, al 95 % hay evidencia de una diferencia en los tiempos medios, porque el intervalo no contiene cero. En promedio, el tiempo en automóvil es entre aproximadamente **2,45 y 9,55 minutos menor** que en transporte público.

**Supuestos:** muestras independientes y representativas, tiempos aproximadamente normales en cada grupo (supuesto indicado por el problema), y uso de Welch sin igualdad de varianzas.

## 4. Tiempo de limpieza antes y después de reorganizar las tareas

Las filas corresponden a los mismos días antes y después; por tanto, se trabaja con diferencias pareadas. Definimos \(D=\text{Antes}-\text{Después}\). Las nueve diferencias, en minutos, son

\[
8,\ 7,\ 5,\ 9,\ 8,\ 8,\ 6,\ 9,\ 7.
\]

Su media y desviación estándar muestral son

\[
\bar d=\frac{67}{9}=7{,}4444\text{ min},\qquad
s_d^2=\frac{14{,}2222}{8}=1{,}7778,\qquad
s_d=1{,}3333\text{ min}.
\]

Como \(n=9\) y la diferencia se supone normal, corresponde un intervalo \(t\) pareado con \(8\) grados de libertad. El error estándar es \(s_d/\sqrt n=1{,}3333/3=0{,}4444\) y \(t_{0{,}975;8}=2{,}3060\):

\[
\begin{aligned}
IC_{95\%}(\mu_D)
&=\bar d\pm t_{0{,}975;8}\frac{s_d}{\sqrt n}\\
&=7{,}4444\pm2{,}3060(0{,}4444)\\
&=(6{,}42,\ 8{,}47)\text{ minutos}.
\end{aligned}
\]

**Interpretación:** la rutina reorganizada reduce el tiempo promedio estimado entre **6,42 y 8,47 minutos**. El intervalo es para la media de las diferencias pareadas (antes menos después), no para dos muestras independientes.

**Supuestos y alcance:** las diferencias por día son independientes entre sí, su distribución poblacional es normal (supuesto del enunciado) y los registros antes/después están correctamente emparejados. La conclusión describe estos registros bajo esos supuestos; no establece causalidad general si las condiciones antes y después no fueron comparables.
