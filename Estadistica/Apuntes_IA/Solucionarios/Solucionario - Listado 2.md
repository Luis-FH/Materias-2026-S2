# Solucionario — Listado 2

#certamen1_estadistica

**Fuente:** [[Listado 2 523250 E y P_II_2026.pdf]]  
**Material relacionado:** [[Clase 1 - De los datos a su resumen]]

> Para las tablas agrupadas se estima cada medida usando la marca de clase; las interpolaciones dentro de un intervalo suponen distribución uniforme. En las varianzas descriptivas se divide por \(n\).

## 1. Duración de 82 entrevistas

Las marcas de clase son \(16,5;\,24,5;\,32,5;\,40,5;\,48,5\) minutos. Las frecuencias acumuladas son \(9,23,43,73,82\).

| Tiempo (min) | Marca \(x_i\) | \(n_i\) | \(N_i\) |
|---|---:|---:|---:|
| \([12,5;20,5]\) | 16,5 | 9 | 9 |
| \((20,5;28,5]\) | 24,5 | 14 | 23 |
| \((28,5;36,5]\) | 32,5 | 20 | 43 |
| \((36,5;44,5]\) | 40,5 | 30 | 73 |
| \((44,5;52,5]\) | 48,5 | 9 | 82 |

### a) Media

\[
\bar x\approx\frac{\sum n_ix_i}{82}
=\frac{9(16,5)+14(24,5)+20(32,5)+30(40,5)+9(48,5)}{82}
=\frac{2793}{82}\approx34,06\text{ min}.
\]

### b) Desviación estándar e interpretación

Con los puntos medios:

\[
\frac{\sum n_ix_i^2}{82}=\frac{102\,356,5}{82}=1248,25,
\qquad
s^2\approx1248,25-(34,06098)^2=88,09994\text{ min}^2.
\]

\[
s\approx\sqrt{88,09994}=9,39\text{ min}.
\]

La duración se dispersa típicamente alrededor de 9,39 minutos respecto del promedio estimado de 34,06 minutos.

### c) Tiempo que deja al 75 % de la muestra por debajo

La posición es \(0,75(82)=61,5\), dentro de la cuarta clase: su límite inferior es 36,5, la frecuencia acumulada anterior es 43 y la frecuencia de clase es 30. Por interpolación:

\[
P_{75}\approx36,5+\frac{61,5-43}{30}(8)
=41,433\text{ min}.
\]

Así, aproximadamente el 75 % de las duraciones no supera 41,43 minutos.

### d) Porcentaje que excede 40 minutos

El umbral 40 está dentro de la cuarta clase \((36,5;44,5]\). De sus 30 observaciones, se estima que la fracción \(4,5/8\) supera 40. Se agregan las 9 de la última clase:

\[
30\left(\frac{44,5-40}{8}\right)+9=16,875+9=25,875,
\qquad
\frac{25,875}{82}(100)\approx31,55\%.
\]

La estimación es **31,55 %**.

### e) Histograma y comentario

Los intervalos tienen amplitud común de 8 minutos:

```text
[12,5;20,5]  █████████                          9
(20,5;28,5]  ██████████████                    14
(28,5;36,5]  ████████████████████              20
(36,5;44,5]  ██████████████████████████████    30
(44,5;52,5]  █████████                          9
             Cada █ representa 1 entrevista
```

Es unimodal, con máximo en \((36,5;44,5]\). Las frecuencias suben desde la primera clase y bajan después de la clase modal; la caída es más pronunciada hacia los tiempos altos. El dibujo de frecuencias no es perfectamente simétrico.

## 2. Edades de niños del centro de salud

Hay \(n=20+9+1+7+3=40\) niños.

### a) Media, mediana y moda

\[
\bar x=\frac{6(20)+7(9)+8(1)+9(7)+10(3)}{40}
=\frac{284}{40}=7,1\text{ años}.
\]

Las observaciones 20 y 21 son 6 y 7 años, respectivamente; por tanto, la mediana es \((6+7)/2=6,5\) años. La moda es **6 años**, con 20 niños.

### b) Varianza, desviación estándar y coeficiente de variación

\[
E(X^2)=\frac{6^2(20)+7^2(9)+8^2(1)+9^2(7)+10^2(3)}{40}
=\frac{2092}{40}=52,3.
\]

\[
\sigma^2=E(X^2)-\bar x^2=52,3-7,1^2=1,89\text{ años}^2,
\quad \sigma=\sqrt{1,89}\approx1,375\text{ años}.
\]

\[
CV=\frac{\sigma}{\bar x}(100\%)=\frac{1,37477}{7,1}(100\%)\approx19,36\%.
\]

