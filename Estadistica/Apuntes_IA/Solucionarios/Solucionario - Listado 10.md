---
seguimiento_certamen2: true
bloque_certamen2: "Regresión"
progreso_certamen2: false
---

# Solucionario — Listado 10: Regresión lineal

#certamen2_estadistica

**Fuente:** [[Listado 10 523250 E y P_II_2026.pdf]] (cinco páginas; se revisó también el anexo completo de salidas).

**Recursos directos:** [[Clase7_2026_regre_lineal_simple_2026.pdf]] y [[Clase8_2026_regre_multiple.pdf]].

**Clasificación:** Certamen 2, por su contenido de regresión lineal simple y múltiple.

## 1. Años de experiencia y salario

Se tiene \(n=100\), \(\sum Y_i=1180\), \(\sum Y_i^2=25543\), \(\sum X_i=1000\), \(\sum X_i^2=12820\) y \(\sum X_iY_i=13469\). El salario \(Y\) está expresado en miles de dólares mensuales.

### a) Recta de regresión estimada

\[
\bar x=\frac{1000}{100}=10,\qquad \bar y=\frac{1180}{100}=11{,}8.
\]

Las sumas centradas son

\[
S_{xx}=12820-\frac{1000^2}{100}=2820,
\]
\[
S_{yy}=25543-\frac{1180^2}{100}=11619,
\qquad
S_{xy}=13469-\frac{1000(1180)}{100}=1669.
\]

Por mínimos cuadrados,

\[
b_1=\frac{S_{xy}}{S_{xx}}=\frac{1669}{2820}=0{,}591844,
\qquad
b_0=\bar y-b_1\bar x=11{,}8-(0{,}591844)(10)=5{,}881560.
\]

Por tanto,

\[
\boxed{\widehat Y=5{,}88156+0{,}591844X}.
\]

La pendiente indica un aumento estimado de **0,591844 miles de dólares por mes** en el salario por cada año adicional de experiencia, en promedio lineal.

### b) Salario estimado para cinco años de experiencia

\[
\widehat Y(5)=5{,}881560+0{,}591844(5)=8{,}840780.
\]

**Respuesta:** \(8{,}84078\) miles de dólares mensuales, es decir, aproximadamente **\$8.840,78 al mes**.

### c) Calidad del ajuste

\[
R^2=\frac{S_{xy}^2}{S_{xx}S_{yy}}
=\frac{1669^2}{2820(11619)}
=0{,}085015.
\]

La recta explica solo **8,50 %** de la variabilidad muestral del salario. La correlación muestral es \(r=\sqrt{R^2}=0{,}2916\), positiva, pero débil; el error estándar residual es aproximadamente

\[
s_e=\sqrt{\frac{SSE}{n-2}}
=\sqrt{\frac{11619-b_1(1669)}{98}}
=10{,}4155
\]

en miles de dólares. Así, la relación lineal tiene **bajo poder explicativo y predicciones individuales imprecisas**. Aun así, la pendiente estimada es positiva y su estadístico \(t\approx3{,}02\) (98 grados de libertad), lo cual sugiere evidencia de asociación lineal distinta de cero. Asociación estadística no implica causalidad.

## 2. Resistencia a la tracción y dimensiones del alambre

Las variables predictoras son \(X_1,\ldots,X_6\), según la definición de la primera página. Cada salida usa los datos del enunciado y tiene \(n=19\) (los grados de libertad residuales son 12 con seis predictores).

En las siguientes tablas, los estadísticos \(F\) faltantes se reconstruyen como

\[
F_{\text{ANOVA}}=\frac{\text{Suma de cuadrados del término}}{\text{cuadrado medio residual}},
\qquad
F_{\text{global}}=\frac{R^2/p}{(1-R^2)/(n-p-1)}.
\]

Los valores se redondean; pequeñas diferencias son esperables porque el PDF entrega varios datos con pocas cifras.

### a) Ecuaciones estimadas

