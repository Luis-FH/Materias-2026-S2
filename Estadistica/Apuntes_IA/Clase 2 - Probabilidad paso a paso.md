# Clase 2 — Probabilidad, paso a paso

#certamen1_estadistica

> [!info] Fuentes y conexiones
> - [[Clase2_2026.pdf]] — presentación de probabilidad.
> - [[Listado 3 523250 E y P_II_2026.pdf]] — práctica de probabilidad condicional, conjunta, total y Bayes.
> - [[Solucionario - Listado 3]] — resolución paso a paso.
> - [[Guia_Conceptos_y_Ejercicios_Probabilidad.pdf]] — repaso de conceptos y ejercicios de probabilidad.
> - [[Lamina_Graficos_Probabilidad-v2.pdf]] — apoyo visual para gráficos de probabilidad.
> - Índice del ramo: Estadística.

## Mapa de la clase

La idea es modelar una situación aleatoria, definir los eventos de interés y calcular probabilidades según la información disponible:

`experimento → espacio muestral → eventos → probabilidades → condicionamiento/relaciones → conclusión`

En cada tema: **resumen → preguntas → profundización → fórmulas → práctica**. Las preguntas son para intentar responder antes de mirar tus apuntes; esta nota no es una pauta resuelta.

---

## Tema 1 — Experimento, espacio muestral y eventos

### 1. Resumen

Un **experimento aleatorio** es un proceso cuyo resultado no se conoce de antemano. El **espacio muestral** (`Ω`) reúne todos los resultados posibles. Un **evento** (`A`) es un conjunto de resultados de `Ω`; ocurre cuando el resultado observado pertenece a ese conjunto.

Ejemplo: al lanzar dos dados, `Ω` contiene los pares ordenados `(i,j)`, con `i,j ∈ {1,…,6}`. El evento «la suma es 7» contiene los pares cuya suma es 7.

### 2. Preguntas

- ¿Qué resultado individual pertenece a `Ω` y qué condición define el evento?
- Al lanzar dos dados, ¿por qué `(2,5)` y `(5,2)` son resultados distintos?
- ¿Cómo expresarías «ocurre A o B», «ocurren ambos» y «no ocurre A»?

### 3. Profundizar

Antes de contar o calcular, define con precisión el experimento y qué cuenta como un resultado. Si importa el orden, los resultados ordenados no se deben combinar. Si dos eventos pueden ocurrir a la vez, su intersección no es vacía; si no pueden, son **mutuamente excluyentes**.

Las operaciones entre eventos convierten frases en conjuntos:

- **Unión** (`A ∪ B`): ocurre A, B o ambos.
- **Intersección** (`A ∩ B`): ocurren A y B.
- **Complemento** (`Aᶜ`): no ocurre A.
- **Diferencia** (`A \setminus B`): ocurre A, pero no B.

### 4. Fórmulas a considerar

No hay una fórmula de probabilidad todavía; primero se describe el evento:

$$
A \cup B,\qquad A \cap B,\qquad A^c,\qquad A \setminus B
$$

Si `A` y `B` son mutuamente excluyentes:

$$
A \cap B = \varnothing
$$

### 5. Enlace con el listado

En [[Listado 3 523250 E y P_II_2026.pdf]], identifica primero los eventos de los ejercicios 1, 3, 4 y 5 antes de aplicar fórmulas. El Listado 3 no dedica un ejercicio aislado a operaciones de conjuntos: esta base se usa en los cálculos posteriores.

**Referencia:** [[Clase2_2026.pdf]], espacio muestral y eventos (PDF, pp. 5–15).

---

## Tema 2 — Qué significa asignar una probabilidad

### 1. Resumen

Una probabilidad asigna a cada evento un número entre 0 y 1: `0` indica probabilidad nula y `1` un evento seguro. En un modelo finito equiprobable, probabilidad nula corresponde a un evento imposible. En un modelo clásico, se puede contar resultados favorables solo cuando todos los resultados elementales son igualmente probables. En otros casos, se necesitan probabilidades dadas por el contexto o estimadas a partir de frecuencias.

### 2. Preguntas

- ¿Es válido dividir «casos favorables» por «casos posibles» en cualquier experimento?
- Si un evento tiene probabilidad `0,2`, ¿qué representa ese número y qué no garantiza sobre un único intento?
- ¿Qué relación debe haber entre un evento y su complemento?

### 3. Profundizar

Las reglas básicas (axiomas) aseguran que las probabilidades sean coherentes. De ellas se derivan reglas prácticas para eventos complementarios y para eventos que pueden ocurrir simultáneamente.

La frecuencia relativa `n(A)/n` en muchos ensayos comparables puede ayudar a estimar `P(A)`, pero no convierte automáticamente los resultados en equiprobables. En problemas con información de tasas, tablas o condiciones, usa esos datos en vez de contar resultados como si tuvieran la misma probabilidad.

