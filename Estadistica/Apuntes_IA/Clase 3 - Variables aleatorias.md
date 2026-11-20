# Clase 3 — Variables aleatorias: guía paso a paso

#certamen1_estadistica

> [!info] Fuentes y conexiones
> - [[Clase3_2026 (1).pdf]] — material de la clase sobre variable aleatoria (29 páginas).
> - [[Listado 4 523250 E y P_II_2026.pdf]] — ejercicios de distribuciones discretas y continuas.
> - [[Solucionario - Listado 4]] — resolución paso a paso.
> - [[resumen_variable_aleatoria.pdf]] — guía complementaria de variables aleatorias.
> - [[ejemplos_variable_aleatoria.pdf]] — ejemplos de variables aleatorias.
> - Índice del ramo: Estadística.

## Mapa de la clase

Una variable aleatoria convierte los resultados de un experimento en números. Una vez que se conoce qué valores puede tomar y con qué probabilidades, se puede describir su distribución, calcular probabilidades y resumir su centro y variabilidad:

`experimento → variable X → distribución → probabilidades → esperanza y varianza`

En cada tema sigue este orden: **1. resumen → 2. preguntas → 3. profundizar → 4. fórmulas → 5. conexión con el listado**. Las preguntas sirven para pausar y comprobar comprensión; la nota no incluye la resolución completa de los ejercicios.

---

## Tema 1 — Variable aleatoria y recorrido

### 1. Resumen

Una **variable aleatoria** (`X`) es una función que asigna un número real a cada resultado de un experimento aleatorio. El número no tiene por qué ser el resultado original: puede resumirlo.

Ejemplo de la clase: se lanza una moneda tres veces y `X` cuenta el número de caras. Los resultados son secuencias como `CCS` o `SSS`, pero los valores de `X` son solo `0, 1, 2, 3`.

El **recorrido** (`R_X`) es el conjunto de valores que la variable puede tomar. Para una variable discreta, basta considerar los valores con probabilidad positiva. Una variable es:

- **Discreta** si su recorrido es finito o numerable; por ejemplo, contar caras, llamadas o productos.
- **Continua** si puede tomar valores en intervalos; por ejemplo, medir tiempo, longitud o masa.

### 2. Preguntas

- ¿Cuál es el experimento y qué aspecto de sus resultados mide `X`?
- En tres lanzamientos, ¿qué valor de `X` corresponde a `CCS`? ¿Y a `SSS`?
- ¿Dos resultados diferentes del experimento pueden producir el mismo valor de `X`?
- ¿Una medida registrada con dos decimales se vuelve necesariamente una variable discreta?

### 3. Profundizar

Para definir bien una variable aleatoria, escribe primero qué se observa y luego qué número se asigna a cada resultado. Distintas secuencias de lanzamientos pueden tener el mismo conteo de caras; por eso `X` resume y pierde parte del detalle del resultado original.

La distinción discreta/continua se refiere al modelo de la variable, no a cómo se anotaron los datos. El tiempo es conceptualmente continuo aunque un cronómetro lo muestre en segundos enteros; el número de clientes es discreto aunque sea grande.

Algunos problemas transforman una variable ya definida. Si el ingreso depende de la demanda `X`, por ejemplo, puede definirse `Y = 200X + 300000`. La distribución de `Y` se obtiene aplicando la transformación a los valores de `X`.

### 4. Fórmulas a considerar

Definición como función:

$$
X:\Omega\to\mathbb{R}
$$

Recorrido:

$$
R_X=\{X(\omega):\omega\in\Omega\}
$$

Para una variable discreta, su soporte probabilístico es `\{x:p_X(x)>0\}`.

Transformación de una variable:

$$
Y=g(X)
$$

### 5. Conexión con el listado

- **Ejercicio 1:** `X` es el número de caras al lanzar cinco monedas; su recorrido se identifica antes de construir la distribución.
- **Ejercicio 2:** `X` representa la demanda diaria del kiosco; luego el ingreso se expresa como una transformación de `X`.
- **Ejercicio 3:** `X` es la capacidad de uno de los modelos disponibles y toma valores de una lista finita.
- **Ejercicio 4:** se vuelve a contar el número de caras, ahora con tres lanzamientos.

