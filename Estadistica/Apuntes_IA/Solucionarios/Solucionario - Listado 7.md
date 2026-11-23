---
seguimiento_certamen2: true
bloque_certamen2: "Intervalos"
progreso_certamen2: false
---

# Solucionario — Listado 7: Intervalos de confianza para una muestra

#certamen2_estadistica

**Fuente:** [[Ayudantia_Intervalos_de_Confianza.pdf]].

**Recursos directos:** [[Clase5_2026.pdf]], [[Resumen_intervalos_de_confianza.pdf]] y [[Tablas Estadísticas.pdf]].

**Nota de identificación:** El encabezado interno del PDF de ayudantía dice «Listado 6»; formalmente en la planificación de la asignatura corresponde a **Listado 7** (Intervalos de confianza para una muestra: media con $\sigma$ conocida, tamaño muestral, hipótesis sobre la media, varianza poblacional y proporción).

---

## 1. Duración de cuentas de crédito

**Enunciado:** La duración de las cuentas de crédito de los clientes de una tienda se distribuye normalmente con una desviación estándar poblacional de $\sigma = 1500$ horas.

---

### a) Intervalo de confianza del 95% para la media poblacional

#### 1. ¿Cómo se identifica en el enunciado?
* **Identificación del parámetro a estimar:** El problema pide construir un intervalo de confianza para la "duración media" de la población ($\mu$).
* **Identificación de los datos y supuestos clave:**
  * **Población Normal:** El enunciado afirma explícitamente que la población de duraciones "se distribuye normalmente".
  * **Varianza poblacional conocida ($\sigma$):** Se indica que la desviación estándar de la *población* es $\sigma = 1500$ horas (no proviene de una muestra, sino que es un parámetro conocido).
  * **Datos muestrales:** Tamaño de muestra $n = 100$ clientes y media muestral $\bar{x} = 9900$ horas.
  * **Nivel de confianza:** $95\% \implies 1 - \alpha = 0.95 \implies \alpha = 0.05$.

#### 2. ¿Por qué se usa esta solución en particular?
Se aplica la fórmula del **Intervalo de Confianza $Z$ para la media con varianza conocida ($\sigma$)**.
* **Justificación teórica:** Dado que la variable aleatoria proviene de una distribución Normal con varianza poblacional $\sigma^2$ conocida, la variable pivote estandarizada:
  $$Z = \frac{\bar{X} - \mu}{\sigma / \sqrt{n}}$$
  sigue exactamente una distribución **Normal Estándar $N(0,1)$**, independientemente de si $n$ es grande o pequeño.
* **Elección de distribución:** No se utiliza la distribución $t$-Student porque esta última solo se emplea cuando la varianza poblacional $\sigma^2$ es desconocida y debe estimarse mediante la varianza muestral $s^2$.

#### 3. Material Teórico y Fórmulas a usar
* **Concepto clave:** Un intervalo de confianza para la media al nivel $100(1-\alpha)\%$ toma la estructura general:
  $$\text{Estimador Puntual} \pm \text{Margen de Error}$$
* **Fórmula explícita:**
  $$IC_{1-\alpha}(\mu) = \left[ \bar{x} - z_{1-\alpha/2} \cdot \frac{\sigma}{\sqrt{n}},\ \bar{x} + z_{1-\alpha/2} \cdot \frac{\sigma}{\sqrt{n}} \right]$$
  Donde:
  * $\bar{x} = 9900$ horas: Estimador puntual de la media poblacional $\mu$.
  * $SE = \frac{\sigma}{\sqrt{n}}$: Error estándar de la media muestral, que mide la variabilidad del estimador entre distintas muestras.
  * $z_{1-\alpha/2}$: Cuantil crítico de la distribución $N(0,1)$ que acumula una probabilidad de $1 - \alpha/2$ a la izquierda. Para una confianza del $95\%$ ($\alpha = 0.05$), se tiene $1 - \alpha/2 = 0.975 \implies z_{0.975} = 1.96$.
  * $E = z_{1-\alpha/2} \cdot \frac{\sigma}{\sqrt{n}}$: Margen de error del intervalo.

#### 4. Desarrollo Paso a Paso