### 4. Fórmulas a considerar

**Modelo clásico**, solo si los resultados elementales son equiprobables:

$$
P(A)=\frac{|A|}{|\Omega|}
$$

**Axiomas y consecuencias:**

$$
P(\Omega)=1,\qquad 0\leq P(A)\leq 1
$$

$$
A\cap B=\varnothing \implies P(A\cup B)=P(A)+P(B)
$$

$$
P(A^c)=1-P(A)
$$

Para dos eventos cualesquiera:

$$
P(A\cup B)=P(A)+P(B)-P(A\cap B)
$$

### 5. Enlace con el listado

En [[Listado 3 523250 E y P_II_2026.pdf]], el ejercicio 2 entrega una tabla de frecuencias: decide primero cuál es el total relevante y qué celdas representan cada evento. Los ejercicios 3–5 entregan probabilidades del contexto, por lo que no se deben reemplazar por un conteo de resultados equiprobables.

**Referencia:** [[Clase2_2026.pdf]], axiomas y propiedades (PDF, pp. 28–30).

---

## Tema 3 — Probabilidad condicional

### 1. Resumen

`P(A | B)` se lee «probabilidad de A dado B». Calcula la probabilidad de A **restringiendo la atención a los casos donde B ya ocurrió**. El evento condicionante `B` pasa a ser la nueva referencia.

### 2. Preguntas

- Al conocer que B ocurrió, ¿qué casos dejan de ser posibles?
- ¿Por qué el denominador de `P(A | B)` es `P(B)` y no `P(A)`?
- ¿Es lo mismo `P(A | B)` que `P(B | A)`?

### 3. Profundizar

En una tabla, ubica primero la condición en el total de referencia. Para `P(A | B)`, cuenta los casos de `A ∩ B` y divídelos por todos los casos de `B`. Esto explica por qué invertir la condición suele cambiar el resultado.

La condición debe tener probabilidad positiva para usar la definición. Si una pregunta dice «dado que…», traduce esa frase con cuidado antes de elegir numerador y denominador.

### 4. Fórmulas a considerar

Para `P(B)>0`:

$$
P(A\mid B)=\frac{P(A\cap B)}{P(B)}
$$

De forma equivalente:

$$
P(A\cap B)=P(A\mid B)P(B)
$$

### 5. Enlace con el listado

- **Ejercicio 1:** compara la probabilidad de que el vuelo llegue a tiempo dado que salió a tiempo con la probabilidad de que haya salido a tiempo dado que llegó a tiempo. Son condiciones distintas.
- **Ejercicio 2 (a) y (b):** lee con cuidado cuál característica queda fijada y cuál se pregunta; los denominadores corresponden a márgenes diferentes de la tabla.

Ambos están en [[Listado 3 523250 E y P_II_2026.pdf]].

**Referencia:** [[Clase2_2026.pdf]], probabilidad condicional (PDF, pp. 35–38).

---

## Tema 4 — Probabilidad conjunta y regla multiplicativa

### 1. Resumen

La **probabilidad conjunta** `P(A ∩ B)` mide la probabilidad de que A y B ocurran ambos. La regla multiplicativa la relaciona con una probabilidad condicional: la probabilidad conjunta es la probabilidad de la condición multiplicada por la probabilidad del otro evento bajo esa condición.

### 2. Preguntas

- ¿Qué parte de la tabla representa que ocurran A y B a la vez?
- Si conoces `P(B)` y `P(A | B)`, ¿cómo reconstruyes la probabilidad conjunta?
- ¿Qué cambia en una secuencia de varios eventos si cada resultado modifica las probabilidades siguientes?

### 3. Profundizar

En la tabla del ejercicio 2, una celda interior representa la coincidencia de dos categorías; una fila o columna completa representa un total marginal. No confundas esos valores: la celda es conjunta, mientras que dividirla por un margen produce una condicional.

Para varios pasos, encadena las condiciones en el orden en que se observan. No supongas que cada paso conserva la misma probabilidad si el contexto cambia.

### 4. Fórmulas a considerar

$$
P(A\cap B)=P(A\mid B)P(B)=P(B\mid A)P(A)
$$

Para tres eventos, cuando las condicionales están definidas:

$$
P(A\cap B\cap C)=P(A)P(B\mid A)P(C\mid A\cap B)
$$

### 5. Enlace con el listado

- **Ejercicio 2:** distingue las celdas conjuntas de los totales y de las probabilidades condicionales que se obtienen a partir de ellos.
- **Ejercicio 3:** cada producto «probabilidad de una condición × probabilidad bajo esa condición» representa un caso conjunto; sumar los casos lleva al tema de probabilidad total.

