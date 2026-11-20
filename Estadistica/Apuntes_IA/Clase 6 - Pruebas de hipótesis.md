---
seguimiento_certamen2: true
bloque_certamen2: "Pruebas de hipótesis"
progreso_certamen2: false
---

# Clase 6 — Pruebas de hipótesis: guía completa

#certamen2_estadistica

> [!info] Fuentes y conexiones
> - [[Clase6_2026.pdf]] — presentación «Test de Hipótesis» (9 páginas).
> - [[Resumen_Prueba_de_Hipótesis.pdf]] — material complementario de fundamentos y casos aplicados.
> - [[Listado 9 523250 E y P_II_2026.pdf]] — ejercicios de pruebas de hipótesis y comparación de proporciones.
> - [[Solucionario - Listado 9]] — resolución paso a paso.
> - Índice del ramo: Estadística.

## Mapa de la clase

Una prueba de hipótesis usa una muestra para evaluar una afirmación acerca de un parámetro poblacional. El resultado no demuestra que una hipótesis sea cierta: indica si la muestra entrega evidencia suficiente para rechazar la hipótesis nula bajo un nivel de significación elegido.

`pregunta → parámetro y supuestos → H₀/H₁ → α y estadístico → región crítica o valor-p → decisión → conclusión contextual`

La presentación recorre la formulación de hipótesis, las cuatro etapas de una prueba, la región crítica, el valor-p, los errores tipo I y II y pruebas para distintos parámetros. En cada tema se sigue: **1. resumen → 2. preguntas → 3. profundizar → 4. fórmulas → 5. conexión con material y ejercicios**.

### Notación

- `H₀`: hipótesis nula; `H₁`: hipótesis alternativa.
- `α`: nivel de significación, que fija la probabilidad máxima tolerada de error tipo I bajo el modelo.
- `β`: probabilidad de error tipo II para un valor alternativo concreto; `1-β` es la potencia.
- `θ₀`: valor del parámetro propuesto por la hipótesis nula.
- `X̄`, `S²`, `S`, `p̂`: media, varianza, desviación estándar y proporción muestrales.
- `Δ₀`: diferencia de parámetros especificada en `H₀` (a menudo, pero no siempre, es 0).
- `z_γ`: cuantil de cola izquierda de la normal estándar, con probabilidad acumulada `γ`.

---

## Tema 1 — ¿Qué pregunta responde una prueba de hipótesis?

### 1. Resumen

Una prueba permite evaluar si los datos muestrales son compatibles con una afirmación sobre una población. Se parte de una hipótesis nula `H₀` y se la contrasta con una alternativa `H₁`. La prueba considera qué resultados serían esperables si `H₀` fuera cierta.

### 2. Preguntas

- ¿Cuál es la población y cuál es el parámetro que se está estudiando?
- ¿Qué valor o afirmación concreta se plantea en `H₀`?
- ¿Qué cambio, diferencia o dirección plantea `H₁`?
- ¿La muestra y el modelo cumplen los supuestos del procedimiento elegido?
- ¿Qué conclusión práctica se necesita responder, más allá de «rechazar» o «no rechazar»?

### 3. Profundizar

`H₀` suele expresar el valor de referencia, igualdad o ausencia de cambio que se evalúa. `H₁` representa la afirmación para la cual se busca evidencia. Los datos no asignan una probabilidad a que `H₀` sea verdadera; se calcula cuán inusual sería el resultado muestral suponiendo `H₀`.

La conclusión tiene dos posibilidades: **rechazar `H₀`** o **no rechazar `H₀`**. No rechazarla no demuestra que sea cierta ni equivale a aceptarla: puede que la muestra no tenga suficiente información para distinguirla de la alternativa.

### 4. Fórmulas a considerar

Esquema de hipótesis para un parámetro `θ`:

$$
H_0:\theta=\theta_0
\qquad\text{frente a}\qquad
H_1:\theta\ne\theta_0,\ \theta>\theta_0\ \text{o}\ \theta<\theta_0
$$

La forma de `H₀` puede escribirse como una igualdad en el valor frontera que se usa para calcular el estadístico. En una prueba unilateral, la hipótesis nula completa también comprende los valores al otro lado de esa frontera.

