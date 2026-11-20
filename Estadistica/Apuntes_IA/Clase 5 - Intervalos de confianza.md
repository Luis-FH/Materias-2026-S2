---
seguimiento_certamen2: true
bloque_certamen2: Intervalos
progreso_certamen2: false
---

# Clase 5 — Intervalos de confianza: guía completa

#certamen2_estadistica

> [!info] Fuentes y conexiones
> - [[Clase5_2026.pdf]] — presentación «Intervalos de Confianza» (31 páginas).
> - **Listado 7:** [[Ayudantia_Intervalos_de_Confianza.pdf]] — guía de ejercicios de intervalos de confianza. La portada del PDF la titula «Listado 6»; aquí se clasifica como Listado 7 según la organización indicada.
> - **Listado 8:** [[Ayudantia_Intervalos_de_Confianza_2.pdf]] — guía de ejercicios de intervalos para medias y comparaciones.
> - [[Solucionario - Listado 7]] y [[Solucionario - Listado 8]] — resoluciones paso a paso de ambos listados.
> - [[Resumen_intervalos_de_confianza.pdf]] — resumen de intervalos de confianza.
> - Índice del ramo: Estadística.

## Mapa de la clase

Un intervalo de confianza combina un **estimador calculado con una muestra** y un **margen de error** para dar un rango de valores plausibles para un parámetro poblacional. El método cambia según el parámetro y la información disponible:

`parámetro → muestra/diseño → estimador → distribución pivote → cuantiles → intervalo → interpretación`

La presentación cubre:

1. Qué es un intervalo de confianza y cómo interpretarlo.
2. Intervalo para una media con varianza conocida.
3. Intervalo para una media con varianza desconocida.
4. Intervalo para la varianza de una población normal.
5. Intervalo para una proporción.
6. Diferencia de dos medias con varianzas conocidas.
7. Diferencia de dos medias con varianzas desconocidas e iguales.
8. Diferencia de dos medias con varianzas desconocidas y distintas.
9. Diferencia de medias en muestras pareadas.
10. Diferencia de dos proporciones.
11. Cociente de dos varianzas.

En cada tema: **1. resumen → 2. preguntas → 3. profundizar → 4. fórmulas → 5. conexión con ejercicios**. Los ejercicios son para practicar el método; esta nota no entrega una pauta con sus respuestas.

### Notación

- `1-α`: nivel de confianza del procedimiento; `α`: nivel de significación.
- `z_{1-α/2}`: cuantil de la normal estándar con área acumulada `1-α/2`.
- `t_{1-α/2,ν}`: cuantil de Student con `ν` grados de libertad.
- `χ²_{γ,ν}` y `F_{γ,ν1,ν2}`: cuantiles de cola izquierda `γ` de las distribuciones chi-cuadrado y F.
- `S²`: varianza muestral con denominador `n-1`; `S`: desviación estándar muestral.

Si tu tabla usa otra convención de cuantiles, comprueba el encabezado antes de sustituir.

---

## Tema 1 — Qué es un intervalo de confianza

### 1. Resumen

Un intervalo de confianza para un parámetro desconocido `θ` se construye a partir de una muestra aleatoria. Sus extremos dependen de la muestra; el parámetro poblacional se considera fijo.

Un procedimiento con confianza `1-α` produce intervalos que contienen el verdadero `θ` en aproximadamente una fracción `1-α` de las muestras repetidas, si se cumplen sus supuestos.

### 2. Preguntas

- ¿Cuál es el parámetro que se quiere estimar: una media, varianza, proporción o diferencia?
- ¿Qué cantidad de la muestra funciona como estimador puntual?
- ¿Qué cambia al aumentar el nivel de confianza manteniendo la muestra?
- ¿Qué cambia al aumentar el tamaño de muestra manteniendo la confianza?
- ¿Un intervalo de confianza del 95% significa que hay 95% de probabilidad de que el parámetro fijo esté en este intervalo ya calculado?

### 3. Profundizar