* **Paso 1: Extracción y sistematización de los datos.**
  $$\bar{x} = 9900 \text{ horas}, \quad \sigma = 1500 \text{ horas}, \quad n = 100, \quad 1-\alpha = 0.95$$

* **Paso 2: Determinación del cuantil crítico de la distribución Normal.**
  Con un nivel de significación $\alpha = 0.05$, dividimos la cola en dos partes iguales ($\alpha/2 = 0.025$). Buscamos en la tabla de la Normal Estándar el valor $z$ tal que $P(Z \le z) = 0.975$:
  $$z_{0.975} = 1.96$$

* **Paso 3: Cálculo del Error Estándar ($SE$) y del Margen de Error ($E$).**
  $$SE = \frac{\sigma}{\sqrt{n}} = \frac{1500}{\sqrt{100}} = \frac{1500}{10} = 150 \text{ horas}$$
  $$E = z_{0.975} \cdot SE = 1.96 \cdot 150 = 294 \text{ horas}$$

* **Paso 4: Construcción y cálculo del intervalo.**
  $$IC_{95\%}(\mu) = 9900 \pm 294 = [9900 - 294,\ 9900 + 294] = [9606,\ 10194] \text{ horas}$$

#### 5. Interpretación y Conclusión Detallada
Con un nivel de confianza del $95\%$, se estima que la duración media poblacional de las cuentas de crédito de los clientes se encuentra entre **9606 horas y 10 194 horas**.
* **Interpretación frecuentista:** Si se extrajeran repetidamente muchas muestras aleatorias de tamaño $n = 100$ de esta misma población y se construyera un intervalo de confianza del $95\%$ para cada una, aproximadamente el $95\%$ de dichos intervalos contendrían el verdadero valor de la media poblacional $\mu$.

---

### b) Tamaño de muestra necesario para un error máximo de 772.5 horas con 99% de confianza

#### 1. ¿Cómo se identifica en el enunciado?
* **Identificación de la pregunta:** El problema solicita hallar el "tamaño de muestra" ($n$).
* **Restricciones entregadas:**
  * Margen de error máximo tolerado: $E = 772.5$ horas.
  * Nivel de confianza deseado: $99\% \implies 1 - \alpha = 0.99 \implies \alpha = 0.01$.
  * Desviación estándar poblacional: $\sigma = 1500$ horas.

#### 2. ¿Por qué se usa esta solución en particular?
Se obtiene despejando el tamaño muestral $n$ de la ecuación del margen de error del Intervalo de Confianza $Z$.
* **Fundamento matemático:** El margen de error viene dado por $E = z_{1-\alpha/2} \cdot \frac{\sigma}{\sqrt{n}}$. Despejando $\sqrt{n}$ y elevando al cuadrado ambos lados, se obtiene la expresión directa para $n$.
* **Criterio de redondeo estricto (Regla de la función Techo $\lceil \cdot \rceil$):** Como el tamaño de muestra debe ser un número entero de elementos/clientes y el enunciado exige que el error *no exceda* el valor máximo de $772.5$ horas, cualquier resultado decimal obliga a **redondear siempre hacia el entero inmediatamente superior**. Si se redondeara hacia abajo, el error real superaría ligeramente el máximo permitido.

#### 3. Material Teórico y Fórmulas a usar
* **Fórmula despejada para el tamaño de muestra $n$:**
  $$n = \left( \frac{z_{1-\alpha/2} \cdot \sigma}{E} \right)^2$$
  Donde:
  * Para una confianza del $99\%$ ($\alpha = 0.01$), la probabilidad acumulada a la izquierda es $1 - \alpha/2 = 0.995$.
  * Buscando en la tabla o distribución Normal Estándar: $z_{0.995} \approx 2.575829$ (comúnmente aproximado como $2.576$ o $2.575$).

#### 4. Desarrollo Paso a Paso

* **Paso 1: Identificación de insumos.**
  $$E = 772.5 \text{ horas}, \quad \sigma = 1500 \text{ horas}, \quad 1-\alpha = 0.99 \implies \alpha/2 = 0.005$$

* **Paso 2: Obtención del valor crítico $z_{0.995}$.**
  $$z_{0.995} \approx 2.575829$$

* **Paso 3: Sustitución en la fórmula y cálculo numérico.**
  $$n = \left( \frac{2.575829 \cdot 1500}{772.5} \right)^2 = \left( \frac{3863.7435}{772.5} \right)^2 = (5.00161)^2 \approx 25.0161$$