### c) Gráfico

La edad toma valores discretos, así que corresponde un gráfico de barras:

```text
6 años   ████████████████████ 20
7 años   █████████             9
8 años   █                     1
9 años   ███████               7
10 años  ███                   3
         Cada █ representa 1 niño
```

## 3. Coeficiente de variación de ingresos netos

Para las 20 compañías exitosas, los datos de \(X\) suman 318 y sus cuadrados suman 7416:

\[
\bar x=318/20=15,9,\qquad
E(X^2)=7416/20=370,8,
\]
\[
\sigma_X^2=370,8-15,9^2=117,99,\qquad
\sigma_X\approx10,8623.
\]

\[
CV_X=\frac{10,8623}{15,9}(100\%)\approx68,32\%.
\]

Para las 250 compañías regularmente exitosas:

\[
\bar y=2125/250=8,5,\qquad
E(Y^2)=18625/250=74,5,
\]
\[
\sigma_Y^2=74,5-8,5^2=2,25,\qquad \sigma_Y=1,5,
\qquad CV_Y=\frac{1,5}{8,5}(100\%)\approx17,65\%.
\]

El ingreso neto como porcentaje de **las ventas** (grupo de compañías regularmente exitosas) es más homogéneo: tiene el menor CV, 17,65 % frente a 68,32 %.

## 4. Resistencia a la tensión: empresas A y B

Se usan marcas \(15,25,35,45,55\) y se divide la varianza por el tamaño de cada grupo.

| Resistencia | Marca | \(n_{iA}\) | \(N_{iA}\) | \(n_{iB}\) | \(N_{iB}\) |
|---|---:|---:|---:|---:|---:|
| \([10,20]\) | 15 | 9 | 9 | 6 | 6 |
| \((20,30]\) | 25 | 12 | 21 | 11 | 17 |
| \((30,40]\) | 35 | 25 | 46 | 12 | 29 |
| \((40,50]\) | 45 | 15 | 61 | 22 | 51 |
| \((50,60]\) | 55 | 7 | 68 | 14 | 65 |

### a) ¿Qué empresa presenta menor dispersión?

Las medias y desviaciones estándar estimadas son:

\[
\bar x_A=\frac{2370}{68}=34,853,\quad
\sigma_A=\sqrt{\frac{91700}{68}-(34,853)^2}\approx11,567;
\]
\[
\bar x_B=\frac{2545}{65}=39,154,\quad
\sigma_B=\sqrt{\frac{109825}{65}-(39,154)^2}\approx12,514.
\]

Si “dispersión” significa desviación estándar absoluta, **A** tiene menor dispersión: 11,57 frente a 12,51 unidades de resistencia. Si se compara la dispersión relativa a medias distintas, \(CV_A\approx33,19\%\) y \(CV_B\approx31,96\%\); con ese criterio, **B** es más homogénea. La elección depende del criterio de dispersión usado.

### b) Percentil 25 de A

La posición es \(0,25(68)=17\); cae en la clase \((20,30]\), pues la frecuencia acumulada pasa de 9 a 21:

\[
P_{25,A}\approx20+\frac{17-9}{12}(10)=26,667.
\]

El 25 % de los lotes de A tiene resistencia estimada no superior a **26,67** unidades.

### c) Medianas de A y B

Para A, \(n/2=34\), que cae en \((30,40]\):

\[
P_{50,A}\approx30+\frac{34-21}{25}(10)=35,2.
\]

Para B, \(n/2=32,5\), que cae en \((40,50]\):

\[
P_{50,B}\approx40+\frac{32,5-29}{22}(10)=41,591.
\]

La mediana estimada de B supera a la de A; la mitad de los lotes de cada empresa queda aproximadamente por debajo de su respectivo valor.

### d) Histogramas y polígonos de frecuencia

Como las clases tienen igual amplitud, se pueden comparar alturas de frecuencia:

```text
Resistencia   Empresa A                 Empresa B
[10,20]       █████████ 9                ██████ 6
(20,30]       ████████████ 12            ███████████ 11
(30,40]       █████████████████████████ 25 ████████████ 12
(40,50]       ███████████████ 15          ██████████████████████ 22
(50,60]       ███████ 7                   ██████████████ 14
```

Los polígonos se construyen uniendo las marcas de clase con sus frecuencias:

| Marca | A | B |
|---:|---:|---:|
| 15 | 9 | 6 |
| 25 | 12 | 11 |
| 35 | 25 | 12 |
| 45 | 15 | 22 |
| 55 | 7 | 14 |