La interpretación frecuentista correcta se refiere al **método**, no a una probabilidad asignada al parámetro fijo después de observar la muestra. Si repitiéramos el muestreo y construyéramos un intervalo cada vez, alrededor del 95% de esos intervalos contendría el parámetro cuando el nivel es 95%.

La forma general de muchos intervalos bilaterales es:

`estimador ± cuantil × error estándar`.

El cuantil determina la confianza y la distribución de referencia. El error estándar mide cuánto varía el estimador entre muestras. A mayor confianza suele corresponder un cuantil y un intervalo mayores; a mayor tamaño muestral suele corresponder un error estándar menor.

El intervalo requiere condiciones de muestreo y modelo: aleatoriedad, independencia cuando corresponde, normalidad para algunos resultados exactos y tamaño suficiente para aproximaciones normales.

### 4. Fórmulas a considerar

Esquema general:

$$
\text{I.C.}=(\text{estimador}-\text{margen},\ \text{estimador}+\text{margen})
$$

Para un intervalo bilateral de confianza `1-α`, se asigna `α/2` a cada cola de la distribución pivote. Por ejemplo, `α=0.05` corresponde a un nivel de confianza de 95%.

### 5. Conexión con los ejercicios

- [[Ayudantia_Intervalos_de_Confianza.pdf]], ejercicios 1–3: interpretar y construir intervalos a partir de datos y de un nivel de confianza.
- [[Ayudantia_Intervalos_de_Confianza_2.pdf]], ejercicios 1–4: aplicar el método en contextos de medias, proporciones y muestras pareadas.

Antes de calcular, anota por separado **parámetro**, **estimador**, **nivel de confianza** y **supuestos**.

**Referencia:** [[Clase5_2026.pdf]], contenidos, objetivos y definición de intervalo (PDF, pp. 1–9).

---

## Tema 2 — Intervalo para una media con varianza poblacional conocida

### 1. Resumen

Si se estima la media `μ` de una población normal y se conoce su desviación estándar poblacional `σ`, se usa la normal estándar. El centro del intervalo es la media muestral `X̄`; el margen depende de `σ`, del tamaño de muestra `n` y del nivel de confianza.

### 2. Preguntas

- ¿Se conoce la desviación estándar de la población `σ`, o solo la de la muestra `S`?
- ¿Por qué el error estándar de `X̄` es `σ/√n`?
- ¿Qué cuantil normal corresponde a 90%, 95% o 99% de confianza?
- ¿Qué efecto tiene duplicar el tamaño muestral sobre el margen de error?

### 3. Profundizar

Para una muestra aleatoria de una población normal, `X̄` tiene media `μ` y varianza `σ²/n`. Al estandarizar, se obtiene un pivote normal estándar. El intervalo se obtiene despejando `μ` en la desigualdad central que conserva probabilidad `1-α`.

Este caso exige conocer `σ`. Si `σ` no está disponible y se reemplaza por `S`, el pivote pasa a ser Student (Tema 3); no conviene cambiar `σ` por `S` y mantener automáticamente el cuantil `z`.

### 4. Fórmulas a considerar

Pivote:

$$
Z=\frac{\bar X-\mu}{\sigma/\sqrt n}\sim N(0,1)
$$

Intervalo bilateral:

$$
\mu\in
\left(
\bar x-z_{1-\alpha/2}\frac{\sigma}{\sqrt n},\
\bar x+z_{1-\alpha/2}\frac{\sigma}{\sqrt n}
\right)
$$

Margen de error:

$$
E=z_{1-\alpha/2}\frac{\sigma}{\sqrt n}
$$

### 5. Conexión con los ejercicios

- [[Ayudantia_Intervalos_de_Confianza.pdf]], ejercicio 1, usa un contexto de duración con distribución normal para construir un intervalo de la media y relacionarlo con el error máximo.
- En el mismo ejercicio, identifica cuidadosamente si el dato entregado es `σ` poblacional o un resumen de una muestra.

**Referencia:** [[Clase5_2026.pdf]], «Para la media μ, varianza conocida» (PDF, pp. 10–13).

---

## Tema 3 — Intervalo para una media con varianza poblacional desconocida

### 1. Resumen

