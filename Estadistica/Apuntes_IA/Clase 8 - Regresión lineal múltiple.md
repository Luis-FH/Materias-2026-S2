---
seguimiento_certamen2: true
bloque_certamen2: "Regresión"
progreso_certamen2: false
---

# Clase 8 — Regresión lineal múltiple

#certamen2_estadistica

> [!info] Fuentes y conexiones
> - [[Clase8_2026_regre_multiple.pdf]] — presentación de regresión múltiple (21 diapositivas).
> - [[Listado 10 523250 E y P_II_2026.pdf]] — el ejercicio 2 aplica regresión múltiple y compara modelos; el ejercicio 1 es de regresión simple.
> - [[Solucionario - Listado 10]] — desarrollo del listado y comparación de modelos.

## Idea central

La regresión lineal múltiple describe una variable respuesta `Y` mediante varias variables explicativas. Cada coeficiente de pendiente representa el cambio esperado en `Y` asociado a aumentar una variable en una unidad, **manteniendo fijas las demás variables del modelo**.

`definir respuesta y predictores → ajustar por MCO → evaluar el modelo global → evaluar coeficientes → comparar modelos → interpretar con cautela`

## Modelo y notación

Para `n` observaciones y `K` variables explicativas:

`Yᵢ = β₀ + β₁Xᵢ₁ + β₂Xᵢ₂ + ··· + βₖXᵢₖ + uᵢ`

- `β₀`: intercepto.
- `βⱼ`: cambio en la media de `Y` por una unidad adicional de `Xⱼ`, manteniendo constantes los otros predictores.
- `uᵢ`: variación no explicada por los predictores.
- `ŷᵢ`: valor ajustado; `ûᵢ = yᵢ − ŷᵢ`: residuo.

En notación matricial, `y = Xβ + u`. La primera columna de `X` contiene unos para estimar el intercepto. Los coeficientes de mínimos cuadrados ordinarios son:

`β̂ = (X′X)⁻¹X′y`

El valor ajustado es `ŷ = Xβ̂`. Con `k` predictores, la varianza residual se estima como:

`σ̂² = SCR / (n − k − 1)`, donde `SCR = Σᵢ (yᵢ − ŷᵢ)²`.

## Evaluación del modelo

La descomposición de variabilidad es `SCT = SCE + SCR`, donde `SCT` es la suma de cuadrados total, `SCE` la explicada por el modelo y `SCR` la residual. El coeficiente de determinación es:

`R² = SCE/SCT = 1 − SCR/SCT`.

`R²` es la proporción de variabilidad muestral de `Y` explicada por el modelo. No mide causalidad y no garantiza que el modelo prediga bien fuera de los datos observados. Al agregar predictores, `R²` no disminuye; por eso también se compara el `R²` ajustado:

`R² ajustado = 1 − (1 − R²)(n − 1)/(n − k − 1)`.

### Prueba global F

Evalúa si el conjunto de predictores aporta evidencia de relación lineal:

- `H₀: β₁ = ··· = βₖ = 0`.
- `H₁`: al menos una pendiente es distinta de cero.
- `F = (SCE/k) / (SCR/(n−k−1))`.

Un valor-p menor que el nivel de significación lleva a rechazar `H₀`; eso indica que al menos un predictor contribuye, pero no identifica por sí solo cuál.

### Pruebas individuales

Para cada predictor `j`, la prueba usual contrasta `H₀: βⱼ = 0` frente a `H₁: βⱼ ≠ 0`, usando el estadístico `t = (β̂ⱼ − 0)/SE(β̂ⱼ)`. La interpretación es condicional a los demás predictores incluidos. Un predictor no significativo no necesariamente es irrelevante en cualquier modelo: los predictores correlacionados pueden compartir información.

## Ejemplo de la presentación

Para el tiempo de servicio `Y`, el número de envases `X₁` y la distancia `X₂`, la salida del ajuste entrega:

`Ŷ = 2.309200 + 2.740369X₁ + 0.012440X₂`.

- Manteniendo fija la distancia, un envase adicional se asocia con un aumento estimado de `2.740369` unidades de `Y`.
- Manteniendo fijo el número de envases, una unidad adicional de distancia se asocia con un aumento estimado de `0.012440` unidades de `Y`.
- El intercepto es el valor ajustado cuando ambos predictores valen cero; solo es sustantivamente interpretable si esa situación tiene sentido en el contexto.
- La salida reporta `R² = 0.9811`, `R² ajustado = 0.9794` y `F(2,22) = 570.7`, con valor-p `< 2.2×10⁻¹⁶`. Se rechaza la hipótesis global de pendientes nulas al nivel usual de 5%.
- La tabla ANOVA informa suma de cuadrados de regresión `5969` y total `6084`; por diferencia, la suma de cuadrados residual es aproximadamente `115`.

## Conexión con el Listado 10

En el ejercicio 2, `Y` es la resistencia a la tracción y los predictores posibles son `X₁` a `X₆`. Para comparar las salidas A–F:

1. Escribe la ecuación de cada modelo usando solo los predictores incluidos.
2. Lee el valor-p de la prueba F para la significancia global y los valores-p individuales de las pendientes.
3. Considera el `R²` ajustado, la significancia, la cantidad de parámetros y el error residual; no elijas solamente por el mayor `R²`.
4. Interpreta cada pendiente condicionada a los demás predictores del modelo escogido.
5. Evalúa si el intercepto en el punto donde todos los predictores son cero tiene sentido dentro del rango observado.

El desarrollo numérico y la comparación de modelos están en [[Solucionario - Listado 10]].

## Errores frecuentes

- Interpretar una pendiente como efecto aislado sin decir «manteniendo los demás predictores constantes».
- Usar el valor-p global como si probara que todas las pendientes son significativas.
- Elegir un modelo solo por su `R²` sin considerar el ajuste por complejidad.
- Interpretar el intercepto fuera de un contexto plausible.
- Afirmar causalidad o extrapolar más allá del rango de los datos sin justificación.