Para cada empresa, los puntos a unir son \((15,n_1),(25,n_2),(35,n_3),(45,n_4),(55,n_5)\); se puede cerrar cada polígono con frecuencia cero a media amplitud antes y después.

## 5. Ventas diarias de 100 vendedores

Se obtienen las frecuencias relativas de la información dada:

\[
f_2=F_2-f_1=0,5-0,2=0,3,\quad F_3=0,6,\quad
F_5=1,\quad F_4=1,9-1=0,9,
\]
\[
f_4=0,9-0,6=0,3,\qquad f_5=1-0,9=0,1.
\]

El resultado es:

| Clase | Ventas (miles de pesos) | \(f_i\) | Vendedores | \(F_i\) |
|---:|---:|---:|---:|---:|
| 1 | \([50,100)\) | 0,2 | 20 | 0,2 |
| 2 | \([100,150)\) | 0,3 | 30 | 0,5 |
| 3 | \([150,200)\) | 0,1 | 10 | 0,6 |
| 4 | \([200,250)\) | 0,3 | 30 | 0,9 |
| 5 | \([250,300]\) | 0,1 | 10 | 1,0 |

### b) Porcentaje que recibe el plus por vender más de $220.000

El umbral equivale a 220 miles de pesos y cae en la clase \([200,250)\). Suponiendo ventas uniformes dentro de la clase, la proporción de esa clase que supera 220 es \((250-220)/50=0,6\). Se estima que \(0,6(30)=18\) vendedores de esa clase cumplen; se suman los 10 de la clase superior:

\[
\frac{18+10}{100}(100\%)=\boxed{28\%}.
\]

### c) Venta mínima para no tener el sueldo congelado

El umbral es el percentil 25. Su posición es 25; la primera clase acumula 20 vendedores y la segunda contiene 30:

\[
P_{25}\approx100+\frac{25-20}{30}(50)
=108,333\text{ miles de pesos}.
\]

La frontera estimada es **$108.333,33 diarios**. Según la regla de congelar a los vendedores con menores ventas, quien venda al menos ese monto no queda en el 25 % inferior (la agrupación solo permite una estimación).

## 6. Concentración de níquel y pH

### a) Resumen gráfico

Cada variable está agrupada en clases de igual amplitud; se pueden usar histogramas con las frecuencias como alturas.

```text
Níquel (mg/kg)
[30,40[  ███████       7
[40,50[  ████████      8
[50,60[  ██████        6
[60,70[  ███           3
[70,80[  ██            2
[80,90]  ████          4

pH
[3,0;3,5[  ███           3
[3,5;4,0[  ████          4
[4,0;4,5[  ███████       7
[4,5;5,0[  █████████     9
[5,0;5,5[  █████         5
[5,5;6,0]  ██            2

Cada █ representa 1 punto de muestreo
```

El níquel alcanza su frecuencia máxima en \([40,50[\) mg/kg y tiene una cola de frecuencias bajas hacia los intervalos altos. El pH se concentra principalmente entre 4,0 y 5,0, con moda agrupada en \([4,5;5,0[\).

### b) Percentil 50 del níquel y promedio del pH

Para el níquel, \(n=30\), \(n/2=15\). La frecuencia acumulada llega a 7 en la primera clase y a 15 en la segunda:

\[
P_{50}\approx40+\frac{15-7}{8}(10)=50\text{ mg/kg}.
\]

Para el promedio de pH se usan las marcas \(3,25;\,3,75;\,4,25;\,4,75;\,5,25;\,5,75\):

\[
\bar x_{\rm pH}
=\frac{3(3,25)+4(3,75)+7(4,25)+9(4,75)+5(5,25)+2(5,75)}{30}
=\frac{135}{30}=4,50.
\]

### c) Comparación de coeficientes de variación

Para níquel, con marcas \(35,45,55,65,75,85\):

\[
\bar x_{\rm Ni}=1620/30=54,\quad
E(X^2)=95750/30=3191,667,
\]
\[
\sigma_{\rm Ni}=\sqrt{3191,667-54^2}\approx16,603,\quad
CV_{\rm Ni}\approx\frac{16,603}{54}(100\%)=30,75\%.
\]

Para pH:

\[
E(X^2)=621,375/30=20,7125,\quad
\sigma_{\rm pH}=\sqrt{20,7125-4,5^2}\approx0,6801,
\]
\[
CV_{\rm pH}\approx\frac{0,6801}{4,5}(100\%)=15,11\%.
\]

El **níquel** presenta mayor variabilidad relativa: su CV es aproximadamente 30,75 %, comparado con 15,11 % para el pH.