### 5. Conexión con ejercicios

- La presentación introduce el propósito de inferir sobre parámetros y la toma de decisiones en [[Clase6_2026.pdf]] (p. 2).
- Antes de calcular, escribe con palabras la afirmación del problema y tradúcela al parámetro. Los intervalos de confianza ayudan a reconocer parámetros como `μ`, `σ²`, `p` y diferencias entre poblaciones.
- Para practicar pruebas de hipótesis y comparación de proporciones, revisa [[Listado 9 523250 E y P_II_2026.pdf]] y [[Solucionario - Listado 9]]. El Listado 6 corresponde a modelos continuos, no a contrastes.

---

## Tema 2 — Hipótesis bilaterales y unilaterales

### 1. Resumen

La alternativa determina qué resultados cuentan como evidencia contra `H₀`:

- **Bilateral:** interesa cualquier diferencia respecto del valor de referencia.
- **Unilateral derecha:** interesa que el parámetro sea mayor.
- **Unilateral izquierda:** interesa que sea menor.

La dirección debe decidirse a partir de la pregunta de investigación, antes de observar el resultado.

### 2. Preguntas

- ¿El enunciado pregunta si el parámetro «cambió» o especifica que «aumentó»/«disminuyó»?
- ¿La región de rechazo debe quedar en una cola o en ambas?
- Si el resultado observado apunta en la dirección opuesta a la esperada, ¿la prueba unilateral lo considera evidencia a favor de `H₁`?
- ¿Se eligió la dirección antes de mirar los datos?

### 3. Profundizar

Una prueba bilateral reparte el nivel `α` entre las dos colas, normalmente `α/2` por cola en una distribución simétrica. En una prueba unilateral, toda la probabilidad de rechazo se ubica en la cola indicada por `H₁`.

No se debe cambiar de una prueba bilateral a una unilateral después de ver los datos para conseguir significación. Tampoco basta con que una muestra tenga una media mayor: la decisión depende de cuánto se aparta el estadístico de lo esperado por variabilidad muestral.

### 4. Fórmulas a considerar

$$
\begin{array}{ll}
\text{Bilateral:} & H_0:\theta=\theta_0,\quad H_1:\theta\ne\theta_0 \\
\text{Cola derecha:} & H_0:\theta\le\theta_0,\quad H_1:\theta>\theta_0 \\
\text{Cola izquierda:} & H_0:\theta\ge\theta_0,\quad H_1:\theta<\theta_0
\end{array}
$$

Para un estadístico simétrico `Z ~ N(0,1)`, las regiones críticas son:

$$
\begin{array}{ll}
\text{Bilateral:} & |Z|>z_{1-\alpha/2} \\
\text{Cola derecha:} & Z>z_{1-\alpha} \\
\text{Cola izquierda:} & Z<z_{\alpha}
\end{array}
$$

Los cuantiles y regiones cambian si el estadístico sigue otra distribución, como `t`, `χ²` o `F`.

### 5. Conexión con ejercicios

- La primera etapa de [[Clase6_2026.pdf]] distingue contrastes bilaterales y unilaterales (p. 3).
- En cualquier ejercicio, subraya la expresión que determina la dirección. No conviertas «es distinto» en «es mayor» solo porque el promedio observado aumentó.
- La guía [[Resumen_Prueba_de_Hipótesis.pdf]] complementa la formulación y aplicación de pruebas.

---

## Tema 3 — Las etapas de una prueba y la región crítica

### 1. Resumen

La clase organiza la prueba en cuatro etapas:

1. Formular `H₀` y `H₁`.
2. Fijar el criterio de prueba: `α`, estadístico y región crítica.
3. Obtener la muestra y calcular el estadístico.
4. Comparar el resultado con la región crítica y concluir.

La región crítica contiene los resultados del estadístico que llevan a rechazar `H₀`.

### 2. Preguntas

- ¿Se establecieron `H₀`, `H₁` y `α` antes de calcular?
- ¿Cuál es la distribución del estadístico bajo `H₀`?
- ¿La región crítica tiene una o dos colas?
- ¿Se rechaza porque el estadístico cae en esa región, o se está usando otro criterio?
- ¿La conclusión responde la pregunta original en contexto?