Si se estima `μ` en una población normal y `σ²` es desconocida, se reemplaza `σ` por la desviación estándar muestral `S` y se usa la distribución t de Student con `n-1` grados de libertad.

### 2. Preguntas

- ¿Por qué usamos `S` en vez de `σ`?
- ¿Qué grados de libertad corresponden a una muestra de tamaño `n`?
- ¿Cómo cambia la forma de la distribución t frente a la normal cuando hay pocos datos?
- ¿Qué ocurre con la t cuando crecen los grados de libertad?

### 3. Profundizar

La incertidumbre adicional por estimar `σ` hace que la t tenga colas más pesadas que la normal estándar, especialmente para muestras pequeñas. Al aumentar los grados de libertad, se aproxima a la normal.

El intervalo t exacto supone una muestra aleatoria independiente de una población normal. Con muestras grandes la aproximación puede ser útil bajo condiciones más generales, pero la forma del muestreo y posibles valores atípicos siguen importando.

No uses los grados de libertad `n-1` por costumbre en cualquier comparación de dos medias: este caso es **una sola muestra**.

### 4. Fórmulas a considerar

Pivote:

$$
T=\frac{\bar X-\mu}{S/\sqrt n}\sim t_{n-1}
$$

Intervalo bilateral:

$$
\mu\in
\left(
\bar x-t_{1-\alpha/2,n-1}\frac{s}{\sqrt n},\
\bar x+t_{1-\alpha/2,n-1}\frac{s}{\sqrt n}
\right)
$$

### 5. Conexión con los ejercicios

- [[Ayudantia_Intervalos_de_Confianza.pdf]], ejercicios 1–3: compara el caso donde la desviación está especificada con situaciones donde se estima a partir de los datos.
- [[Ayudantia_Intervalos_de_Confianza_2.pdf]], ejercicio 1: práctica de un intervalo para una diferencia de medias; contrástalo con este caso de una sola media para identificar el diseño correcto.

**Referencia:** [[Clase5_2026.pdf]], «Para la media μ, varianza desconocida» (PDF, pp. 14–15).

---

## Tema 4 — Intervalo para la varianza de una población normal

### 1. Resumen

Para estimar la varianza `σ²` de una población normal, se usa un pivote chi-cuadrado con `n-1` grados de libertad. El intervalo para `σ²` no suele ser simétrico alrededor de `S²`, porque la distribución chi-cuadrado es asimétrica.

### 2. Preguntas

- ¿Qué supuesto de distribución permite usar este pivote?
- ¿Por qué aparecen `n-1` grados de libertad?
- ¿Por qué se necesitan dos cuantiles distintos para los extremos?
- Si el intervalo pedido es para `σ` y no para `σ²`, qué transformación falta?

### 3. Profundizar

El pivote `(n-1)S²/σ²` sigue una chi-cuadrado cuando la población es normal. Despejando `σ²`, el cuantil más alto queda en el denominador del extremo inferior y el cuantil más bajo en el denominador del extremo superior: el orden se invierte al dividir.

El resultado corresponde a la varianza. Si el problema pide desviación estándar, toma la raíz cuadrada de ambos extremos, que son no negativos. La normalidad de la población es un supuesto importante para este intervalo exacto.

### 4. Fórmulas a considerar

Pivote:

$$
\frac{(n-1)S^2}{\sigma^2}\sim\chi^2_{n-1}
$$

Si `χ²_{γ,ν}` denota el cuantil de cola izquierda `γ`:

$$
\sigma^2\in
\left(
\frac{(n-1)s^2}{\chi^2_{1-\alpha/2,n-1}},\
\frac{(n-1)s^2}{\chi^2_{\alpha/2,n-1}}
\right)
$$

Intervalo para la desviación estándar:

$$
\sigma\in
\left(
\sqrt{\frac{(n-1)s^2}{\chi^2_{1-\alpha/2,n-1}}},\
\sqrt{\frac{(n-1)s^2}{\chi^2_{\alpha/2,n-1}}}
\right)
$$

### 5. Conexión con los ejercicios

