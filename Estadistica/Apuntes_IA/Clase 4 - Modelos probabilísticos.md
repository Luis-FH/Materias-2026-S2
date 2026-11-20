# Clase 4 — Modelos probabilísticos: guía completa

#certamen1_estadistica

> [!info] Fuentes y conexiones
> - [[Clase4_2026 (1).pdf]] — presentación «Modelos probabilísticos» (63 páginas).
> - [[Listado 4 523250 E y P_II_2026.pdf]] — práctica de distribuciones, probabilidades, esperanza y varianza.
> - [[Solucionario - Listado 4]] — resolución del Listado 4.
> - [[Listado 5 523250 E y P_II_2026.pdf]] y [[Solucionario - Listado 5]] — modelos discretos.
> - [[Listado 6 523250 E y P_II_2026.pdf]] y [[Solucionario - Listado 6]] — modelos continuos.
> - [[Resumen_modelos_discretos.pdf]] — resumen de modelos discretos.
> - [[Ejercicio_modelos_discretos.pdf]] — ejercicios de modelos discretos.
> - [[Tablas Estadísticas.pdf]] — tablas para consultar distribuciones y probabilidades.
> - Índice del ramo: Estadística.

## Alcance y mapa

La Clase 4 presenta **modelos probabilísticos concretos**. La pregunta central no es solo «¿qué fórmula uso?», sino:

1. ¿Qué experimento genera los datos?
2. ¿Qué cuenta `X` y qué valores puede tomar?
3. ¿Qué condiciones del experimento determinan el modelo?
4. ¿Qué parámetros describen la situación?
5. ¿Qué probabilidad, esperanza o variabilidad necesito?

Recorrido completo del material:

| Familia | Modelo | Idea del experimento |
|---|---|---|
| Discreta | Bernoulli | Un ensayo, éxito/fracaso |
| Discreta | Binomial | Número de éxitos en `n` ensayos independientes |
| Discreta | Geométrica | Ensayos hasta el primer éxito |
| Discreta | Binomial negativa | Ensayos hasta el éxito número `r` |
| Discreta | Hipergeométrica | Éxitos en una muestra sin reemplazo |
| Discreta | Poisson | Conteo de ocurrencias en una unidad de tiempo/espacio |
| Continua | Uniforme | Todos los subintervalos de igual longitud tienen igual densidad |
| Continua | Exponencial | Tiempo de espera hasta una ocurrencia |
| Continua | Normal | Medición continua con distribución simétrica en forma de campana |

Cada modelo se estudia con el mismo ciclo: **1. resumen → 2. preguntas → 3. profundizar → 4. fórmulas → 5. conexión con el listado**.

---

## Tema 1 — Ensayo de Bernoulli

### 1. Resumen

Un **ensayo de Bernoulli** tiene dos resultados posibles: éxito y fracaso. Se define `X=1` si ocurre el éxito y `X=0` si ocurre el fracaso. Si la probabilidad de éxito es `p`, la de fracaso es `q=1-p`.

Ejemplos: acertar un blanco, que una pieza resulte defectuosa o que una moneda salga cara. «Éxito» solo nombra el resultado de interés; no significa necesariamente algo deseable.

### 2. Preguntas

- ¿Cuál es el resultado que se ha definido como éxito?
- ¿Los dos resultados son exhaustivos y mutuamente excluyentes?
- ¿Cuál es `p` y cuál es `q`? ¿Suman 1?
- Si cambio qué resultado llamo éxito, ¿cómo cambia `X`?

### 3. Profundizar

Bernoulli modela **una sola observación**. Si repetimos ensayos Bernoulli con la misma probabilidad de éxito e independencia, podemos contar los éxitos con un modelo binomial.

La variable indicadora `X` es útil porque convierte una respuesta cualitativa (sí/no) en un número. Su esperanza es `p`: en muchas repeticiones comparables, la proporción de éxitos tiende a `p`.

### 4. Fórmulas a considerar

$$
P(X=x)=p^x(1-p)^{1-x},\qquad x\in\{0,1\}
$$

$$
E[X]=p,\qquad \operatorname{Var}(X)=p(1-p)=pq
$$

### 5. Conexión con el Listado 4

En los **ejercicios 1 y 4**, cada lanzamiento individual de una moneda se puede representar como Bernoulli. El número total de caras de varios lanzamientos se modela con una binomial (Tema 2).

**En la clase:** [[Clase4_2026 (1).pdf]], modelo de Bernoulli (PDF, pp. 2–9).