### 3. Profundizar

El estadístico convierte la diferencia entre lo observado y lo propuesto por `H₀` en unidades de error estándar. Un valor extremo indica que el resultado sería poco habitual si `H₀` fuera cierta. La región crítica se determina con la distribución del estadístico bajo `H₀` y con el nivel `α`.

El nivel de significación se fija antes de observar la muestra. Si el estadístico cae en la región crítica, se rechaza `H₀`; si no cae, no se rechaza. Los supuestos (por ejemplo, independencia, normalidad o tamaño muestral) forman parte del método: una fórmula correcta aplicada a un diseño inadecuado puede llevar a una conclusión no confiable.

### 4. Fórmulas a considerar

Esquema de un estadístico estandarizado:

$$
\text{estadístico de prueba}
=
\frac{\text{estimador observado}-\text{valor especificado por }H_0}
{\text{error estándar bajo }H_0}
$$

Para una prueba de cola derecha de nivel `α`, se rechaza si el estadístico supera el cuantil `1-α`; para una prueba bilateral simétrica se rechaza si su valor absoluto supera el cuantil `1-α/2`. La distribución de referencia puede ser normal, t de Student, chi-cuadrado o F.

### 5. Conexión con ejercicios

- Las etapas 1 a 4 aparecen en [[Clase6_2026.pdf]] (pp. 3–5).
- Practica escribiendo primero la regla de decisión y después sustituyendo los datos. Así evitas escoger la cola o el cuantil a conveniencia del resultado.
- Para un ejercicio todavía no resuelto, registra: parámetro, diseño, supuestos, hipótesis, estadístico, región crítica, decisión y conclusión contextual.

---

## Tema 4 — Estadístico de prueba según el parámetro

### 1. Resumen

El estimador y su error estándar dependen del parámetro y del diseño. La clase enumera pruebas para una media, una varianza, una proporción, diferencias de medias y proporciones y un cociente de varianzas. En dos muestras, primero hay que decidir si son independientes o pareadas; para medias independientes también importa si las varianzas son conocidas, iguales o distintas.

### 2. Preguntas

- ¿Se contrasta un parámetro de una población o una diferencia/cociente entre dos?
- ¿Las observaciones de las dos muestras son independientes o están emparejadas?
- ¿Se conoce `σ`, o se estima con `S`?
- ¿Qué distribución tiene el estadístico bajo `H₀`?
- ¿Se cumplen las condiciones para usar una aproximación normal o el supuesto de población normal?

### 3. Profundizar

La tabla siguiente es un mapa de los estadísticos habituales para contrastes en los que se prueba el valor nulo indicado. Los procedimientos exactos pueden tener condiciones adicionales; verifica siempre la fórmula de la asignatura y los supuestos del enunciado.

| Parámetro y diseño | Estadístico bajo `H₀` | Referencia y condiciones principales |
|---|---|---|
| Una media `μ`, `σ` conocida | `Z=(X̄-μ₀)/(σ/√n)` | Normal estándar; muestra aleatoria, y población normal o aproximación justificada. |
| Una media `μ`, `σ` desconocida | `T=(X̄-μ₀)/(S/√n)` | `t` con `n-1` grados de libertad; muestra de población normal para resultado exacto. |
| Varianza `σ²` | `χ²=(n-1)S²/σ₀²` | Chi-cuadrado con `n-1` grados de libertad; población normal. |
| Proporción `p` | `Z=(p̂-p₀)/√(p₀(1-p₀)/n)` | Normal aproximada; las cantidades esperadas de éxitos y fracasos bajo `H₀` deben ser suficientes. |
| Diferencia de medias pareadas | `T=(D̄-Δ₀)/(S_D/√n_D)` | `t` con `n_D-1` grados de libertad; se analiza una muestra de diferencias `D`. |
| Diferencia de medias independientes, `σ₁`,`σ₂` conocidas | `Z=(X̄₁-X̄₂-Δ₀)/√(σ₁²/n₁+σ₂²/n₂)` | Normal estándar bajo los supuestos de muestreo y modelo. |
| Diferencia de medias independientes, varianzas desconocidas e iguales | `T=(X̄₁-X̄₂-Δ₀)/(S_p√(1/n₁+1/n₂))` | `t` con `n₁+n₂-2` grados de libertad; varianzas poblacionales iguales. `S_p²=[(n₁-1)S₁²+(n₂-1)S₂²]/(n₁+n₂-2)`. |
| Diferencia de medias independientes, varianzas desconocidas y distintas | `T=(X̄₁-X̄₂-Δ₀)/√(S₁²/n₁+S₂²/n₂)` | Prueba de Welch; los grados de libertad se aproximan con una fórmula específica. |
| Cociente de varianzas de poblaciones normales | `F=(S₁²/S₂²)/(σ₁²/σ₂²)_0` | F con `n₁-1` y `n₂-1` grados de libertad; muestras independientes y poblaciones normales. |
| Diferencia de proporciones, `H₀:p₁-p₂=0` | `Z=(p̂₁-p̂₂)/√(p̂(1-p̂)(1/n₁+1/n₂))` | Normal aproximada; `p̂=(x₁+x₂)/(n₁+n₂)` es la proporción combinada bajo igualdad. |