- Las [[Ayudantia_Intervalos_de_Confianza.pdf]] y [[Ayudantia_Intervalos_de_Confianza_2.pdf]] permiten practicar la identificación del parámetro y del modelo, pero confirma en el enunciado cuál problema pide un intervalo para `σ²`; no confundas una desviación estándar de contexto con un intervalo para la varianza.
- En esta sección del material compartido no hay un Listado numerado que sirva como pauta específica de intervalos para varianza.

**Referencia:** [[Clase5_2026.pdf]], «Para la varianza σ² de X ~ N(μ,σ²)» (PDF, pp. 16–18).

---

## Tema 5 — Intervalo para una proporción poblacional

### 1. Resumen

Una proporción poblacional `p` describe la fracción de elementos que presenta una característica. Con `n` observaciones Bernoulli independientes, la proporción muestral es `p̂=X/n`, donde `X` cuenta éxitos.

Cuando la aproximación normal es razonable, el intervalo se centra en `p̂` y usa su error estándar estimado.

### 2. Preguntas

- ¿Qué resultado se definió como éxito?
- ¿Cuál es `X` y cómo se obtiene `p̂`?
- ¿Es suficiente que `n` sea grande, o debe haber suficientes éxitos y fracasos esperados?
- ¿Por qué el error estándar depende de `p` y cómo se reemplaza cuando `p` es desconocida?

### 3. Profundizar

La proporción muestral es una media de variables indicadoras 0/1. Por eso su varianza es `p(1-p)/n`, y el teorema central del límite motiva una aproximación normal cuando hay suficientes observaciones en ambas categorías.

Como `p` es desconocida, el intervalo de Wald sustituye `p` por `p̂` en el error estándar. La aproximación puede ser deficiente si hay pocos éxitos o pocos fracasos; verifica las condiciones indicadas en la clase y considera métodos alternativos cuando la muestra o la proporción sean extremas.

### 4. Fórmulas a considerar

Estimador:

$$
\hat p=\frac{X}{n}
$$

Error estándar estimado:

$$
\widehat{SE}(\hat p)=
\sqrt{\frac{\hat p(1-\hat p)}{n}}
$$

Intervalo normal aproximado:

$$
p\in
\left(
\hat p-z_{1-\alpha/2}
\sqrt{\frac{\hat p(1-\hat p)}{n}},\
\hat p+z_{1-\alpha/2}
\sqrt{\frac{\hat p(1-\hat p)}{n}}
\right)
$$

Condición aproximada de la presentación:

$$
n\hat p\geq 5,\qquad n(1-\hat p)\geq 5
$$

### 5. Conexión con los ejercicios

- [[Ayudantia_Intervalos_de_Confianza_2.pdf]], ejercicio 2: comparar proporciones de accidentes según grupo y construir un intervalo para la diferencia; antes de comparar dos grupos, practica cada estimación de proporción por separado.
- Los Listados 5 y 6 no son listados de intervalos para proporción.

**Referencia:** [[Clase5_2026.pdf]], sección «Proporción» (PDF, pp. 19–21).

---

## Tema 6 — Diferencia de dos medias con varianzas conocidas

### 1. Resumen

Para comparar las medias `μ_X-μ_Y` de dos poblaciones independientes, con varianzas conocidas `σ_X²` y `σ_Y²`, se centra el intervalo en `X̄-Ȳ`. El error estándar combina la incertidumbre de las dos medias.

### 2. Preguntas

- ¿Las muestras provienen de grupos independientes o son mediciones pareadas?
- ¿Qué diferencia poblacional se pide: `μ_X-μ_Y` o `μ_Y-μ_X`?
- ¿Por qué las varianzas de las medias se suman?
- ¿Qué significa que el intervalo incluya o no incluya cero?

### 3. Profundizar

Para muestras independientes, `Var(X̄-Ȳ)=σ_X²/n+σ_Y²/m`. Las desviaciones estándar no se suman directamente: se combinan las **varianzas** de los estimadores.