---

## Tema 2 — Distribución binomial

### 1. Resumen

La **binomial** cuenta cuántos éxitos ocurren en `n` ensayos Bernoulli independientes, todos con la misma probabilidad de éxito `p`. Se escribe `X ~ Bin(n,p)`.

`X` puede valer `0,1,…,n`. La binomial responde preguntas como «¿cuál es la probabilidad de obtener exactamente `k` éxitos en `n` intentos?».

### 2. Preguntas

- ¿Qué cuenta `X`: los intentos hasta el primer éxito o los éxitos en un número fijo de intentos?
- ¿Se fija `n` antes de realizar el experimento?
- ¿Cada ensayo tiene el mismo `p`?
- ¿El resultado de un ensayo cambia la probabilidad del siguiente?
- ¿Qué significa «a lo más `k`», «al menos `k`» y «exactamente `k`»?

### 3. Profundizar

Comprueba las cuatro condiciones antes de usar la fórmula:

1. Número fijo de ensayos `n`.
2. Dos resultados por ensayo, éxito/fracaso.
3. Probabilidad de éxito constante `p`.
4. Ensayos independientes.

El coeficiente combinatorio cuenta de cuántas maneras se pueden ubicar los `k` éxitos entre los `n` ensayos. La probabilidad de una secuencia específica con `k` éxitos y `n-k` fracasos es `p^k(1-p)^{n-k}`; multiplicar por el número de secuencias produce la función de probabilidad.

Para una probabilidad acumulada, suma los valores pertinentes o usa el complemento. Por ejemplo, `P(X≥1)=1-P(X=0)`. «Al menos uno» suele ser más fácil por complemento que sumando `P(X=1)+…+P(X=n)`.

### 4. Fórmulas a considerar

Función de probabilidad:

$$
P(X=k)=\binom{n}{k}p^k(1-p)^{n-k},\qquad k=0,1,\ldots,n
$$

Esperanza, varianza y desviación estándar:

$$
E[X]=np,\qquad \operatorname{Var}(X)=np(1-p)=npq,\qquad
\sigma_X=\sqrt{npq}
$$

Complemento para «al menos un éxito»:

$$
P(X\geq 1)=1-P(X=0)=1-(1-p)^n
$$

### 5. Conexión con el Listado 4

- **Ejercicio 1:** número de caras en cinco lanzamientos; especifica el éxito y reconoce `n=5`.
- **Ejercicio 4:** número de caras en tres lanzamientos. Además de la distribución, pide FDA y medidas de resumen; construye primero la distribución y luego acumula o suma.

Para empezar cada uno, escribe una frase del tipo «`X` cuenta ___ éxitos en ___ ensayos; la probabilidad de éxito es ___».

**En la clase:** [[Clase4_2026 (1).pdf]], modelo binomial (PDF, pp. 10–15).

---

## Tema 3 — Distribución geométrica

### 1. Resumen

La **geométrica** modela el número de ensayos Bernoulli necesarios hasta obtener el **primer éxito**, contando también el ensayo exitoso. Se escribe `X ~ Geo(p)` y toma valores `1,2,3,…`.

### 2. Preguntas

- ¿El conteo incluye el ensayo en que finalmente ocurre el éxito?
- Si el primer ensayo tiene éxito, ¿qué valor toma `X`?
- ¿Qué probabilidad debe tener una secuencia con `k-1` fracasos seguidos por un éxito?
- ¿Qué cambiaría si se definiera `X` como el número de fracasos antes del primer éxito?

### 3. Profundizar

Para que el modelo aplique, los ensayos deben ser independientes y la probabilidad `p` debe mantenerse constante en cada intento. Para que el primer éxito ocurra en el ensayo `k`, debe haber `k-1` fracasos y luego un éxito.

La convención usada aquí cuenta **ensayos hasta el éxito**; por eso el soporte empieza en 1 y `E[X]=1/p`. Algunos textos definen otra variable que cuenta solo fracasos antes del éxito: su soporte y su esperanza cambian. Fíjate siempre en la definición de `X`.

La geométrica carece de memoria: si los ensayos siguen siendo independientes, esperar varios fracasos no altera la probabilidad ni la distribución del número adicional de intentos.

### 4. Fórmulas a considerar

$$
P(X=k)=(1-p)^{k-1}p,\qquad k=1,2,\ldots
$$

$$
P(X>k)=(1-p)^k
$$

$$
E[X]=\frac{1}{p},\qquad
\operatorname{Var}(X)=\frac{1-p}{p^2}
$$