Practica en [[Listado 4 523250 E y P_II_2026.pdf]]. Para repasar el experimento y sus resultados, vuelve a la explicación del espacio muestral y la probabilidad.

**Referencia:** [[Clase3_2026 (1).pdf]], definición y tipos de variables aleatorias (PDF, pp. 4–6).

---

## Tema 2 — Distribución discreta: función de probabilidad

### 1. Resumen

La **función de probabilidad** o **función de masa** de una variable discreta asigna a cada valor posible `x` su probabilidad:

`p_X(x) = P(X = x)`.

La lista o tabla de valores `x` y probabilidades `p_X(x)` describe la distribución de `X`. Las probabilidades deben ser no negativas y sumar 1.

### 2. Preguntas

- ¿Qué eventos elementales forman el evento `X = x`?
- ¿Cómo verificas rápidamente si una tabla propuesta puede ser una función de probabilidad?
- Si varios resultados del experimento producen `X = x`, ¿se suma la probabilidad de esos resultados?
- ¿Cómo obtienes `P(X ≤ a)` a partir de una tabla discreta?

### 3. Profundizar

Procedimiento para construir una distribución desde un experimento:

1. Define `X` y enumera su recorrido.
2. Para cada valor `x`, identifica todos los resultados que hacen que `X = x`.
3. Calcula `P(X=x)` sumando las probabilidades de esos resultados.
4. Comprueba que cada probabilidad sea no negativa y que el total sea 1.

Si los resultados elementales son equiprobables, el conteo puede simplificar el cálculo, pero solo después de comprobar esa condición. En problemas con probabilidades distintas, no basta contar cuántos resultados producen `x`.

Para un evento formado por varios valores de `X`, se suman las masas correspondientes. Por ejemplo, `P(a ≤ X ≤ b)` es la suma de las probabilidades de todos los valores del recorrido que cumplen la desigualdad, incluidos los extremos.

### 4. Fórmulas a considerar

Función de masa:

$$
p_X(x)=P(X=x)
$$

Condiciones de validez:

$$
p_X(x)\geq 0,\qquad \sum_{x\in R_X}p_X(x)=1
$$

Probabilidad de un conjunto de valores `A`:

$$
P(X\in A)=\sum_{x\in A\cap R_X}p_X(x)
$$

### 5. Conexión con el listado

- **Ejercicio 1:** completa la distribución del número de caras en cinco lanzamientos y luego usa esa tabla para responder probabilidades.
- **Ejercicio 2:** comprueba que las probabilidades de demanda sumen 1 antes de calcular el ingreso esperado.
- **Ejercicio 3:** la tabla de capacidades y probabilidades ya especifica una distribución discreta; úsala como base para los cálculos posteriores.
- **Ejercicio 4:** construye la distribución del número de caras en tres lanzamientos.

Todos están en [[Listado 4 523250 E y P_II_2026.pdf]].

**Referencia:** [[Clase3_2026 (1).pdf]], función de probabilidad discreta y ejemplo de lanzamientos (PDF, pp. 8–10).

---

## Tema 3 — Distribución continua: función de densidad

### 1. Resumen

Una variable continua se describe mediante una **función de densidad** `f_X(x)`. La densidad no es la probabilidad de que `X` tome exactamente el valor `x`: las probabilidades se obtienen como áreas bajo la curva en intervalos.

Una densidad válida es no negativa y el área total bajo ella es 1. Para una variable continua, la probabilidad de un solo punto es cero.

### 2. Preguntas

- ¿Qué representa geométricamente `P(a < X < b)`?
- ¿Por qué una densidad puede ser mayor que 1 en algún punto y aun así ser válida?
- ¿Cuál es la diferencia entre `f_X(2)` y `P(X=2)`?
- ¿Cambian las probabilidades si se incluye o no un extremo del intervalo?

### 3. Profundizar