Fija el orden de la resta antes de calcular. Cambiar de `μ_X-μ_Y` a `μ_Y-μ_X` cambia el signo de los extremos, no la conclusión sustantiva. Si cero pertenece al intervalo, los datos son compatibles con una diferencia nula al nivel asociado; esto no prueba que las medias sean idénticas.

### 4. Fórmulas a considerar

Para muestras independientes y varianzas conocidas:

$$
(\bar X-\bar Y)-(\mu_X-\mu_Y)
\sim N\left(0,\frac{\sigma_X^2}{n}+\frac{\sigma_Y^2}{m}\right)
$$

$$
\mu_X-\mu_Y\in
\left(
(\bar x-\bar y)-z_{1-\alpha/2}
\sqrt{\frac{\sigma_X^2}{n}+\frac{\sigma_Y^2}{m}},\
(\bar x-\bar y)+z_{1-\alpha/2}
\sqrt{\frac{\sigma_X^2}{n}+\frac{\sigma_Y^2}{m}}
\right)
$$

### 5. Conexión con los ejercicios

- [[Ayudantia_Intervalos_de_Confianza_2.pdf]], ejercicio 1: comparación de medias entre dos tratamientos; identifica si las varianzas poblacionales están especificadas o si deben estimarse.
- Distingue este caso de la comparación pareada del Tema 9: dos grupos de sujetos no implican automáticamente independencia entre todas las observaciones.

**Referencia:** [[Clase5_2026.pdf]], «Dos poblaciones: varianza conocida» (PDF, pp. 23–24).

---

## Tema 7 — Diferencia de dos medias con varianzas desconocidas e iguales

### 1. Resumen

Si las dos muestras son independientes, las poblaciones son normales y sus varianzas desconocidas se suponen iguales, se estima una varianza común agrupando ambas varianzas muestrales. El pivote sigue una t de Student con `n+m-2` grados de libertad.

### 2. Preguntas

- ¿Qué evidencia o supuesto permite tratar las varianzas como iguales?
- ¿Qué información de ambas muestras se incorpora en `S_p²`?
- ¿Por qué los grados de libertad son `n+m-2`?
- ¿Qué supuesto de independencia se necesita entre grupos?

### 3. Profundizar

La varianza agrupada es un promedio ponderado por los grados de libertad, no el promedio simple de `S_X²` y `S_Y²` salvo tamaños apropiados. La raíz `S_p` estima la desviación común.

La igualdad de varianzas es un supuesto del método, no una conclusión automática porque las varianzas muestrales se vean parecidas. Si la igualdad no es razonable, considera el método de varianzas distintas (Tema 8). Para muestras pareadas, usa las diferencias por sujeto (Tema 9).

### 4. Fórmulas a considerar

Varianza agrupada:

$$
S_p^2=
\frac{(n-1)S_X^2+(m-1)S_Y^2}{n+m-2}
$$

Intervalo:

$$
\mu_X-\mu_Y\in
\left(
(\bar x-\bar y)-t_{1-\alpha/2,n+m-2}
S_p\sqrt{\frac1n+\frac1m},\
(\bar x-\bar y)+t_{1-\alpha/2,n+m-2}
S_p\sqrt{\frac1n+\frac1m}
\right)
$$

### 5. Conexión con los ejercicios

- [[Ayudantia_Intervalos_de_Confianza_2.pdf]], ejercicio 1: organiza los resúmenes por grupo y determina si el supuesto de varianzas iguales es defendible antes de usar la fórmula agrupada.
- Si el enunciado no justifica varianzas iguales, no agrupes solo para obtener un resultado.

**Referencia:** [[Clase5_2026.pdf]], «Dos poblaciones: varianzas desconocidas e iguales» (PDF, pp. 25–26).

---

## Tema 8 — Diferencia de dos medias con varianzas desconocidas y distintas

### 1. Resumen

Para dos muestras independientes con varianzas desconocidas que no se suponen iguales, se usa el intervalo de **Welch**. La incertidumbre combina las dos varianzas muestrales y los grados de libertad se aproximan.

### 2. Preguntas