En una prueba pareada, `n_D` es el número de pares y `S_D` la desviación estándar de las diferencias. Para pruebas de proporciones y diferencias de proporciones con valores nulos distintos de cero, no reutilices automáticamente la fórmula de igualdad: consulta el método específico.

### 4. Fórmulas a considerar

Como patrón, muchos estadísticos para medias y proporciones comparan un estimador con el valor bajo `H₀` y lo dividen por el error estándar calculado bajo esa hipótesis. Las pruebas de varianzas emplean pivotes chi-cuadrado o F.

Para dos medias pareadas, define primero `D_i=X_i-Y_i`; la prueba se realiza sobre `μ_D`, no como si fueran dos muestras independientes. Para dos medias independientes con varianzas desconocidas distintas, el estadístico de Welch no debe sustituirse por el de varianzas iguales sin justificación.

### 5. Conexión con ejercicios

- La lista de parámetros de la presentación aparece en [[Clase6_2026.pdf]] (p. 7); la p. 8 indica que las pruebas se especifican en una hoja de fórmulas y conecta sus conclusiones con los intervalos de confianza.
- Usa los intervalos de confianza para recordar los pivotes y errores estándar; aquí cambia la pregunta: en vez de estimar un rango, se contrasta un valor propuesto.
- El Listado 6 (ejercicios 1–4) practica modelos normales, exponenciales y uniformes, no la selección de estos contrastes. El Listado 9 contiene los ejercicios de contraste y su desarrollo está en [[Solucionario - Listado 9]].

---

## Tema 5 — Valor-p

### 1. Resumen

El valor-p es la probabilidad, suponiendo `H₀` y el modelo de la prueba, de obtener un estadístico tan extremo o más que el observado en la dirección o direcciones de `H₁`. Se compara con `α` para decidir.

### 2. Preguntas

- ¿El valor-p se calculó en la cola o colas definidas por `H₁`?
- ¿Es menor o igual que `α`?
- ¿Se está interpretando como una probabilidad calculada bajo `H₀`, o equivocadamente como la probabilidad de que `H₀` sea verdadera?
- Si cambia `α`, ¿cambia el valor-p calculado a partir de los datos?

### 3. Profundizar

Un valor-p pequeño indica que el resultado observado sería inusual bajo `H₀`; por eso constituye evidencia contra ella. El valor-p no mide el tamaño del efecto ni la importancia práctica, y no es la probabilidad de que el resultado se deba «al azar» sin más especificación.

El valor-p se calcula una vez fijados el estadístico, el modelo y la alternativa. `α` es el umbral de decisión acordado; no altera el valor-p. Dos estudios pueden tener el mismo valor-p y efectos de magnitudes distintas, por lo que también conviene reportar estimaciones y, cuando corresponda, intervalos de confianza.

### 4. Fórmulas a considerar

$$
\begin{array}{ll}
p\text{-valor}\le\alpha &\Longrightarrow \text{rechazar }H_0,\\
p\text{-valor}>\alpha &\Longrightarrow \text{no rechazar }H_0.
\end{array}
$$