Practica en [[Listado 3 523250 E y P_II_2026.pdf]].

**Referencia:** [[Clase2_2026.pdf]], probabilidad conjunta y regla multiplicativa (PDF, alrededor de pp. 39–42).

---

## Tema 5 — Independencia de eventos

### 1. Resumen

A y B son independientes si conocer que ocurrió uno no cambia la probabilidad del otro. La independencia es una relación probabilística, no significa que los eventos sean distintos ni que no puedan ocurrir juntos.

### 2. Preguntas

- Si A y B son independientes, ¿qué debería pasar con `P(A | B)` y `P(A)`?
- ¿Dos eventos mutuamente excluyentes pueden ser independientes si ambos tienen probabilidad positiva?
- ¿Qué diferencia hay entre decir «independientes» y decir «uno ocurre primero»?

### 3. Profundizar

Comprueba independencia con una igualdad de probabilidades, no por intuición ni porque los nombres de los eventos parezcan no relacionados. Si `P(B)>0`, comparar `P(A | B)` con `P(A)` es equivalente a comparar la probabilidad conjunta con el producto de las marginales.

Si A y B son mutuamente excluyentes y `P(A)>0`, entonces saber que A ocurrió hace imposible B; por tanto, no son independientes (salvo casos con probabilidad cero).

### 4. Fórmulas a considerar

Definición:

$$
P(A\cap B)=P(A)P(B)
$$

Si `P(B)>0`, forma equivalente:

$$
P(A\mid B)=P(A)
$$

### 5. Enlace con el listado

El [[Listado 3 523250 E y P_II_2026.pdf]] no plantea la independencia como ejercicio separado. En los ejercicios 1–5, úsala como una **comprobación**, no como una suposición: antes de multiplicar probabilidades marginales, verifica que el enunciado justifique independencia.

**Referencia:** [[Clase2_2026.pdf]], independencia de eventos (PDF, pp. 42–43).

---

## Tema 6 — Probabilidad total y teorema de Bayes

### 1. Resumen

La **probabilidad total** calcula la probabilidad de un resultado separando los distintos caminos o causas que pueden producirlo. **Bayes** invierte el condicionamiento: usa la evidencia observada para calcular la probabilidad de una causa o condición.

### 2. Preguntas

- ¿Qué conjunto de casos posibles se debe separar para usar probabilidad total?
- ¿Por qué cada término de la suma incluye tanto la probabilidad del caso como la probabilidad del resultado bajo ese caso?
- En Bayes, ¿qué es la evidencia observada y qué probabilidad se quiere actualizar?

### 3. Profundizar

Primero construye una partición: los casos `A₁,…,Aₖ` deben cubrir todo el espacio y no superponerse. Luego calcula la probabilidad del resultado `B` por cada caso y suma. Para Bayes, el denominador es precisamente esa probabilidad total de la evidencia; el numerador es la probabilidad conjunta del caso de interés y la evidencia.

En problemas de diagnóstico, por ejemplo, no basta con conocer la tasa de aciertos: también importa cuán frecuente es la condición antes de observar el resultado. Bayes combina ambas piezas.

### 4. Fórmulas a considerar

Si `A₁,…,Aₖ` forman una partición de `Ω`:

$$
P(B)=\sum_{i=1}^{k}P(B\mid A_i)P(A_i)
$$

Teorema de Bayes:

$$
P(A_j\mid B)=
\frac{P(B\mid A_j)P(A_j)}
{\sum_{i=1}^{k}P(B\mid A_i)P(A_i)}
$$

Para dos casos complementarios, `A` y `Aᶜ`:

$$
P(B)=P(B\mid A)P(A)+P(B\mid A^c)P(A^c)
$$

### 5. Enlace con el listado

- **Ejercicio 3:** separa los casos «llueve» y «no llueve» para calcular la probabilidad total de que el trabajo termine a tiempo; después, la pregunta inversa usa Bayes.
- **Ejercicios 4 y 5:** identifica los grupos o condiciones iniciales, calcula la probabilidad total de la evidencia y luego actualiza la probabilidad pedida con Bayes.

Practica en [[Listado 3 523250 E y P_II_2026.pdf]].

**Referencia:** [[Clase2_2026.pdf]], probabilidad total (PDF, p. 46) y Bayes (PDF, p. 49).

---

## Ruta corta para abordar un ejercicio

1. Define el experimento, el espacio muestral y los eventos.
2. Escribe qué se pide con notación: `P(A)`, `P(A ∩ B)` o `P(A | B)`.
3. Si aparece «dado que», fija primero el denominador.
4. Si hay varios grupos que cubren todos los casos, considera probabilidad total.
5. Si se pide una condición después de observar evidencia, considera Bayes.
6. Revisa que el resultado esté entre 0 y 1 y que responda exactamente a la pregunta.