### 5. Conexión con el Listado 4

El **Listado 4 no presenta un ejercicio que describa explícitamente «ensayar hasta el primer éxito»**. Los ejercicios 1 y 4 practican los ensayos Bernoulli, que son el punto de partida; para practicar una geométrica, traduce una situación con intentos repetidos y detente en el primer éxito.

**En la clase:** [[Clase4_2026 (1).pdf]], modelo geométrico (PDF, pp. 16–21).

---

## Tema 4 — Distribución binomial negativa

### 1. Resumen

La **binomial negativa** cuenta el número de ensayos Bernoulli hasta obtener el éxito número `r`, con la misma probabilidad `p` e independencia entre ensayos. Se escribe `X ~ BinNeg(r,p)`. El soporte es `r,r+1,…`.

La geométrica es el caso particular `r=1`.

### 2. Preguntas

- ¿Cuál es el número de éxitos que se debe alcanzar?
- ¿`X` cuenta ensayos totales o fracasos antes de alcanzar `r` éxitos?
- Si el éxito número `r` ocurre en el ensayo `k`, ¿cuántos éxitos hay entre los primeros `k-1` ensayos?
- ¿Cómo se reconoce el caso geométrico dentro de este modelo?

### 3. Profundizar

Para que el éxito `r` ocurra exactamente en el ensayo `k`:

1. El ensayo `k` debe ser un éxito.
2. Entre los primeros `k-1` ensayos debe haber exactamente `r-1` éxitos.
3. Los otros `k-r` ensayos anteriores son fracasos.

Por eso el número de maneras de ordenar los primeros `k-1` resultados es `C(k-1,r-1)`. Esta versión de la binomial negativa cuenta **ensayos totales**, incluido el éxito número `r`.

### 4. Fórmulas a considerar

$$
P(X=k)=\binom{k-1}{r-1}p^r(1-p)^{k-r},
\qquad k=r,r+1,\ldots
$$

$$
E[X]=\frac{r}{p},\qquad
\operatorname{Var}(X)=\frac{r(1-p)}{p^2}
$$

### 5. Conexión con el Listado 4

El listado no incluye un ejercicio explícito de «esperar hasta el éxito número `r`». Relaciona el modelo con Bernoulli, binomial y geométrica para distinguir qué cantidad se fija y qué se cuenta. Si se pide número de ensayos en un número fijo de intentos, es binomial; si se detiene al completar cierto número de éxitos, es binomial negativa.

**En la clase:** [[Clase4_2026 (1).pdf]], modelo binomial negativo (PDF, pp. 22–27).

---

## Tema 5 — Distribución hipergeométrica

### 1. Resumen

La **hipergeométrica** cuenta los éxitos en una muestra aleatoria de tamaño `n`, seleccionada **sin reemplazo** de una población finita de tamaño `N`, que contiene `M` éxitos y `N-M` fracasos.

Se escribe `X ~ HGeom(N,M,n)`. El número de éxitos posible está acotado por el tamaño de la muestra y por los elementos disponibles en la población.

### 2. Preguntas

- ¿La población es finita?
- ¿Se devuelve cada elemento antes de seleccionar el siguiente?
- ¿La probabilidad de éxito en la siguiente extracción se mantiene fija?
- ¿Qué valores mínimos y máximos puede tomar `X`?
- ¿Por qué la binomial puede ser una aproximación cuando la población es grande frente a la muestra?

### 3. Profundizar

En una muestra sin reemplazo, las selecciones están relacionadas: cada extracción cambia la composición de lo que queda. Por eso no corresponde tratar automáticamente cada extracción como un ensayo independiente con una probabilidad constante.

El numerador cuenta muestras con exactamente `x` éxitos: elegir `x` entre los `M` éxitos y `n-x` entre los `N-M` fracasos. El denominador cuenta todas las muestras posibles de tamaño `n`.

El soporte debe respetar ambas restricciones: no se pueden extraer menos éxitos de los que permite la muestra, ni más éxitos de los que hay en la población.

### 4. Fórmulas a considerar

$$
P(X=x)=
\frac{\binom{M}{x}\binom{N-M}{n-x}}{\binom{N}{n}}
$$

Valores permitidos:

$$
\max(0,n-(N-M))\leq x\leq \min(n,M)
$$

Esperanza y varianza:

$$
E[X]=n\frac{M}{N}
$$

$$
\operatorname{Var}(X)=
n\frac{M}{N}\left(1-\frac{M}{N}\right)
\frac{N-n}{N-1}
$$