Para una prueba simétrica con estadístico observado `z_obs`:

$$
\begin{array}{ll}
\text{Cola derecha:} & p=P(Z\ge z_{\text{obs}}),\\
\text{Cola izquierda:} & p=P(Z\le z_{\text{obs}}),\\
\text{Bilateral:} & p=2P(Z\ge |z_{\text{obs}}|).
\end{array}
$$

En una prueba t, chi-cuadrado o F, se usa la distribución correspondiente y la cola correcta; la expresión bilateral no siempre se obtiene simplemente duplicando una cola.

### 5. Conexión con ejercicios

- La definición y el criterio valor-p/`α` se presentan en [[Clase6_2026.pdf]] (p. 5).
- Practica identificando primero si el contraste es unilateral o bilateral y después calcula el área pertinente. Un valor-p de `0.03`, por ejemplo, llevaría a rechazar con `α=0.05`, pero no con `α=0.01`.
- Los ejercicios de pruebas del [[Listado 9 523250 E y P_II_2026.pdf]] permiten practicar la decisión mediante estadístico y valor-p; consulta [[Solucionario - Listado 9]] para el desarrollo.

---

## Tema 6 — Error tipo I, error tipo II y potencia

### 1. Resumen

Como la decisión se toma con una muestra, puede ser incorrecta. El **error tipo I** ocurre al rechazar `H₀` cuando es verdadera. El **error tipo II** ocurre al no rechazar `H₀` cuando es falsa. La potencia es la probabilidad de rechazar `H₀` cuando una alternativa concreta es verdadera.

### 2. Preguntas

- ¿Qué afirmación es verdadera en cada casilla de la tabla de decisión?
- ¿Qué error limita el nivel de significación `α`?
- ¿Por qué `β` depende del valor real del parámetro alternativo?
- ¿Qué efecto pueden tener el tamaño muestral, la variabilidad y el tamaño del efecto sobre la potencia?

### 3. Profundizar

| Realidad | No rechazar `H₀` | Rechazar `H₀` |
|---|---|---|
| `H₀` verdadera | Decisión correcta | Error tipo I (`α`) |
| `H₀` falsa | Error tipo II (`β`) | Decisión correcta (potencia `1-β`) |

`α` controla el riesgo de tipo I según el diseño de la prueba. `β` no es un único número sin especificar una alternativa: suele variar según cuánto se aleja el parámetro verdadero del valor nulo. Con un tamaño muestral mayor o un efecto más grande suele aumentar la potencia, si las demás condiciones se mantienen.

Reducir `α` puede hacer más difícil rechazar `H₀` y, con el mismo tamaño muestral, reducir la potencia frente a ciertas alternativas. El equilibrio depende de las consecuencias prácticas de ambos errores.

### 4. Fórmulas a considerar

$$
\alpha=P(\text{rechazar }H_0\mid H_0\text{ verdadera})
$$

$$
\beta(\theta)=P(\text{no rechazar }H_0\mid \theta\text{ es una alternativa concreta})
$$

$$
\text{Potencia}(\theta)=1-\beta(\theta)
$$

### 5. Conexión con ejercicios

- La tabla y las definiciones se desarrollan en [[Clase6_2026.pdf]] (p. 6).
- Para cada contexto, describe con palabras qué consecuencia tendría un falso positivo (tipo I) y un falso negativo (tipo II); esto ayuda a decidir qué nivel de error es más crítico.
- El Listado 6 no incluye ejercicios de errores de decisión ni de potencia.

---

## Tema 7 — Conclusión estadística y conclusión contextual

### 1. Resumen

La decisión estadística debe traducirse a una respuesta sobre el problema original. Rechazar `H₀` significa que, al nivel elegido y bajo los supuestos del modelo, hay evidencia estadística a favor de `H₁`. No rechazarla significa que la evidencia no fue suficiente para rechazarla.

### 2. Preguntas