- ¿Qué cambia en el error estándar respecto al caso de varianzas iguales?
- ¿Por qué no se usa una varianza agrupada?
- ¿Los grados de libertad son necesariamente un entero simple `n+m-2`?
- ¿Cuándo conviene elegir Welch en lugar de suponer varianzas iguales?

### 3. Profundizar

Welch permite que los grupos tengan dispersiones y tamaños distintos. El error estándar es la raíz de `S_X²/n+S_Y²/m`. La aproximación de grados de libertad depende de ambas varianzas y tamaños; algunas tablas o programas aceptan grados de libertad no enteros.

La fórmula requiere muestras independientes. Si los datos se midieron sobre las mismas unidades o unidades emparejadas, la estructura de dependencia se aprovecha formando diferencias (Tema 9).

### 4. Fórmulas a considerar

Error estándar:

$$
SE_W=\sqrt{\frac{S_X^2}{n}+\frac{S_Y^2}{m}}
$$

Grados de libertad aproximados de Welch–Satterthwaite:

$$
\nu\approx
\frac{\left(S_X^2/n+S_Y^2/m\right)^2}
{\dfrac{(S_X^2/n)^2}{n-1}
+\dfrac{(S_Y^2/m)^2}{m-1}}
$$

Intervalo:

$$
\mu_X-\mu_Y\in
\left(
(\bar x-\bar y)-t_{1-\alpha/2,\nu}SE_W,\
(\bar x-\bar y)+t_{1-\alpha/2,\nu}SE_W
\right)
$$

### 5. Conexión con los ejercicios

- [[Ayudantia_Intervalos_de_Confianza_2.pdf]], ejercicio 1: compara los tamaños y dispersiones de los grupos antes de elegir entre varianzas iguales o distintas.
- Explica en la resolución por qué escoges Welch o la fórmula agrupada; la elección depende del diseño y del supuesto, no solo de cuál intervalo queda más estrecho.

**Referencia:** [[Clase5_2026.pdf]], «Dos poblaciones: varianzas desconocidas y distintas» (PDF, pp. 26–27).

---

## Tema 9 — Diferencia de medias para muestras pareadas

### 1. Resumen

Las muestras son **pareadas** cuando cada observación de un grupo se vincula naturalmente con una del otro, por ejemplo, antes/después en la misma persona. Se calcula una diferencia `D_i` por pareja y se construye un intervalo para la media de esas diferencias `μ_D`.

### 2. Preguntas

- ¿Cada observación de `X` tiene una pareja específica en `Y`?
- ¿Qué dirección define la diferencia: antes menos después, o después menos antes?
- ¿Cuántas observaciones independientes hay: los sujetos o las dos columnas por separado?
- ¿Cómo afecta la variación dentro de cada pareja a la precisión del intervalo?

### 3. Profundizar

El análisis pareado reduce el problema a una muestra de diferencias. La dependencia entre las dos mediciones queda incorporada en `S_D`; no se deben tratar los dos grupos como independientes.

La interpretación del signo depende del orden de la resta. Si `D=antes-después`, una media positiva indica que la medición antes tiende a ser mayor. Escribe la definición de `D` antes de calcular.

### 4. Fórmulas a considerar

Para `n` diferencias independientes `D_1,…,D_n`:

$$
\bar D=\frac1n\sum_{i=1}^{n}D_i,\qquad
S_D^2=\frac{1}{n-1}\sum_{i=1}^{n}(D_i-\bar D)^2
$$

Intervalo t para la media de las diferencias:

$$
\mu_D\in
\left(
\bar d-t_{1-\alpha/2,n-1}\frac{s_D}{\sqrt n},\
\bar d+t_{1-\alpha/2,n-1}\frac{s_D}{\sqrt n}
\right)
$$

### 5. Conexión con los ejercicios

- [[Ayudantia_Intervalos_de_Confianza_2.pdf]], ejercicio 4, compara los tiempos de la misma rutina antes y después de una reorganización. Las observaciones están emparejadas; trabaja con las diferencias por día.
- Contrástalo con el ejercicio 1 de esa ayudantía, que compara grupos separados.

**Referencia:** [[Clase5_2026.pdf]], «Dos poblaciones: muestras pareadas» (PDF, p. 28).