* **Paso 4: Análisis de precisión y aplicación del redondeo.**
  * Si se tomara $n = 25$, el margen de error real con el cuantil preciso sería:
    $$E_{real} = 2.575829 \cdot \frac{1500}{\sqrt{25}} = 2.575829 \cdot 300 = 772.75 \text{ horas}$$
    Dado que $772.75 > 772.5$, se incumpliría la condición de error máximo.
  * Por tanto, aplicando la función techo para garantizar el cumplimiento del error máximo:
    $$n = \lceil 25.0161 \rceil = 26 \text{ clientes}$$

#### 5. Interpretación y Conclusión Detallada
Para garantizar con un nivel de confianza del $99\%$ que el margen de error en la estimación de la duración media no supere las $772.5$ horas, se requiere seleccionar una muestra de al menos **26 clientes**.
* **Nota pedagógica sobre valores tabulados:** Si se utilizara el cuantil redondeado habitual de tabla $z_{0.995} = 2.575$, el cálculo daría $n = \left(\frac{2.575 \cdot 1500}{772.5}\right)^2 = 25.0006$, cuyo redondeo al entero superior arroja de forma consistente **$n = 26$ clientes**.

---

## 2. Puntaje promedio de establecimientos educacionales

**Enunciado:** En una muestra de $42$ establecimientos educacionales, se obtuvo un puntaje promedio de $107.6$ puntos en una prueba estandarizada. Asuma que la desviación estándar poblacional es $\sigma = 1.3$ puntos. Construya un intervalo de confianza del 95% para la media poblacional. Con base en este intervalo, ¿es plausible afirmar que el puntaje promedio de la población es de 110 puntos?

---

### 1. ¿Cómo se identifica en el enunciado?
* **Identificación del parámetro:** Se requiere estudiar el "puntaje promedio" poblacional ($\mu$).
* **Identificación de la información conocida:**
  * Muestra: $n = 42$ establecimientos.
  * Media muestral: $\bar{x} = 107.6$ puntos.
  * Desviación estándar de la población: $\sigma = 1.3$ puntos ($\sigma$ conocida).
  * Nivel de confianza: $95\% \implies 1 - \alpha = 0.95 \implies z_{0.975} = 1.96$.
* **Pregunta de decisión:** "¿Es plausible afirmar que el puntaje promedio de la población es de 110 puntos?" $\implies$ Inferencia sobre la compatibilidad de una hipótesis nula $H_0: \mu = 110$ con los datos observados.

### 2. ¿Por qué se usa esta solución en particular?
1. **Para la construcción del intervalo:** Se utiliza la fórmula del **Intervalo de Confianza $Z$ para la media con $\sigma$ conocida**. Aunque no se especifique la distribución de la población original, el **Teorema del Límite Central (TLC)** asegura que como el tamaño muestral $n = 42 \ge 30$ es suficientemente grande, la distribución de la media muestral $\bar{X}$ es aproximadamente Normal.
2. **Para la evaluación de plausibilidad ($\mu = 110$):** Existe una **relación de equivalencia dual entre los Intervalos de Confianza y las Pruebas de Hipótesis bilaterales**. Un valor constante $\mu_0$ es plausible para la media al nivel de significación $\alpha$ si y solo si $\mu_0$ pertenece al intervalo de confianza del $100(1-\alpha)\%$. Si $\mu_0$ queda fuera del intervalo, se rechaza la hipótesis $H_0: \mu = \mu_0$ al nivel $\alpha$.

### 3. Material Teórico y Fórmulas a usar
* **Fórmula del Intervalo de Confianza $Z$ para la media:**
  $$IC_{1-\alpha}(\mu) = \left[ \bar{x} - z_{1-\alpha/2} \cdot \frac{\sigma}{\sqrt{n}},\ \bar{x} + z_{1-\alpha/2} \cdot \frac{\sigma}{\sqrt{n}} \right]$$
* **Estadístico de prueba $z_{obs}$ (Contraste de hipótesis bilateral $H_0: \mu = 110$ vs $H_1: \mu \neq 110$):**
  $$z_{obs} = \frac{\bar{x} - \mu_0}{\sigma / \sqrt{n}}$$
  Criterio de rechazo al nivel del $5\%$: Rechazar $H_0$ si $|z_{obs}| > z_{0.975} = 1.96$.