| Salida | Modelo estimado |
|---|---|
| A | \(\widehat Y=3{,}13682+0{,}64443X_1-0{,}01042X_2+0{,}50465X_3-0{,}11967X_4-2{,}46177X_5+1{,}50441X_6\) |
| B | \(\widehat Y=4{,}96439+0{,}45370X_1+0{,}49090X_3-0{,}10707X_4-1{,}82178X_5\) |
| C | \(\widehat Y=2{,}41933+0{,}55297X_1+0{,}47898X_3-0{,}12338X_4\) |
| D | \(\widehat Y=4{,}65631+0{,}51133X_3-0{,}12418X_4\) |
| E | \(\widehat Y=-8{,}9710+0{,}5931X_3\) |
| F | \(\widehat Y=24{,}60167-0{,}16344X_4\) |

### b) Pruebas de hipótesis de las salidas

Para los coeficientes individuales, la salida de regresión prueba \(H_0:\beta_j=0\) frente a una alternativa bilateral. La prueba \(F\) global contrasta que todos los coeficientes de pendiente del modelo sean cero. Para \(\alpha=0{,}05\):

| Modelo | \(F\) global (gl) | Valor \(p\) global | Conclusión global | Coeficientes de pendiente con \(p<0{,}05\) |
|---|---:|---:|---|---|
| A | 4,928 (6, 12) | 0,00921 | Significativo | \(X_3\) (0,00403) |
| B | 7,693 (4, 14) | 0,001699 | Significativo | \(X_3\) (0,00284), \(X_4\) (0,04743) |
| C | 10,272 (3, 15) | 0,0006303 | Significativo | \(X_3\) (0,00271), \(X_4\) (0,01415) |
| D | 14,701 (2, 16) | 0,0002379 | Significativo | \(X_3\) (0,00125), \(X_4\) (0,01336) |
| E | 15,520 (1, 17) | 0,001057 | Significativo | \(X_3\) (0,00106) |
| F | 7,664 (1, 17) | 0,01315 | Significativo | \(X_4\) (0,01315) |

Así, para cada una de las seis salidas se rechaza la hipótesis global de pendientes nulas al 5 %. Esto no significa que todos sus predictores sean significativos: por ejemplo, en A solo \(X_3\) lo es individualmente; en B, \(X_1\) y \(X_5\) no lo son; en C, \(X_1\) no lo es.

La tabla ANOVA que acompaña a las salidas usa pruebas secuenciales (tipo I): cada fila contrasta el aporte de esa variable **después de las variables que aparecen antes** en esa fórmula. Los estadísticos \(F\) faltantes son:

| Modelo | Términos en el orden de la salida: \(F\) ANOVA (valor \(p\) reportado) |
|---|---|
| A | \(X_1:4{,}337\) (0,059343); \(X_2:2{,}187\) (0,164974); \(X_3:16{,}864\) (0,001455); \(X_4:4{,}715\) (0,050673); \(X_5:0{,}476\) (0,503302); \(X_6:0{,}980\) (0,341642) |
| B | \(X_1:4{,}673\) (0,048455); \(X_3:17{,}916\) (0,0008357); \(X_4:7{,}525\) (0,015856); \(X_5:0{,}657\) (0,4310898) |
| C | \(X_1:4{,}782\) (0,0450181); \(X_3:18{,}335\) (0,0006552); \(X_4:7{,}701\) (0,0141538) |
| D | \(X_3:21{,}667\) (0,0002643); \(X_4:7{,}733\) (0,0133574) |
| E | \(X_3:15{,}520\) (0,001057) |
| F | \(X_4:7{,}664\) (0,01315) |

El orden importa en estas filas; no se deben confundir con las pruebas \(t\) de cada coeficiente, que evalúan su efecto condicionado a los demás predictores del modelo.

### c) Elección del modelo e interpretación

Una elección parsimoniosa y respaldada por las pruebas es **D**, con \(X_3\) y \(X_4\):

\[
\widehat Y=4{,}65631+0{,}51133X_3-0{,}12418X_4.
\]