---

## Tema 10 — Diferencia de dos proporciones

### 1. Resumen

Para comparar las proporciones `p_X-p_Y` en dos poblaciones independientes, se resta la proporción muestral de un grupo menos la del otro. Bajo aproximación normal, el error estándar combina la variabilidad estimada de ambas proporciones.

### 2. Preguntas

- ¿Los grupos son independientes?
- ¿Cuál es el orden de la diferencia y qué significa un valor positivo?
- ¿Cada grupo tiene suficientes éxitos y fracasos para una aproximación normal?
- ¿Se está estimando una diferencia de proporciones o probando una hipótesis de igualdad?

### 3. Profundizar

Para un intervalo de confianza, se estima por separado la varianza de cada proporción y se suman porque las muestras son independientes. No se usa aquí una proporción combinada, que suele aparecer en pruebas de hipótesis bajo la hipótesis nula de igualdad.

Si las proporciones provienen de datos pareados (por ejemplo, respuestas antes/después en los mismos individuos), esta fórmula independiente no corresponde; se necesita un análisis que conserve los pares.

### 4. Fórmulas a considerar

Proporciones muestrales:

$$
\hat p_X=\frac{X}{n},\qquad \hat p_Y=\frac{Y}{m}
$$

Intervalo normal aproximado:

$$
p_X-p_Y\in
\left(
(\hat p_X-\hat p_Y)-z_{1-\alpha/2}
\sqrt{\frac{\hat p_X(1-\hat p_X)}{n}
+\frac{\hat p_Y(1-\hat p_Y)}{m}},\
(\hat p_X-\hat p_Y)+z_{1-\alpha/2}
\sqrt{\frac{\hat p_X(1-\hat p_X)}{n}
+\frac{\hat p_Y(1-\hat p_Y)}{m}}
\right)
$$

Comprueba suficiencia de éxitos y fracasos en cada grupo; como regla aproximada, cada cantidad esperada debe ser al menos 5.

### 5. Conexión con los ejercicios

- [[Ayudantia_Intervalos_de_Confianza_2.pdf]], ejercicio 2, compara proporciones de accidentes entre grupos. Identifica los numeradores de éxitos y los tamaños de muestra antes de usar la fórmula.
- Los PDFs numerados como Listados 5 y 6 (modelos discretos y continuos) no son guías de intervalos para proporciones; estas corresponden a las ayudantías organizadas aquí como Listados 7 y 8.

**Referencia:** [[Clase5_2026.pdf]], «Diferencia de proporciones» (PDF, pp. 21–22 y 26).

---

## Tema 11 — Cociente de dos varianzas

### 1. Resumen

Para comparar las varianzas `σ_X²/σ_Y²` de dos poblaciones normales con muestras independientes, se utiliza la distribución F. El intervalo se basa en el cociente de las varianzas muestrales y en cuantiles F con grados de libertad asociados a cada muestra.

### 2. Preguntas

- ¿Las poblaciones se suponen normales y las muestras independientes?
- ¿Qué cociente se quiere estimar: `σ_X²/σ_Y²` o el inverso?
- ¿Qué grados de libertad corresponden al numerador y al denominador?
- ¿Por qué el orden de los cuantiles importa al formar los extremos?

### 3. Profundizar

El pivote `(S_X²/σ_X²)/(S_Y²/σ_Y²)` sigue una distribución F bajo normalidad e independencia. Al despejar el cociente poblacional, el intervalo puede expresarse como el cociente muestral dividido por cuantiles F; el cuantil superior va en el extremo inferior.

La distribución F es asimétrica y depende del orden de sus dos grados de libertad. Si inviertes el cociente de varianzas, también cambian el orden y los grados de libertad. Este intervalo es sensible a desviaciones de normalidad.

### 4. Fórmulas a considerar

Pivote:

$$
\frac{S_X^2/S_Y^2}{\sigma_X^2/\sigma_Y^2}
\sim F_{n-1,m-1}
$$

Si `F_{γ;ν1,ν2}` es el cuantil de cola izquierda `γ`:

