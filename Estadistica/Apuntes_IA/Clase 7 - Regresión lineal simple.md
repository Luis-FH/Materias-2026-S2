---
seguimiento_certamen2: true
bloque_certamen2: "Regresión"
progreso_certamen2: false
---

# Clase 7 — Regresión lineal simple: guía completa

#certamen2_estadistica

> [!info] Fuentes y conexiones
> - [[Clase7_2026_regre_lineal_simple_2026.pdf]] — presentación «Regresión Lineal Simple» (6 páginas).
> - [[Listado 10 523250 E y P_II_2026.pdf]] — ejercicio 1 practica la recta estimada, una predicción y la calidad del ajuste; el ejercicio 2 introduce modelos con varias variables.
> - [[Solucionario - Listado 10]] — resolución del ejercicio 1 y análisis de modelos del ejercicio 2.
> - La regresión múltiple se aborda en el material de la Clase 8; el Listado 10 contiene ejercicios de ambos temas.
> - Índice del ramo: Estadística.

## Mapa de la clase

La regresión lineal simple describe cómo cambia una variable respuesta `Y` al variar una variable explicativa `X`, mediante una recta. La clase presenta el modelo probabilístico, la estimación de sus parámetros, la recta ajustada, la correlación, el coeficiente de determinación y un ejemplo con predicción.

`definir X e Y → explorar los datos → estimar intercepto y pendiente → obtener la recta → evaluar asociación y ajuste → predecir con cautela`

En cada tema se sigue: **1. resumen → 2. preguntas → 3. profundizar → 4. fórmulas → 5. conexión con ejercicios**.

### Notación

- `X`: variable explicativa o predictora; `Y`: variable respuesta.
- `β₁`: intercepto poblacional; `β₂`: pendiente poblacional.
- `β̂₁`, `β̂₂`: estimaciones muestrales del intercepto y la pendiente.
- `εᵢ`: error aleatorio de la observación `i`; `σ²`: varianza de esos errores.
- `Ŷᵢ = β̂₁ + β̂₂xᵢ`: respuesta ajustada para `xᵢ`.
- `ȳ`, `x̄`: medias muestrales; `r`: correlación muestral; `R²`: coeficiente de determinación.
- `n`: número de pares observados `(xᵢ,yᵢ)`.

---

## Tema 1 — El modelo de regresión lineal simple

### 1. Resumen

El modelo relaciona una respuesta continua `Y` con una sola variable explicativa `X`. Para cada valor `xᵢ`, la respuesta tiene una media lineal `β₁+β₂xᵢ` y una variación aleatoria alrededor de esa media:

$$
Y_i=\beta_1+\beta_2x_i+\varepsilon_i
$$

La recta representa la tendencia promedio; no afirma que todas las observaciones caigan exactamente sobre ella.

### 2. Preguntas

- ¿Cuál variable se quiere explicar o predecir (`Y`)?
- ¿Cuál variable se usa como explicativa (`X`)?
- ¿Tiene sentido sustantivo suponer una tendencia aproximadamente lineal?
- ¿Las observaciones corresponden a pares relacionados y son independientes entre sí?
- ¿Se está interpretando una asociación o se pretende afirmar causalidad?

### 3. Profundizar

La presentación plantea que los valores de `X` se consideran dados y que las respuestas son independientes, con distribución normal y varianza común:

$$
Y_i\sim N(\beta_1+\beta_2x_i,\sigma^2)
$$

Así, para cada `xᵢ`, la media de `Yᵢ` está sobre la recta y la dispersión alrededor de ella tiene varianza `σ²`. Las condiciones habituales para una inferencia confiable incluyen independencia, relación media aproximadamente lineal, varianza constante y distribución aproximadamente normal de los errores para muestras pequeñas. Conviene revisar gráficos de dispersión y residuos: una recta no repara curvatura, grupos, valores atípicos ni dependencia.