- ¿Se indicó `α` y el resultado que determinó la decisión?
- ¿La conclusión nombra el parámetro y la población del problema?
- ¿Se evitó afirmar que `H₀` quedó demostrada o aceptada?
- ¿La relevancia estadística implica también relevancia práctica?
- ¿Se mencionaron límites importantes de diseño o supuestos?

### 3. Profundizar

La significación estadística no dice por sí sola cuán grande o importante es una diferencia. Conviene distinguir entre evidencia estadística, magnitud del efecto e importancia en el contexto. Una muestra muy grande puede detectar diferencias pequeñas; una muestra pequeña puede no detectar una diferencia que sería relevante.

Las pruebas de hipótesis y los intervalos de confianza están relacionados: un intervalo bilateral de nivel `1-α` excluye `θ₀` precisamente cuando la prueba bilateral correspondiente rechaza `H₀: θ=θ₀` al nivel `α`, siempre que ambos métodos usen el mismo modelo y supuestos. La clase destaca que las conclusiones de pruebas e intervalos se corresponden.

### 4. Fórmulas a considerar

Plantilla breve para redactar una conclusión:

> Con nivel de significación `α = ...`, [se rechaza / no se rechaza] `H₀` porque [el estadístico cayó / no cayó en la región crítica, o el valor-p fue ...]. En el contexto, [hay / no hay] evidencia estadística suficiente para afirmar que `...`.

La relación intervalo-prueba para un contraste bilateral:

$$
\theta_0\notin IC_{1-\alpha}
\quad\Longleftrightarrow\quad
\text{rechazar }H_0:\theta=\theta_0
\text{ con una prueba bilateral de nivel }\alpha
$$

### 5. Conexión con ejercicios

- La diapositiva de cierre vincula las pruebas con los intervalos de confianza en [[Clase6_2026.pdf]] (p. 8).
- Revisa los intervalos de confianza para estimar la magnitud plausible del efecto.
- Como práctica guiada disponible, [[Resumen_Prueba_de_Hipótesis.pdf]] ofrece material complementario; confirma en cada ejemplo qué parámetro, diseño y supuestos se usan antes de trasladar la conclusión.

---

## Ruta corta para resolver una prueba

1. **Traducir la pregunta:** identificar población, parámetro y valor de referencia.
2. **Formular `H₀` y `H₁`:** definir si el contraste es bilateral o unilateral antes de mirar el resultado.
3. **Fijar `α`:** no escogerlo después de calcular el estadístico.
4. **Revisar el diseño y los supuestos:** una muestra, dos independientes o pareadas; datos, varianza conocida/desconocida y modelo.
5. **Elegir estadístico y distribución:** normal, `t`, chi-cuadrado o `F`, según corresponda.
6. **Calcular y decidir:** usar región crítica o comparar el valor-p con `α`.
7. **Comunicar:** redactar la conclusión contextual y no decir «aceptamos `H₀`».
8. **Interpretar con cuidado:** distinguir significación estadística de importancia práctica y, si corresponde, acompañar con intervalo de confianza.

## Errores frecuentes

- Elegir una prueba unilateral después de observar que la diferencia va en esa dirección.
- Confundir `α` con el valor-p o con la probabilidad de que `H₀` sea verdadera.
- Afirmar «se acepta `H₀`» cuando el resultado correcto es «no se rechaza `H₀`».
- Usar el estadístico de muestras independientes para datos pareados.
- Suponer varianzas iguales sin respaldo o aplicar un pivote normal cuando se debe usar `t`.
- Usar una prueba de proporción aproximada sin comprobar las condiciones de tamaño.
- Interpretar significación como prueba de causalidad o de relevancia práctica.
- Aplicar un modelo sin revisar independencia, muestreo y condiciones de normalidad requeridas.

## Conexiones dentro del ramo

- Las variables aleatorias → distribuciones y esperanza/varianza que explican el comportamiento muestral.
- Los modelos probabilísticos → modelos normal y otros supuestos usados para construir estadísticos.
- Los intervalos de confianza → pivotes, errores estándar y relación entre contraste bilateral e intervalo.
- [[Resumen_Prueba_de_Hipótesis.pdf]] → desarrollo complementario de fundamentos y casos aplicados.
- Listado 9 → ejercicios de pruebas de hipótesis y comparación de proporciones.