La altura de la curva mide densidad, no probabilidad puntual. Por eso `f_X(x)` puede superar 1, siempre que la función no sea negativa y su integral total sea 1.

Para calcular la probabilidad en un intervalo, integra entre los límites en el orden correcto. Si la densidad es cero fuera de un rango, el área y la probabilidad fuera de ese rango también son cero. Para una variable continua, agregar o quitar un extremo no cambia la probabilidad del intervalo porque `P(X=a)=0`.

En ejercicios con constantes desconocidas:

1. Usa la condición de área total 1 para encontrar la constante o una relación entre constantes.
2. Usa la información adicional entregada para determinar las restantes.
3. Integra la densidad en el intervalo pedido.

### 4. Fórmulas a considerar

Condiciones de densidad:

$$
f_X(x)\geq 0,\qquad \int_{-\infty}^{\infty}f_X(x)\,dx=1
$$

Probabilidad en un intervalo:

$$
P(a<X\leq b)=\int_a^b f_X(x)\,dx
$$

Probabilidad en un punto:

$$
P(X=a)=0
$$

### 5. Conexión con el listado

- **Ejercicios 5–8:** practican el uso de densidades definidas por tramos o con constantes por determinar; las preguntas piden probabilidades, media o variabilidad.
- **Ejercicio 9:** aplica una densidad a un contexto de precipitaciones y solicita probabilidades para intervalos.

Practica en [[Listado 4 523250 E y P_II_2026.pdf]]. La clase ilustra una variable de tiempo de vida con densidad exponencial en [[Clase3_2026 (1).pdf]] (PDF, pp. 11–13).

---

## Tema 4 — Función de distribución acumulada

### 1. Resumen

La **función de distribución acumulada** (FDA o CDF) de `X` se define como:

`F_X(x) = P(X ≤ x)`.

Acumula la probabilidad hasta `x`. Existe para variables discretas y continuas. En el caso discreto forma escalones; en el continuo se obtiene integrando la densidad.

### 2. Preguntas

- ¿Qué evento representa `F_X(3)`?
- ¿Cómo se calcula `P(a < X ≤ b)` usando `F_X`?
- ¿Por qué la CDF nunca disminuye?
- ¿Qué diferencia visual esperas entre la CDF de una variable discreta y la de una continua?

### 3. Profundizar

La FDA traduce desigualdades acumuladas en una sola función. Para una variable discreta, suma las probabilidades de todos los valores que no superan `x`. Para una continua, integra la densidad desde menos infinito hasta `x`.

Es una función no decreciente, con valores entre 0 y 1, que tiende a 0 hacia la izquierda y a 1 hacia la derecha. Puede tener saltos: el tamaño del salto en `x` es `P(X=x)`. En el caso continuo, la FDA es continua; donde es derivable, su derivada es la densidad.

Cuida el signo de las desigualdades. La diferencia `F(b)-F(a)` representa `P(a<X≤b)`, no `P(a≤X≤b)` en general si hay masa puntual en `a`.

### 4. Fórmulas a considerar

Definición:

$$
F_X(x)=P(X\leq x)
$$

Probabilidad entre dos límites:

$$
P(a<X\leq b)=F_X(b)-F_X(a)
$$

Caso discreto:

$$
F_X(x)=\sum_{y\leq x}p_X(y)
$$

Caso continuo:

$$
F_X(x)=\int_{-\infty}^{x}f_X(t)\,dt
$$

Relación entre densidad y FDA, cuando la derivada existe:

$$
f_X(x)=F_X'(x)
$$

### 5. Conexión con el listado

- **Ejercicio 4 (b):** pide la función de distribución del número de caras; constrúyela acumulando los valores de la función de masa.
- **Ejercicio 6 (b):** pide la FDA a partir de una densidad; integra por tramos y respeta los rangos.
- **Ejercicios 7–9:** usa la densidad para obtener probabilidades; también puedes verificar resultados con la FDA cuando ya esté construida.

En [[Listado 4 523250 E y P_II_2026.pdf]].

**Referencia:** [[Clase3_2026 (1).pdf]], definición y propiedades de la función de distribución acumulada (PDF, pp. 14–19).