El factor `(N-n)/(N-1)` refleja la corrección por muestreo sin reemplazo.

### 5. Conexión con el Listado 4

El listado trabaja con distribuciones discretas, pero **no se identifica en sus ejercicios 1–4 una selección explícita sin reemplazo de una población finita**. El criterio decisivo para reconocer la hipergeométrica es «muestra sin reemplazo», no solo que se cuenten éxitos.

**En la clase:** [[Clase4_2026 (1).pdf]], modelo hipergeométrico (PDF, pp. 28–34).

---

## Tema 6 — Distribución de Poisson

### 1. Resumen

La **Poisson** modela el número de ocurrencias de un evento en un intervalo fijo de tiempo, espacio o alguna otra unidad, cuando la tasa promedio de ocurrencias es `λ`. Se escribe `X ~ Pois(λ)`, con soporte `0,1,2,…`.

### 2. Preguntas

- ¿Qué se está contando y cuál es el intervalo de referencia?
- ¿La tasa `λ` se refiere a ese intervalo o a otra unidad?
- Si duplicas el intervalo y la tasa es constante, ¿cómo cambia el parámetro esperado?
- ¿Por qué `λ` debe ser no negativo?

### 3. Profundizar

`λ` es el número promedio esperado de ocurrencias **en el intervalo especificado**. Si se cambia de unidad, también se debe cambiar la tasa. Por ejemplo, una tasa por hora debe convertirse antes de calcular para 15 minutos.

La distribución se usa como modelo de conteo; no significa que las ocurrencias sean predecibles individualmente. En situaciones apropiadas, la binomial puede aproximarse por Poisson cuando `n` es grande, `p` es pequeño y `np` se mantiene aproximadamente constante. Esta aproximación no reemplaza la comprobación de que el modelo sea razonable.

### 4. Fórmulas a considerar

$$
P(X=k)=e^{-\lambda}\frac{\lambda^k}{k!},
\qquad k=0,1,2,\ldots
$$

$$
E[X]=\lambda,\qquad \operatorname{Var}(X)=\lambda
$$

Probabilidad de ninguna ocurrencia:

$$
P(X=0)=e^{-\lambda}
$$

Si una tasa es `r` por unidad y se observa un intervalo de longitud `t`, el parámetro correspondiente es `λ=rt`.

### 5. Conexión con el Listado 4

Los ejercicios 1–4 del listado enfatizan conteos discretos, distribución y momentos; esa práctica ayuda a sumar probabilidades de conteo. Sin embargo, **no identifico en ellos un proceso de ocurrencias por intervalo que especifique una tasa Poisson**. Para practicar este modelo, el enunciado debe definir el intervalo y entregar una tasa promedio.

**En la clase:** [[Clase4_2026 (1).pdf]], modelo de Poisson (PDF, pp. 35–39).

---

## Tema 7 — Distribución uniforme continua

### 1. Resumen

Una variable `X` tiene distribución **uniforme continua** en `(a,b)` si su densidad es constante en ese intervalo y cero fuera. Se escribe `X ~ U(a,b)`. La probabilidad de un subintervalo depende de su longitud relativa dentro de `(a,b)`.

### 2. Preguntas

- ¿En qué intervalo está definida la densidad?
- ¿Qué valor constante necesita tener para que el área total sea 1?
- ¿Qué fracción de la longitud total representa el intervalo pedido?
- ¿Por qué la probabilidad de un punto individual es cero?

### 3. Profundizar

La curva de densidad es un rectángulo de base `b-a` y área 1; su altura debe ser `1/(b-a)`. Si todos los subintervalos de igual longitud dentro del soporte reciben la misma probabilidad, el modelo uniforme es coherente.

La uniforme es un modelo continuo, aunque se diga informalmente que «todos los valores son igual de probables». Más precisamente, **los intervalos de igual longitud** tienen igual probabilidad; cada punto individual tiene probabilidad cero.

### 4. Fórmulas a considerar

Densidad:

$$
f_X(x)=
\begin{cases}
\dfrac{1}{b-a},&a<x<b,\\
0,&\text{en otro caso.}
\end{cases}
$$

FDA:

$$
F_X(x)=
\begin{cases}
0,&x\leq a,\\
\dfrac{x-a}{b-a},&a<x<b,\\
1,&x\geq b.
\end{cases}
$$

Para `a≤c≤d≤b`:

$$
P(c\leq X\leq d)=\frac{d-c}{b-a}
$$