Una asociación lineal tampoco demuestra que `X` cause cambios en `Y`; puede haber variables omitidas, confusión o una dirección causal distinta.

### 4. Fórmulas a considerar

$$
Y_i=\beta_1+\beta_2x_i+\varepsilon_i,\qquad
\varepsilon_i\ \text{independientes con }E(\varepsilon_i)=0,\ 
\operatorname{Var}(\varepsilon_i)=\sigma^2
$$

Forma equivalente de la media condicional:

$$
E(Y_i\mid X=x_i)=\beta_1+\beta_2x_i
$$

El modelo normal presentado en clase añade `εᵢ ~ N(0,σ²)`.

### 5. Conexión con ejercicios

- [[Clase7_2026_regre_lineal_simple_2026.pdf]], pp. 2–3: notación, modelo y estimación.
- En el ejercicio 1 de [[Listado 10 523250 E y P_II_2026.pdf]], identifica experiencia laboral como `X` y salario como `Y`. Comprueba que esa elección responde a la pregunta planteada.
- La exploración gráfica y los resúmenes de datos ayudan a recordar por qué se debe mirar la nube de puntos antes de resumirla con una recta.

---

## Tema 2 — Interpretar intercepto y pendiente

### 1. Resumen

En `β₁+β₂x`, el intercepto `β₁` es la respuesta media del modelo cuando `X=0`. La pendiente `β₂` indica cuánto cambia la respuesta media cuando `X` aumenta una unidad. La interpretación debe conservar las unidades y el contexto.

### 2. Preguntas

- ¿Qué significa que `X` aumente una unidad en el problema?
- ¿En qué unidades se mide `Y` y, por tanto, la pendiente?
- ¿`X=0` tiene sentido y está dentro del rango observado?
- ¿El intercepto describe un caso real o es solo necesario para posicionar la recta?
- ¿La pendiente expresa cambio promedio o cambio exacto para cada individuo?

### 3. Profundizar

Si `β̂₂=0.893`, el ajuste estima que la respuesta media aumenta `0.893` unidades de `Y` por cada unidad adicional de `X`. No significa que cada persona o tienda aumente exactamente esa cantidad.

El intercepto se interpreta como respuesta media en `X=0`, pero puede no ser útil si cero queda fuera del rango muestral o no representa una situación posible. La pendiente describe asociación en la escala elegida y no debe presentarse como causal sin un diseño que justifique esa conclusión.

### 4. Fórmulas a considerar

Recta poblacional media:

$$
E(Y\mid X=x)=\beta_1+\beta_2x
$$

Cambio en la respuesta media entre `x` y `x+Δx`:

$$
\Delta E(Y\mid X)=\beta_2\Delta x
$$

Unidades:

$$
[\beta_1]=[Y],\qquad [\beta_2]=\frac{[Y]}{[X]}
$$

### 5. Conexión con ejercicios

- En el ejercicio 1 del [[Listado 10 523250 E y P_II_2026.pdf]], describe la pendiente estimada con las unidades de salario y años de experiencia antes de calcular la predicción.
- El ejemplo de la presentación estima una recta entre número de técnicos comerciales y unidades vendidas por semana; interpreta la pendiente en «aparatos por técnico» y dentro de ese contexto ([[Clase7_2026_regre_lineal_simple_2026.pdf]], p. 6).

---

## Tema 3 — Estimación de la recta por mínimos cuadrados

### 1. Resumen

Los parámetros desconocidos `β₁` y `β₂` se estiman con la muestra. El método de mínimos cuadrados elige la recta que minimiza la suma de los cuadrados de los residuos, es decir, de las diferencias entre cada respuesta observada y su valor ajustado.

### 2. Preguntas

- ¿Qué es un residuo y cómo se diferencia de un valor ajustado?
- ¿Por qué se elevan los residuos al cuadrado?
- ¿La recta estimada pasa por `(x̄,ȳ)`?
- ¿Qué ocurre con la pendiente si las variables están asociadas positivamente o negativamente?
- ¿Cuál es la diferencia entre estimar `β₂` y calcular una predicción `Ŷ`?