---

## Tema 5 — Esperanza y transformaciones

### 1. Resumen

La **esperanza** `E[X]` es el promedio teórico o centro de la distribución. No tiene que ser un valor que la variable pueda tomar. Para variables discretas se pondera cada valor por su probabilidad; para variables continuas se pondera con la densidad e integra.

También se puede calcular la esperanza de una transformación `g(X)` directamente a partir de la distribución de `X`, sin construir primero la distribución de `g(X)`.

### 2. Preguntas

- ¿Qué expresa la esperanza de una distribución: un resultado garantizado o un promedio de largo plazo?
- ¿Puede `E[X]` quedar fuera del recorrido de una variable discreta?
- Si `Y=200X+300000`, ¿cómo se relaciona `E[Y]` con `E[X]`?
- ¿Por qué para `E[g(X)]` no siempre basta con calcular `g(E[X])`?

### 3. Profundizar

La esperanza funciona como promedio ponderado. Valores más probables tienen más peso. En una tabla discreta, multiplica cada `x` por `p_X(x)` y suma; en una distribución continua, integra `x f_X(x)`.

Para una transformación, aplica la función a cada valor posible y promedia esos resultados con las probabilidades originales. En general:

`E[g(X)]` no es lo mismo que `g(E[X])`.

Una excepción útil son las transformaciones lineales: `E[aX+b]=aE[X]+b`. Así se calcula directamente el ingreso esperado a partir de la demanda esperada.

### 4. Fórmulas a considerar

Esperanza discreta:

$$
E[X]=\sum_{x\in R_X}x\,p_X(x)
$$

Esperanza continua:

$$
E[X]=\int_{-\infty}^{\infty}x\,f_X(x)\,dx
$$

Esperanza de una función:

$$
E[g(X)]=
\begin{cases}
\displaystyle\sum_x g(x)p_X(x), & X\text{ discreta},\\[4pt]
\displaystyle\int_{-\infty}^{\infty}g(x)f_X(x)\,dx, & X\text{ continua}.
\end{cases}
$$

Linealidad:

$$
E[aX+b]=aE[X]+b
$$

### 5. Conexión con el listado

- **Ejercicio 2:** calcula el ingreso esperado usando `Y=200X+300000`; puedes hallar primero `E[X]` y luego aplicar linealidad.
- **Ejercicio 3:** calcula `E[X]` para la distribución discreta de capacidades.
- **Ejercicios 5–9:** calculan esperanza de variables continuas integrando `x f_X(x)` en el soporte.

En [[Listado 4 523250 E y P_II_2026.pdf]]. La clase también muestra una transformación de salarios en [[Clase3_2026 (1).pdf]] (PDF, pp. 20–25).

---

## Tema 6 — Varianza, desviación estándar y cambio de escala

### 1. Resumen

La **varianza** mide la dispersión de la distribución alrededor de su media. Es el promedio de las desviaciones cuadráticas respecto de la esperanza. La **desviación estándar** es la raíz de la varianza y queda expresada en las mismas unidades que `X`.

Al cambiar la escala de una variable, la media y la dispersión no se transforman de la misma manera: sumar una constante desplaza la distribución, mientras que multiplicar por una constante también cambia su dispersión.

### 2. Preguntas

- ¿Por qué las desviaciones con signo no sirven directamente para medir dispersión?
- ¿Por qué se elevan al cuadrado las desviaciones en la definición de varianza?
- Si sumas 10 a todos los valores de `X`, ¿cambia la varianza?
- Si conviertes metros a centímetros, ¿qué ocurre con la desviación estándar?
- ¿Por qué la desviación estándar suele ser más fácil de interpretar que la varianza?

### 3. Profundizar

Procedimiento de cálculo:

1. Calcula `E[X]`.
2. Calcula la esperanza del cuadrado de las desviaciones, o usa la forma abreviada.
3. Para volver a las unidades originales, toma la raíz cuadrada y obtén `σ_X`.