$$
E[X]=\frac{a+b}{2},\qquad
\operatorname{Var}(X)=\frac{(b-a)^2}{12}
$$

### 5. Conexión con el Listado 4

- **Ejercicio 6:** la distancia `X` al centro de la diana se modela con una densidad constante en un intervalo. Se pide normalizar la densidad, construir la FDA, hallar esperanza/varianza y calcular probabilidades.
- Los ejercicios **5, 8 y 9** también practican densidades e integración; no todos son uniformes, por lo que primero revisa la forma de `f(x)`.

En [[Listado 4 523250 E y P_II_2026.pdf]] y [[Clase4_2026 (1).pdf]] (PDF, pp. 40–47).

---

## Tema 8 — Distribución exponencial

### 1. Resumen

La **exponencial** modela un tiempo de espera continuo hasta una ocurrencia, con tasa `λ>0`. Se escribe `X ~ Exp(λ)`, donde `λ` es la tasa por unidad de tiempo (o de la magnitud observada). Su soporte es `x≥0`.

### 2. Preguntas

- ¿`λ` representa una tasa o un tiempo medio?
- ¿Cuál es el soporte físicamente razonable para un tiempo de espera?
- Si una pregunta dice «dura más de `t`», ¿qué área o cola hay que calcular?
- ¿Por qué importa mantener consistentes las unidades de `λ` y `t`?

### 3. Profundizar

Con la parametrización de la clase, `λ` es la **tasa** y el promedio de espera es `1/λ`. No confundas la tasa con la media: si la tasa se expresa por hora, `1/λ` queda en horas.

La propiedad sin memoria dice que, dado que la espera ya superó `s`, la distribución de la espera adicional es la misma que al inicio. Es una propiedad particular del modelo exponencial; no se debe asumir para cualquier tiempo de vida.

La clase también relaciona la exponencial con un tiempo de vida. Si la densidad se define solo para `x>0`, debe ser cero para valores negativos.

### 4. Fórmulas a considerar

Densidad y FDA:

$$
f_X(x)=
\begin{cases}
\lambda e^{-\lambda x},&x\geq 0,\\
0,&x<0,
\end{cases}
\qquad
F_X(x)=
\begin{cases}
1-e^{-\lambda x},&x\geq 0,\\
0,&x<0.
\end{cases}
$$

Cola o supervivencia:

$$
P(X>t)=e^{-\lambda t},\qquad t\geq 0
$$

Esperanza y varianza:

$$
E[X]=\frac{1}{\lambda},\qquad
\operatorname{Var}(X)=\frac{1}{\lambda^2}
$$

Propiedad sin memoria:

$$
P(X>s+t\mid X>s)=P(X>t)
$$

### 5. Conexión con el Listado 4

- **Ejercicio 7:** la densidad con forma exponencial permite comprobar que la función sea válida, usar la cola `P(X>10)` y calcular probabilidades en intervalos.
- **Ejercicios 5, 8 y 9:** sirven para practicar integración de densidades y cálculo de probabilidades aunque no necesariamente sean exponenciales.

En [[Listado 4 523250 E y P_II_2026.pdf]] y [[Clase4_2026 (1).pdf]] (PDF, pp. 48–54).

---

## Tema 9 — Distribución normal y normal estándar

### 1. Resumen

La **normal** es una distribución continua, simétrica y con forma de campana, determinada por su media `μ` y varianza `σ²`. Se escribe `X ~ N(μ,σ²)`. La media indica el centro y la desviación estándar `σ` controla la dispersión.

La **normal estándar** `Z ~ N(0,1)` permite usar una misma tabla para calcular probabilidades de cualquier normal mediante estandarización.

### 2. Preguntas

- ¿Qué parámetro determina el centro? ¿Cuál determina la dispersión?
- ¿Qué diferencia hay entre `σ` y `σ²`?
- ¿Cómo conviertes un valor `x` de una normal cualquiera a escala estándar?
- ¿Cómo representas `P(X≤x)` con la CDF estándar `Φ`?
- Si el área buscada está a la derecha, ¿cómo la relacionas con el área acumulada a la izquierda?

### 3. Profundizar

Para estandarizar, resta la media y divide por la desviación estándar. El resultado indica cuántas desviaciones estándar separan a `x` del centro. La transformación conserva el orden: valores mayores de `X` corresponden a valores mayores de `Z`.