Ambos coeficientes de pendiente son significativos al 5 %. En cambio, al agregar \(X_1\) a D para obtener C, el coeficiente de \(X_1\) tiene \(p=0{,}30110\); no hay evidencia de que esa variable mejore el modelo una vez controladas \(X_3\) y \(X_4\). La \(R^2\) ajustada de C es 0,6071 y la de D es 0,6035, prácticamente similares; la desviación residual también es similar (0,8515 en C frente a 0,8554 en D). Por parsimonia se prefiere D. Es una selección razonable, no una demostración de que sea el único modelo posible.

- Manteniendo fijo \(X_4\), aumentar \(X_3\) en una unidad se asocia con un aumento estimado de **0,51133 unidades de resistencia**.
- Manteniendo fijo \(X_3\), aumentar \(X_4\) en una unidad se asocia con una disminución estimada de **0,12418 unidades de resistencia**.
- Las unidades específicas de \(X_3\), \(X_4\) y de la resistencia no están indicadas en el anexo; por ello no se pueden añadir unidades físicas sin inventarlas. Las interpretaciones son asociativas, no causales.

El intercepto estima la resistencia cuando \(X_3=X_4=0\). Ese punto no representa dimensiones físicas plausibles de un alambre, por lo que **no es razonable darle una interpretación práctica**; sirve para posicionar la recta/plano ajustado.

### d) Coeficiente de determinación de D

\[
R^2=0{,}6476.
\]

El modelo lineal con \(X_3\) y \(X_4\) explica aproximadamente **64,76 % de la variabilidad muestral** de la resistencia a la tracción. El 35,24 % restante queda en los residuos y otros factores no incluidos. La \(R^2\) ajustada es aproximadamente 0,6035.

## 3. Ventas y presupuesto en medios publicitarios

El anexo muestra cinco modelos para \(n=200\) observaciones, con `sales` como respuesta y combinaciones de `youtube`, `facebook` y `newspaper` como predictores.

### a) Modelos estimados

| Salida | Modelo estimado |
|---|---|
| A | \(\widehat{sales}=3{,}526667+0{,}045765\,youtube+0{,}188530\,facebook-0{,}001037\,newspaper\) |
| B | \(\widehat{sales}=3{,}50532+0{,}04575\,youtube+0{,}18799\,facebook\) |
| C | \(\widehat{sales}=8{,}439112+0{,}047537\,youtube\) |
| D | \(\widehat{sales}=11{,}17397+0{,}20250\,facebook\) |
| E | \(\widehat{sales}=14{,}82169+0{,}05469\,newspaper\) |

### b) Pruebas de hipótesis

En todos los modelos la prueba \(F\) global contrasta que todas las pendientes sean cero. Los valores faltantes se calculan a partir de \(R^2\) y los grados de libertad:

| Modelo | \(R^2\) ajustada | \(F\) global (gl) | Valor \(p\) global |
|---|---:|---:|---:|
| A | 0,8956 | 570,3 (3, 196) | \(<2{,}2\times10^{-16}\) |
| B | 0,8962 | 859,6 (2, 197) | \(<2{,}2\times10^{-16}\) |
| C | 0,6099 | 312,18 (1, 198) | \(<2{,}2\times10^{-16}\) |
| D | 0,3286 | 98,41 (1, 198) | \(<2{,}2\times10^{-16}\) |
| E | 0,0473 | 10,89 (1, 198) | 0,001148 |

Todos los modelos son globalmente significativos al 5 %. Para los coeficientes individuales, la salida A indica que YouTube y Facebook son significativos (\(p<2\times10^{-16}\)), pero periódico no (\(p=0{,}86\)). En B, YouTube y Facebook son significativos (ambos \(p<2\times10^{-16}\)). En C, YouTube es significativo; en D, Facebook es significativo; y en E, periódico es significativo (\(p=0{,}00115\)). Que un predictor sea significativo en un modelo simple no implica que aporte información adicional al incluir otros predictores.

### c) Elección del modelo e interpretación