### 3. Profundizar

Para cada par de datos, el residuo es `eᵢ=yᵢ-ŷᵢ`. Los residuos positivos indican que la respuesta observada está por encima de la recta; los negativos, por debajo. Al cuadrarlos, los errores positivos y negativos no se cancelan y las desviaciones grandes reciben más peso.

La recta de mínimos cuadrados con intercepto pasa por el centro de los datos `(x̄,ȳ)`. Bajo el modelo de clase, los estimadores de mínimos cuadrados coinciden con los de máxima verosimilitud para los parámetros de la recta cuando se asumen errores normales. La varianza residual se estima utilizando `n-2` grados de libertad porque se estimaron dos parámetros.

### 4. Fórmulas a considerar

Define:

$$
S_{xx}=\sum_{i=1}^{n}(x_i-\bar x)^2,\qquad
S_{xy}=\sum_{i=1}^{n}(x_i-\bar x)(y_i-\bar y)
$$

Estimadores:

$$
\hat\beta_2=\frac{S_{xy}}{S_{xx}},\qquad
\hat\beta_1=\bar y-\hat\beta_2\bar x
$$

Forma computacional equivalente para la pendiente:

$$
\hat\beta_2=
\frac{\sum x_i y_i-n\bar x\bar y}
{\sum x_i^2-n\bar x^2}
$$

Recta estimada, valores ajustados y residuos:

$$
\hat y_i=\hat\beta_1+\hat\beta_2x_i,\qquad
e_i=y_i-\hat y_i
$$

Estimación insesgada de la varianza del error:

$$
s^2=\frac{\sum_{i=1}^{n}(y_i-\hat y_i)^2}{n-2}
=\frac{\sum e_i^2}{n-2}
$$

### 5. Conexión con ejercicios

- [[Clase7_2026_regre_lineal_simple_2026.pdf]], p. 3, entrega los estimadores y la estimación de `σ²`.
- En el ejercicio 1 del [[Listado 10 523250 E y P_II_2026.pdf]], usa las sumas proporcionadas para obtener `x̄`, `ȳ`, `Sxx` y `Sxy`; luego calcula primero la pendiente y después el intercepto.
- Comprueba que la recta calculada pasa por `(x̄,ȳ)` y que los residuos de mínimos cuadrados suman aproximadamente cero (salvo redondeo).

---

## Tema 4 — Correlación y asociación lineal

### 1. Resumen

El coeficiente de correlación mide la dirección y fuerza de la asociación lineal entre dos variables. Sus valores están entre `-1` y `1`: el signo indica dirección y la magnitud indica qué tan cerca está la asociación de una línea recta.

### 2. Preguntas

- ¿`r` es positivo, negativo o cercano a cero?
- ¿Qué indica su magnitud sobre la asociación lineal?
- ¿Hay valores atípicos que influyan fuertemente en `r`?
- Si `r=0`, ¿se puede concluir que no existe ninguna relación entre `X` e `Y`?
- ¿Cambiar las unidades de medición modifica el valor de `r`?

### 3. Profundizar

`r=1` o `r=-1` corresponde a asociación lineal perfecta en la muestra; `r=0` indica ausencia de asociación lineal muestral, pero aún puede existir una relación curva u otra dependencia. Por ello, `r` debe interpretarse junto con el gráfico de dispersión.

La correlación es simétrica: `r(X,Y)=r(Y,X)`. La regresión no es simétrica, pues el ajuste de `Y` sobre `X` depende de cuál variable se define como respuesta. La correlación por sí sola no distingue predictor y respuesta ni demuestra causalidad.

### 4. Fórmulas a considerar

$$
r=
\frac{\sum_{i=1}^{n}(x_i-\bar x)(y_i-\bar y)}
{\sqrt{\sum_{i=1}^{n}(x_i-\bar x)^2
\sum_{i=1}^{n}(y_i-\bar y)^2}}
$$