### 4. Desarrollo Paso a Paso

* **Paso 1: Recopilación de parámetros y estadísticos.**
  $$n = 42, \quad \bar{x} = 107.6 \text{ puntos}, \quad \sigma = 1.3 \text{ puntos}, \quad 1-\alpha = 0.95 \implies z_{0.975} = 1.96$$

* **Paso 2: Cálculo del Error Estándar ($SE$) y del Margen de Error ($E$).**
  $$SE = \frac{\sigma}{\sqrt{n}} = \frac{1.3}{\sqrt{42}} \approx \frac{1.3}{6.480741} \approx 0.200593 \text{ puntos}$$
  $$E = z_{0.975} \cdot SE = 1.96 \cdot 0.200593 \approx 0.393162 \text{ puntos}$$

* **Paso 3: Construcción del Intervalo de Confianza del 95%.**
  $$IC_{95\%}(\mu) = 107.6 \pm 0.393162 = [107.6 - 0.393162,\ 107.6 + 0.393162]$$
  $$IC_{95\%}(\mu) = [107.2068,\ 107.9932] \text{ puntos}$$

* **Paso 4: Evaluación de la plausibilidad del valor $\mu = 110$.**
  * **Análisis mediante el Intervalo de Confianza:** El valor $110$ no se encuentra dentro del intervalo de confianza de $95\%$ ($110 \notin [107.2068, 107.9932]$), ya que el límite superior ($107.9932$) es estrictamente menor que $110$.
  * **Análisis mediante el Estadístico de Prueba Equivalente:**
    $$z_{obs} = \frac{107.6 - 110}{0.200593} = \frac{-2.4}{0.200593} \approx -11.9645$$
    Como $|z_{obs}| = 11.9645 \gg 1.96$, el valor observado está a casi 12 errores estándares de distancia de 110.

### 5. Interpretación y Conclusión Detallada
* El intervalo de confianza del $95\%$ para el puntaje promedio poblacional de los establecimientos es **[107.21, 107.99] puntos**.
* **Respuesta a la pregunta del enunciado:** **NO es plausible afirmar que el puntaje promedio de la población sea de 110 puntos**. Con un $95\%$ de confianza, la verdadera media poblacional es significativamente inferior a 110 puntos. Los datos muestrales proporcionan evidencia estadística abrumadora para rechazar dicha hipótesis.

---

## 3. Precios en ocho comercios

**Enunciado:** Los precios (en unidades de precio) de un determinado producto en $8$ comercios elegidos al azar fueron: $132, 125, 130, 139, 126, 138, 124, 140$. Asuma que la muestra proviene de una población normal.

---

### a) Intervalo de confianza del 95% para la varianza poblacional ($\sigma^2$)

#### 1. ¿Cómo se identifica en el enunciado?
* **Identificación del parámetro a estimar:** El enunciado solicita un intervalo para la "varianza poblacional" ($\sigma^2$).
* **Identificación de la información conocida:**
  * Muestra pequeña de datos brutos: $n = 8$ comercios.
  * Supuesto explícito sobre la población: "proviene de una población normal".
* **Identificación de la distribución de referencia:** Para la inferencia sobre la varianza $\sigma^2$ de una población Normal, la distribución correspondiente es la **Chi-cuadrado ($\chi^2$)**.

#### 2. ¿Por qué se usa esta solución en particular?
Se utiliza el **Intervalo de Confianza Chi-cuadrado para la varianza de una población Normal**.
* **Fundamento teórico:** La cantidad pivote construida mediante la varianza muestral $S^2$:
  $$V = \frac{(n-1)S^2}{\sigma^2} \sim \chi^2_{n-1}$$
  sigue exactamente una distribución Chi-cuadrado con $\nu = n-1$ grados de libertad, **condición válida únicamente si la población es Normal**.