La varianza siempre es no negativa. Es cero solo cuando `X` es constante con probabilidad 1. La varianza se expresa en unidades al cuadrado; la desviación estándar, en unidades de `X`.

Para `Y=aX+b`, el desplazamiento `b` no modifica la dispersión. El factor `a` multiplica la desviación estándar por `|a|` y la varianza por `a²`. El coeficiente de variación compara dispersión con escala mediante `σ_X/μ_X`; es útil principalmente cuando la media es positiva y la escala de razón tiene sentido.

### 4. Fórmulas a considerar

Definición:

$$
\operatorname{Var}(X)=E[(X-\mu_X)^2],\qquad \mu_X=E[X]
$$

Forma computacional equivalente:

$$
\operatorname{Var}(X)=E[X^2]-(E[X])^2
$$

Caso discreto:

$$
\operatorname{Var}(X)=\sum_x(x-\mu_X)^2p_X(x)
$$

Caso continuo:

$$
\operatorname{Var}(X)=\int_{-\infty}^{\infty}(x-\mu_X)^2f_X(x)\,dx
$$

Desviación estándar y transformación lineal:

$$
\sigma_X=\sqrt{\operatorname{Var}(X)},\qquad
\operatorname{Var}(aX+b)=a^2\operatorname{Var}(X),\qquad
\sigma_{aX+b}=|a|\sigma_X
$$

Coeficiente de variación:

$$
CV_X=\frac{\sigma_X}{\mu_X}
$$

### 5. Conexión con el listado

- **Ejercicios 2 y 3:** calculan varianza de variables discretas; compara la varianza con la desviación estándar para interpretar las unidades.
- **Ejercicio 4 (c):** pide esperanza, varianza y desviación estándar para el número de caras.
- **Ejercicios 5–9:** practican los mismos resúmenes para densidades continuas.

En [[Listado 4 523250 E y P_II_2026.pdf]]. La clase desarrolla la definición y ejemplos de varianza en [[Clase3_2026 (1).pdf]] (PDF, pp. 26–29).

---

## Estrategia para resolver ejercicios del capítulo

### Si la variable es discreta

1. Define `X` en una frase y escribe su recorrido.
2. Construye una tabla con columnas `x` y `p_X(x)`.
3. Verifica `p_X(x) ≥ 0` y `Σ p_X(x)=1`.
4. Traduce la pregunta a una suma de probabilidades o a una esperanza.
5. Si piden la FDA, acumula las probabilidades en orden creciente de `x`.
6. Calcula `E[X]`, luego `E[X²]` y `Var(X)=E[X²]-(E[X])²`.
7. Interpreta el resultado y sus unidades.

### Si la variable es continua

1. Escribe el soporte donde `f_X(x)` no es cero.
2. Comprueba no negatividad e integral total 1; encuentra constantes desconocidas.
3. Representa la probabilidad pedida como una integral con límites correctos.
4. Si piden la FDA, integra desde menos infinito y define por tramos cuando corresponda.
5. Calcula media y segundo momento integrando `x f_X(x)` y `x² f_X(x)`.
6. Obtén varianza, desviación estándar y una interpretación con unidades.

## Errores que conviene vigilar

- Confundir `p_X(x)` con `P(X≤x)` o con `P(X=x)`.
- Usar una suma para una variable continua o una integral para una tabla discreta.
- Olvidar que la suma de masas o el área total de una densidad debe ser 1.
- Integrar sobre valores fuera del soporte o no separar una función definida por tramos.
- Calcular `E[g(X)]` como `g(E[X])` sin que corresponda.
- Calcular la varianza como `E[X²]` y olvidar restar `(E[X])²`.
- Reportar la varianza con las unidades de `X`; sus unidades son al cuadrado.
- En una FDA, perder los signos de desigualdad o dejar fuera los saltos de una distribución discreta.

## Contenido adicional del Listado 4

El Listado 4 incluye al final desigualdades de Markov y Chebyshev. Son herramientas para acotar probabilidades usando momentos; se presentan como una extensión del listado y no como uno de los ejes centrales de esta nota de la Clase 3.