Con las sumas centradas abreviadas:

$$
r=\frac{S_{xy}}{\sqrt{S_{xx}S_{yy}}},
\qquad -1\le r\le 1
$$

### 5. Conexión con ejercicios

- [[Clase7_2026_regre_lineal_simple_2026.pdf]], p. 4, presenta `r`, su interpretación y la recta ajustada.
- En el ejercicio 1 del [[Listado 10 523250 E y P_II_2026.pdf]], la pregunta sobre calidad del ajuste se relaciona con `r` y `R²`, pero interpreta también la nube de puntos y el propósito de la predicción.
- La presentación ilustra asociaciones perfectas positivas y negativas y ausencia de asociación lineal; compáralas con posibles patrones curvos antes de generalizar lo que significa `r=0` (p. 4).

---

## Tema 5 — Coeficiente de determinación `R²`

### 1. Resumen

`R²` resume qué fracción de la variabilidad observada de `Y` queda explicada por la recta ajustada en la muestra. En regresión lineal simple con intercepto, `R²=r²`; se encuentra entre 0 y 1.

### 2. Preguntas

- ¿Qué porcentaje de variabilidad de `Y` corresponde a `R²=0.817`?
- ¿`R²` alto prueba que el modelo es correcto o causal?
- ¿Un valor alto garantiza que las predicciones fuera del rango observado sean confiables?
- ¿Qué información se pierde al elevar `r` al cuadrado?
- ¿Se revisaron residuos, linealidad y valores influyentes además de `R²`?

### 3. Profundizar

En el modelo simple con intercepto, `R²` se puede leer como proporción de variabilidad muestral de `Y` explicada por su relación lineal con `X`. Por ejemplo, `R²=0.817` equivale a 81.7% de la variabilidad en la muestra; no significa que la predicción tenga un 81.7% de probabilidad de ser correcta ni que `X` cause ese porcentaje de `Y`.

Al cuadrar la correlación, `R²` no conserva la dirección de la asociación: una correlación negativa también puede producir un `R²` alto. Además, un `R²` grande no detecta por sí solo curvatura, puntos influyentes ni una mala extrapolación.

### 4. Fórmulas a considerar

En regresión simple con intercepto:

$$
R^2=r^2
$$

Descomposición de sumas de cuadrados:

$$
SST=\sum(y_i-\bar y)^2,\qquad
SSE=\sum(y_i-\hat y_i)^2,\qquad
R^2=1-\frac{SSE}{SST}
$$

En este caso `SST` mide variabilidad total y `SSE` la variabilidad residual. Porcentaje asociado al ajuste lineal: `100R²%`.

### 5. Conexión con ejercicios

- [[Clase7_2026_regre_lineal_simple_2026.pdf]], p. 5, ilustra varios niveles de `R²`; la p. 6 calcula `r=0.904` y `R²=0.817` para el ejemplo de ventas.
- En el ejercicio 1(c) del [[Listado 10 523250 E y P_II_2026.pdf]], evalúa el ajuste con el criterio pedido y explica `R²` como proporción de variabilidad muestral, no como causalidad.

---

## Tema 6 — Predicción, ajuste y límites de uso

### 1. Resumen

Una vez estimada la recta, se sustituye un valor de `X` para obtener una respuesta media estimada. La predicción es más defendible dentro del rango de `X` observado; fuera de él se extrapola y el patrón lineal puede dejar de ser válido.

### 2. Preguntas

- ¿El valor de `X` para el que se predice está dentro del rango muestral?
- ¿La pregunta solicita una respuesta media o el resultado de una observación individual?
- ¿Las unidades de la predicción son las mismas que las de `Y`?
- ¿El valor ajustado es una predicción exacta o una estimación con incertidumbre?
- ¿La asociación observada permite una conclusión causal?

### 3. Profundizar