Se elige **B**, con YouTube y Facebook:

\[
\widehat{sales}=3{,}50532+0{,}04575\,youtube+0{,}18799\,facebook.
\]

El modelo A agrega `newspaper`, cuyo coeficiente tiene \(p=0{,}86\), sin evidencia de aporte una vez controlados los otros medios. El \(R^2\) de A y B se redondea a 0,8972, la \(R^2\) ajustada es ligeramente mayor en B (0,8962 frente a 0,8956) y el error estándar residual baja de 2,023 a 2,018.

- Manteniendo fijo el presupuesto de Facebook, un aumento de una unidad en `youtube` se asocia con un aumento estimado de **0,04575 unidades de ventas**.
- Manteniendo fijo el presupuesto de YouTube, un aumento de una unidad en `facebook` se asocia con un aumento estimado de **0,18799 unidades de ventas**.
- El intercepto 3,50532 representa las ventas estimadas si ambos presupuestos fueran cero. Es una referencia matemática; su interpretación práctica depende de si cero gasto está en el rango observado, algo que el anexo no informa. No debe extrapolarse sin verificarlo.

El PDF declara las ventas en dólares, pero no especifica claramente en qué unidades están codificados los predictores y las salidas del conjunto `marketing`. Por eso las pendientes se expresan como **unidades de `sales` por unidad de presupuesto**, sin convertirlas a dólares o miles de dólares.

### d) Coeficiente de determinación del modelo B

\[
R^2=0{,}8972.
\]

YouTube y Facebook explican conjuntamente aproximadamente **89,72 % de la variabilidad muestral** de las ventas; alrededor de 10,28 % no queda explicado por este modelo lineal.

### f) Completar la tabla ANOVA del modelo elegido

Para B, el cuadrado medio residual es

\[
CM_E=\frac{802{,}0}{197}=4{,}0711.
\]

Los \(F\) secuenciales se obtienen como \(CM_{\text{término}}/CM_E\). La tabla completa, con redondeos compatibles con las sumas de cuadrados impresas, es:

| Fuente | gl | Suma de cuadrados | Cuadrado medio | \(F\) | Valor \(p\) |
|---|---:|---:|---:|---:|---:|
| `youtube` | 1 | 4773,1 | 4773,1 | **1172,44** | \(<2{,}2\times10^{-16}\) |
| `facebook` | 1 | 2225,7 | 2225,7 | **546,71** | \(<2{,}2\times10^{-16}\) |
| Residuos | 197 | 802,0 | **4,0711** | — | — |

Los \(F\) de esta tabla son secuenciales: `facebook` se evalúa después de `youtube`, según el orden de la fórmula en R.

## Valores faltantes reconstruidos del anexo

Además de los solicitados para el modelo escogido, se completaron las cifras ausentes de las salidas. En la tabla ANOVA de regresión para tracción (ejercicio 2), los \(F\) son:

| Salida | \(F\) global | \(F\) de las filas ANOVA en orden |
|---|---:|---|
| A | 4,928 | 4,337; 2,187; 16,864; 4,715; 0,476; 0,980 |
| B | 7,693 | 4,673; 17,916; 7,525; 0,657 |
| C | 10,272 | 4,782; 18,335; 7,701 |
| D | 14,701 | 21,667; 7,733 |
| E | 15,520 | 15,520 |
| F | 7,664 | 7,664 |

En la tabla ANOVA para ventas (ejercicio 3), los \(F\) de las filas de predictores, en orden, son:

| Salida | \(F\) de las filas ANOVA en orden |
|---|---|
| A | 1166,78; 544,07; 0,0244 |
| B | 1172,44; 546,71 |
| C | 312,15 |
| D | 98,42 |
| E | 10,89 |

Las \(R^2\) ajustadas reconstruidas son: tracción A 0,5670; B 0,5980; C 0,6071; D 0,6035; E 0,4464; F 0,2702; ventas A 0,8956; B 0,8962; C 0,6099; D 0,3286; E 0,0473.