$$
\frac{\sigma_X^2}{\sigma_Y^2}\in
\left(
\frac{s_X^2/s_Y^2}{F_{1-\alpha/2;n-1,m-1}},\
\frac{s_X^2/s_Y^2}{F_{\alpha/2;n-1,m-1}}
\right)
$$

### 5. Conexión con los ejercicios

- Las dos ayudantías permiten practicar cómo reconocer si se comparan medias, proporciones o dispersiones. Revisa el parámetro que pregunta cada enunciado: un intervalo para diferencia de medias no informa directamente sobre el cociente de varianzas.
- No atribuyas a los Listados 5 o 6 un ejercicio de cociente de varianzas sin confirmarlo en el enunciado.

**Referencia:** [[Clase5_2026.pdf]], «Intervalos de confianza para cociente de varianzas» (PDF, pp. 29–30).

---

## Guía para elegir el intervalo

| Pregunta | Diseño / información | Método de esta clase |
|---|---|---|
| Una media `μ` | `σ` poblacional conocida | Normal `z` |
| Una media `μ` | `σ` desconocida, una muestra | Student `t`, `n-1` g.l. |
| Una varianza `σ²` | Una población normal | Chi-cuadrado |
| Una proporción `p` | Bernoulli, aproximación normal válida | Normal `z` |
| Diferencia de medias | Dos muestras independientes, varianzas conocidas | Normal `z` |
| Diferencia de medias | Dos muestras independientes, varianzas desconocidas e iguales | t agrupada |
| Diferencia de medias | Dos muestras independientes, varianzas desconocidas y distintas | Welch |
| Cambio medio | Mediciones pareadas | t sobre diferencias |
| Diferencia de proporciones | Dos muestras independientes | Normal `z` |
| Cociente de varianzas | Poblaciones normales, muestras independientes | F |

## Errores que conviene evitar

- Interpretar el nivel de confianza como probabilidad posterior de que el parámetro fijo esté dentro de un intervalo ya calculado.
- Confundir `σ` poblacional con `s` muestral; esto cambia el pivote `z`/`t`.
- Usar `n` grados de libertad en lugar de `n-1` para una sola muestra t.
- Confundir varianza y desviación estándar, o entregar un intervalo para `σ²` cuando se pide `σ`.
- Invertir los cuantiles chi-cuadrado o F al despejar el parámetro.
- Aplicar la fórmula normal para proporciones con pocos éxitos o fracasos.
- Tratar muestras pareadas como independientes o invertir el signo sin cambiar la interpretación.
- Usar varianza agrupada sin suponer varianzas poblacionales iguales.
- Usar la fórmula de Welch para datos pareados.
- Leer cuantiles de una tabla sin comprobar si son de cola izquierda o derecha.
- Informar solo el intervalo sin explicar qué parámetro y qué población representa.

## Ruta de resolución para cualquier intervalo

1. **Traduce la pregunta:** identifica el parámetro y sus unidades.
2. **Identifica el diseño:** una muestra, dos independientes o pareadas; conteo/proporción o medición continua.
3. **Registra la información conocida:** `σ`, `s`, proporciones, normalidad, igualdad de varianzas y tamaño muestral.
4. **Elige el pivote y los grados de libertad** según ese diseño.
5. **Determina `α` y el cuantil:** para confianza bilateral `1-α`, busca `1-α/2`.
6. **Calcula estimador, error estándar y margen de error.**
7. **Escribe ambos extremos** en el orden correcto.
8. **Interpreta el intervalo** en contexto y revisa signos, unidades y supuestos.

## Sobre los listados disponibles

Los Listados 7 y 8 corresponden a las ayudantías de intervalos de confianza: [[Ayudantia_Intervalos_de_Confianza.pdf]] y [[Ayudantia_Intervalos_de_Confianza_2.pdf]]. La primera portada conserva la numeración «Listado 6» del PDF original. Sus desarrollos están en [[Solucionario - Listado 7]] y [[Solucionario - Listado 8]]. Conviene intentar primero los ejercicios sin mirar soluciones y anotar qué supuesto te hizo elegir cada método.