La predicción `ŷ=β̂₁+β̂₂x` estima la media de la respuesta en `X=x`; una observación individual también contiene error aleatorio alrededor de esa media. Por tanto, en general hay más incertidumbre al predecir un individuo que al estimar la media condicional.

La presentación ejemplifica una recta `ŷ=100.536+0.893x`, calcula una predicción y evalúa el ajuste (`r=0.904`, `R²=0.817`). Esa recta corresponde al ejemplo de tiendas y ventas de la diapositiva, no a los datos del ejercicio 1 del Listado 10: no mezcles coeficientes de ejemplos distintos.

Antes de usar una predicción, revisa el rango de datos, el gráfico y los supuestos. La clase presenta el ajuste y la predicción puntual, pero no desarrolla aquí intervalos de predicción ni pruebas de significación para la pendiente.

### 4. Fórmulas a considerar

Predicción puntual en `x₀`:

$$
\hat y(x_0)=\hat\beta_1+\hat\beta_2x_0
$$

Residuo para una observación:

$$
e_i=y_i-\hat y_i
$$

El residuo es una discrepancia observada en la muestra; no debe confundirse con el error poblacional no observado `εᵢ`.

### 5. Conexión con ejercicios

- El ejemplo y la predicción aparecen en [[Clase7_2026_regre_lineal_simple_2026.pdf]], p. 6.
- El ejercicio 1(b) del [[Listado 10 523250 E y P_II_2026.pdf]] pide estimar el salario mensual para una experiencia dada; utiliza la recta que calculaste en 1(a), sustituye ese valor de `X` y reporta las unidades.
- El ejercicio 1(c) pide evaluar la calidad del ajuste. Distingue esa evaluación de la predicción individual y explica el alcance de la asociación observada.
- El ejercicio 2 del Listado 10 incluye varias características explicativas y corresponde a regresión múltiple, no a las fórmulas de regresión simple de esta nota.

---

## Ruta corta para resolver un ejercicio

1. Define qué variable es la respuesta `Y` y cuál es la explicativa `X`; conserva sus unidades.
2. Grafica o inspecciona los pares para juzgar si una relación lineal es razonable y detectar valores atípicos.
3. Calcula `x̄`, `ȳ`, `Sxx` y `Sxy`.
4. Obtén `β̂₂=Sxy/Sxx` y `β̂₁=ȳ-β̂₂x̄`.
5. Escribe e interpreta `ŷ=β̂₁+β̂₂x`.
6. Calcula `r` y `R²` cuando se solicite y explica qué describen.
7. Para predecir, sustituye el valor pedido en la recta, verifica si está dentro del rango observado y reporta las unidades.
8. Concluye en contexto sin confundir asociación con causalidad ni ajuste con certeza predictiva.

## Errores frecuentes

- Intercambiar `X` e `Y`: la recta de `Y` sobre `X` no es la misma que la de `X` sobre `Y`.
- Interpretar la pendiente como cambio exacto de cada observación en vez de cambio promedio estimado.
- Dar significado real al intercepto aunque `X=0` no sea posible o esté fuera del rango de datos.
- Concluir que `r=0` significa que no existe relación de ningún tipo.
- Confundir `R²` con una probabilidad, una medida causal o un indicador completo de validez del modelo.
- Usar una recta para extrapolar lejos de las observaciones.
- Mezclar la recta del ejemplo de la clase con los datos del Listado 10.
- Suponer que una predicción puntual no tiene error.

## Conexiones dentro del ramo

- Exploración gráfica y descripción inicial de datos → revisión de la nube de puntos antes del ajuste.
- Intervalos de confianza y pruebas de hipótesis → inferencia que amplía la estimación descriptiva; esta clase no desarrolla esos procedimientos.
- Regresión múltiple → extensión a más de una variable explicativa.
- [[Listado 10 523250 E y P_II_2026.pdf]] → ejercicio 1 de regresión simple; ejercicio 2 se conecta con regresión múltiple.