La función `Φ(z)=P(Z≤z)` acumula el área a la izquierda. Muchas tablas entregan precisamente esa área; otras pueden tener otro formato, así que verifica el encabezado antes de leerlas.

Usa simetría alrededor de cero para convertir probabilidades de cola derecha en probabilidades acumuladas. Para intervalos, resta dos probabilidades acumuladas. No confundas la densidad en un punto con un área de probabilidad.

### 4. Fórmulas a considerar

Densidad de `X ~ N(μ,σ²)`:

$$
f_X(x)=\frac{1}{\sigma\sqrt{2\pi}}
\exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right),
\qquad -\infty<x<\infty
$$

Media y varianza:

$$
E[X]=\mu,\qquad \operatorname{Var}(X)=\sigma^2
$$

Estandarización:

$$
Z=\frac{X-\mu}{\sigma}\sim N(0,1)
$$

Probabilidad acumulada e intervalo:

$$
P(X\leq x)=\Phi\left(\frac{x-\mu}{\sigma}\right)
$$

$$
P(a<X\leq b)=
\Phi\left(\frac{b-\mu}{\sigma}\right)
-\Phi\left(\frac{a-\mu}{\sigma}\right)
$$

Simetría y cola:

$$
\Phi(-z)=1-\Phi(z),\qquad P(Z>z)=1-\Phi(z)
$$

### 5. Conexión con el Listado 4

En las páginas 1–3 del [[Listado 4 523250 E y P_II_2026.pdf]] no se distingue un ejercicio que declare explícitamente `X ~ N(μ,σ²)`. Los ejercicios 5–9 sí practican densidades continuas, probabilidades y momentos; sirven para afianzar la interpretación de áreas y la integración, pero no sustituyen la práctica de estandarizar y leer una tabla normal.

La parte final de [[Clase4_2026 (1).pdf]] trabaja la normal estándar y probabilidades usando tablas (PDF, pp. 55–63). Usa también [[Tablas Estadísticas.pdf]] para practicar la lectura de `Φ`.

---

## Cómo elegir un modelo: preguntas de diagnóstico

1. **¿La variable es un conteo o una medida continua?**
   - Conteo `0,1,2,…`: considera un modelo discreto.
   - Tiempo, distancia o medida: considera una densidad continua.
2. **¿Hay un número fijo de ensayos y se cuentan éxitos?**
   - Sí, con independencia y `p` constante: binomial.
3. **¿El experimento se repite hasta alcanzar un éxito?**
   - Primer éxito: geométrica.
   - Éxito número `r`: binomial negativa.
4. **¿Se extrae una muestra de una población finita sin reemplazo?**
   - Hipergeométrica.
5. **¿Se cuenta cuántas ocurrencias hay por intervalo, dada una tasa media?**
   - Poisson.
6. **¿Es una medida continua en un intervalo con densidad constante?**
   - Uniforme.
7. **¿Se modela el tiempo de espera hasta un evento con tasa constante y falta de memoria?**
   - Exponencial.
8. **¿La variable continua se modela simétrica alrededor de una media y la tabla normal es pertinente?**
   - Normal; estandariza antes de usar la tabla.

## Errores que conviene evitar

- Aplicar una fórmula porque los datos «parecen» binomiales sin verificar independencia y `p` constante.
- Confundir binomial (número de éxitos en `n` intentos) con geométrica (ensayos hasta el primer éxito).
- Usar geométrica o binomial negativa sin indicar si `X` cuenta ensayos totales o fracasos.
- Tratar una muestra sin reemplazo como independiente cuando la población no es grande respecto de la muestra.
- Usar Poisson sin fijar el intervalo y las unidades de la tasa.
- Confundir la tasa `λ` de la exponencial con su media `1/λ`.
- Interpretar la densidad continua como probabilidad puntual.
- Olvidar que la varianza normal es `σ²`, pero se estandariza dividiendo por `σ`.
- Leer una tabla normal sin confirmar si entrega área a la izquierda, cola derecha u otra convención.

## Ruta de resolución

1. Define `X` con palabras y escribe sus unidades.
2. Anota el soporte y qué evento se considera éxito, si aplica.
3. Elige el modelo **a partir del mecanismo del experimento**, no solo por la forma de los números.
4. Anota la parametrización y las unidades de cada parámetro.
5. Traduce la pregunta: exacta, acumulada, cola, intervalo, esperanza o varianza.
6. Sustituye en la fórmula y comprueba límites y soporte.
7. Revisa que una probabilidad esté entre 0 y 1 y que la respuesta tenga interpretación y unidades coherentes.