* **Naturaleza asimétrica de la distribución:** A diferencia de la distribución Normal o $t$-Student, la distribución Chi-cuadrado es **asimétrica y estrictamente positiva**. Por este motivo, los cuantiles de cola inferior ($\chi^2_{\alpha/2}$) y cola superior ($\chi^2_{1-\alpha/2}$) son distintos en magnitud, y en la fórmula del intervalo el cuantil superior $\chi^2_{1-\alpha/2}$ divide al límite inferior, mientras que el cuantil inferior $\chi^2_{\alpha/2}$ divide al límite superior.

#### 3. Material Teórico y Fórmulas a usar
* **Fórmulas de estadísticos muestrales (Media y Varianza Muestral):**
  $$\bar{x} = \frac{\sum_{i=1}^n x_i}{n}$$
  $$s^2 = \frac{\sum_{i=1}^n (x_i - \bar{x})^2}{n - 1} = \frac{\sum_{i=1}^n x_i^2 - n\bar{x}^2}{n - 1}$$
* **Fórmula del Intervalo de Confianza para $\sigma^2$:**
  $$IC_{1-\alpha}(\sigma^2) = \left[ \frac{(n-1)s^2}{\chi^2_{1-\alpha/2,\ n-1}},\ \frac{(n-1)s^2}{\chi^2_{\alpha/2,\ n-1}} \right]$$
  Donde para un $95\%$ de confianza ($\alpha = 0.05$) con $n-1 = 7$ grados de libertad:
  * $\chi^2_{0.975,\ 7}$: Cuantil de cola izquierda $0.975$ (cuantil superior).
  * $\chi^2_{0.025,\ 7}$: Cuantil de cola izquierda $0.025$ (cuantil inferior).

#### 4. Desarrollo Paso a Paso

* **Paso 1: Cálculo de la media muestral ($\bar{x}$).**
  $$\sum_{i=1}^8 x_i = 132 + 125 + 130 + 139 + 126 + 138 + 124 + 140 = 1054$$
  $$\bar{x} = \frac{1054}{8} = 131.75$$

* **Paso 2: Cálculo de las desviaciones al cuadrado y la varianza muestral ($s^2$).**
  Calculamos las diferencias cuadráticas respecto a la media $\bar{x} = 131.75$:
  * $(132 - 131.75)^2 = (0.25)^2 = 0.0625$
  * $(125 - 131.75)^2 = (-6.75)^2 = 45.5625$
  * $(130 - 131.75)^2 = (-1.75)^2 = 3.0625$
  * $(139 - 131.75)^2 = (7.25)^2 = 52.5625$
  * $(126 - 131.75)^2 = (-5.75)^2 = 33.0625$
  * $(138 - 131.75)^2 = (6.25)^2 = 39.0625$
  * $(124 - 131.75)^2 = (-7.75)^2 = 60.0625$
  * $(140 - 131.75)^2 = (8.25)^2 = 68.0625$

  Suma de cuadrados de las diferencias ($SS$):
  $$SS = \sum_{i=1}^8 (x_i - \bar{x})^2 = 301.5$$
  Varianza muestral $s^2$:
  $$s^2 = \frac{301.5}{8 - 1} = \frac{301.5}{7} \approx 43.071428$$
  Nótese que el numerador de la fórmula $(n-1)s^2$ es exactamente igual al término $SS = 301.5$.

* **Paso 3: Obtención de los cuantiles de la distribución Chi-cuadrado ($\chi^2$) con 7 grados de libertad.**
  Para $\alpha = 0.05$ y $\nu = 7$:
  * $\chi^2_{0.975,\ 7} = 16.0128$ (cuantil superior de tabla)
  * $\chi^2_{0.025,\ 7} = 1.6899$ (cuantil inferior de tabla)

* **Paso 4: Sustitución y cálculo de los límites del intervalo.**
  $$Límite\ Inferior = \frac{(n-1)s^2}{\chi^2_{0.975,\ 7}} = \frac{301.5}{16.0128} \approx 18.8287$$
  $$Límite\ Superior = \frac{(n-1)s^2}{\chi^2_{0.025,\ 7}} = \frac{301.5}{1.6899} \approx 178.4129$$
  $$IC_{95\%}(\sigma^2) = [18.83,\ 178.42] \text{ unidades}^2$$

#### 5. Interpretación y Conclusión Detallada
Con un $95\%$ de confianza, la varianza poblacional de los precios del producto en los comercios se estima entre **18.83 y 178.42 unidades cuadradas**.
* **Extensión a la desviación estándar ($\sigma$):** Extrayendo la raíz cuadrada a ambos extremos del intervalo de la varianza, se obtiene el intervalo para la desviación estándar poblacional de los precios:
  $$IC_{95\%}(\sigma) = [\sqrt{18.8287},\ \sqrt{178.4129}] = [4.34,\ 13.36] \text{ unidades de precio}$$

---

### b) Intervalo de confianza del 95% para la proporción de precios menores o iguales a 130

#### 1. ¿Cómo se identifica en el enunciado?
* **Identificación del parámetro:** Se solicita estimar la "proporción" ($p$) de comercios que ofrecen el producto a un precio menor o igual a 130.
* **Identificación de los datos:**
  * Tamaño de muestra total: $n = 8$ comercios.
  * Conteo de "éxitos" (precios $x_i \le 130$): Revisando los datos brutos, los comercios con precio $\le 130$ son $125, 130, 126, 124 \implies X = 4$ comercios.
  * Proporción muestral observada: $\hat{p} = \frac{X}{n} = \frac{4}{8} = 0.5$.

#### 2. ¿Por me se usa esta solución en particular?
* **Método de Wald (Normal Aproximado):** Es la fórmula estándar enseñada en el curso para intervalos de proporción basados en el Teorema del Límite Central.
* **Análisis crítico del tamaño muestral y métodos alternativos:**
  * *Observación metodológica fundamental:* Para que la aproximación Normal de Wald sea altamente precisa, se requiere habitualmente la condición de muestra grande: $n\hat{p} \ge 5$ y $n(1-\hat{p}) \ge 5$. En este ejercicio se tiene $n\hat{p} = 4 < 5$ y $n(1-\hat{p}) = 4 < 5$, por lo que el tamaño muestral es reducido.
  * Por este motivo, se presenta el cálculo mediante la **fórmula de Wald** (esperada en la pauta oficial del curso) y se agrega la discusión de sus limitaciones frente al intervalo binomial exacto de **Clopper-Pearson**.

#### 3. Material Teórico y Fórmulas a usar
* **Proporción muestral ($\hat{p}$):**
  $$\hat{p} = \frac{X}{n}, \quad q = 1 - \hat{p}$$
* **Fórmula de Wald para el IC de una proporción:**
  $$IC_{1-\alpha}(p) = \hat{p} \pm z_{1-\alpha/2} \cdot \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$$
  Para una confianza del $95\%$: $z_{0.975} = 1.96$.

#### 4. Desarrollo Paso a Paso

* **Paso 1: Determinación de la proporción muestral.**
  $$n = 8, \quad X = 4 \implies \hat{p} = \frac{4}{8} = 0.5, \quad 1 - \hat{p} = 0.5$$

* **Paso 2: Cálculo del Error Estándar ($SE$).**
  $$SE = \sqrt{\frac{\hat{p}(1-\hat{p})}{n}} = \sqrt{\frac{0.5 \cdot 0.5}{8}} = \sqrt{\frac{0.25}{8}} = \sqrt{0.03125} \approx 0.176777$$

* **Paso 3: Cálculo del Margen de Error ($E$).**
  $$E = z_{0.975} \cdot SE = 1.96 \cdot 0.176777 \approx 0.346483 \text{ (es decir, } 34.65\%\text{)}$$

* **Paso 4: Construcción del intervalo.**
  $$IC_{95\%}(p) = 0.5 \pm 0.346483 = [0.5 - 0.346483,\ 0.5 + 0.346483] = [0.1535,\ 0.8465]$$
  En porcentaje: **[15.35%, 84.65%]**.

#### 5. Interpretación y Conclusión Detallada
* Mediante el método aproximado de Wald, con un $95\%$ de confianza se estima que la proporción de comercios con precios $\le 130$ se encuentra entre **15.35% y 84.65%**.
* **Discusión de resultados:** El intervalo resultante es muy amplio (abarca una amplitud de $69.3\%$). Esto refleja la alta incertidumbre derivada de contar con solo $8$ observaciones. Si se calcula el intervalo binomial exacto de Clopper-Pearson (adecuado para muestras pequeñas), se obtiene el rango **[15.70%, 84.30%]**, confirmando la baja precisión de estimación debido al tamaño restringido de la muestra.

