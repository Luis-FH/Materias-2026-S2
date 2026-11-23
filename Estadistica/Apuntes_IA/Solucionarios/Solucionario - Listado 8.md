---
seguimiento_certamen2: true
bloque_certamen2: "Intervalos"
progreso_certamen2: false
---

# Solucionario — Listado 8: Intervalos de confianza para comparar dos grupos

#certamen2_estadistica

**Fuente:** [[Ayudantia_Intervalos_de_Confianza_2.pdf]] (Guía de dos páginas; resolución completa de los 4 ejercicios).

**Recursos directos:** [[Clase5_2026.pdf]], [[Resumen_intervalos_de_confianza.pdf]] y [[Tablas Estadísticas.pdf]].

**Nota de identificación:** Corresponde al **Listado 8** de la asignatura (Intervalos de confianza para comparar dos poblaciones: diferencia de medias en muestras independientes con varianzas desconocidas distintas/iguales, diferencia de proporciones y diferencia de medias en muestras pareadas).

---

## 1. Permeabilidad del concreto con dos contenidos de asfalto

**Enunciado:** Se mide la permeabilidad del concreto (en pulgadas por hora) preparado con dos porcentajes distintos de asfalto (3% y 7%). Los resultados de los especímenes evaluados son:
* 3% de asfalto: $1189, 840, 1020, 980$ ($n_1 = 4$).
* 7% de asfalto: $853, 900, 733, 785$ ($n_2 = 4$).

---

### a) Intervalo de confianza del 90% para la diferencia de medias ($\mu_{3\%} - \mu_{7\%}$)

#### 1. ¿Cómo se identifica en el enunciado?
* **Identificación del parámetro:** Se busca estimar la diferencia de promedios entre dos tratamientos o grupos independientes $\implies$ **Diferencia de medias poblacionales ($\mu_1 - \mu_2$)**, donde $\mu_1$ es la permeabilidad media con 3% de asfalto y $\mu_2$ con 7% de asfalto.
* **Identificación de los datos y tipo de diseño:**
  * Dos muestras pequeñas e independientes: $n_1 = 4$ especímenes y $n_2 = 4$ especímenes.
  * No se conocen las varianzas poblacionales $\sigma_1^2$ y $\sigma_2^2$.
  * Al calcular las varianzas muestrales a partir de los datos brutos, obtenemos $s_1^2 \approx 20636.92$ y $s_2^2 \approx 5420.92$. Se observa que la varianza del grupo al 3% es casi 4 veces mayor que la del grupo al 7%. No hay indicación de que las varianzas sean iguales.
  * Nivel de confianza solicitado: $90\% \implies 1 - \alpha = 0.90 \implies \alpha = 0.10 \implies \alpha/2 = 0.05$.

#### 2. ¿Por qué se usa esta solución en particular?
Se utiliza el **Intervalo de Confianza de Welch ($t$-Student con varianzas desconocidas y distintas: $\sigma_1^2 \neq \sigma_2^2$)**.
* **Justificación metodológica:**
  1. Las varianzas poblacionales verdaderas son desconocidas.
  2. Asumir varianzas iguales (método *pooled*) cuando la variabilidad muestral difiere notablemente ($20636.92$ vs $5420.92$) y las muestras son pequeñas compromete la precisión de los niveles de confianza.
  3. El procedimiento de **Welch-Satterthwaite** no asume igualdad de varianzas y calcula unos grados de libertad efectivos ($\nu$) ajustados según la dispersión y tamaño de cada grupo, garantizando inferencias robustas.

#### 3. Material Teórico y Fórmulas a usar
* **Estadísticos muestrales de cada grupo:**
  $$\bar{x}_1 = \frac{\sum x_{1i}}{n_1}, \quad s_1^2 = \frac{\sum (x_{1i} - \bar{x}_1)^2}{n_1 - 1}$$
  $$\bar{x}_2 = \frac{\sum x_{2i}}{n_2}, \quad s_2^2 = \frac{\sum (x_{2i} - \bar{x}_2)^2}{n_2 - 1}$$
* **Error Estándar de Welch ($SE$):**
  $$SE = \sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}$$
* **Grados de Libertad de Welch-Satterthwaite ($\nu$):**
  $$\nu = \frac{\left( \frac{s_1^2}{n_1} + \frac{s_2^2}{n_2} \right)^2}{\frac{(s_1^2 / n_1)^2}{n_1 - 1} + \frac{(s_2^2 / n_2)^2}{n_2 - 1}}$$
* **Fórmula del Intervalo de Confianza para $\mu_1 - \mu_2$:**
  $$IC_{1-\alpha}(\mu_1 - \mu_2) = (\bar{x}_1 - \bar{x}_2) \pm t_{1-\alpha/2,\ \nu} \cdot \sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}$$

#### 4. Desarrollo Paso a Paso

* **Paso 1: Cálculo de las medias y varianzas muestrales.**
  * *Grupo 1 (3% asfalto):*
    $$\sum x_{1i} = 1189 + 840 + 1020 + 980 = 4029 \implies \bar{x}_1 = \frac{4029}{4} = 1007.25 \text{ pulg/h}$$
    $$SS_1 = \sum (x_{1i} - 1007.25)^2 = (181.75)^2 + (-167.25)^2 + (12.75)^2 + (-27.25)^2 = 61910.75$$
    $$s_1^2 = \frac{61910.75}{4 - 1} = \frac{61910.75}{3} \approx 20636.9167$$

  * *Grupo 2 (7% asfalto):*
    $$\sum x_{2i} = 853 + 900 + 733 + 785 = 3271 \implies \bar{x}_2 = \frac{3271}{4} = 817.75 \text{ pulg/h}$$
    $$SS_2 = \sum (x_{2i} - 817.75)^2 = (35.25)^2 + (82.25)^2 + (-84.75)^2 + (-32.75)^2 = 16262.75$$
    $$s_2^2 = \frac{16262.75}{4 - 1} = \frac{16262.75}{3} \approx 5420.9167$$

  * *Diferencia de medias muestrales:*
    $$\bar{x}_1 - \bar{x}_2 = 1007.25 - 817.75 = 189.50 \text{ pulg/h}$$

* **Paso 2: Cálculo del Error Estándar ($SE$).**
  $$\frac{s_1^2}{n_1} = \frac{20636.9167}{4} = 5159.2292, \quad \frac{s_2^2}{n_2} = \frac{5420.9167}{4} = 1355.2292$$
  $$SE = \sqrt{5159.2292 + 1355.2292} = \sqrt{6514.4584} \approx 80.712195 \text{ pulg/h}$$

* **Paso 3: Cálculo de los grados de libertad de Welch ($\nu$) y cuantil $t$.**
  $$\nu = \frac{(6514.4584)^2}{\frac{(5159.2292)^2}{3} + \frac{(1355.2292)^2}{3}} = \frac{42438168.1}{\frac{26617645.9}{3} + \frac{1836646.2}{3}} = \frac{42438168.1}{8872548.6 + 612215.4} = \frac{42438168.1}{9484764.0} \approx 4.4744$$
  Para una confianza del $90\%$ ($\alpha = 0.10 \implies 1-\alpha/2 = 0.95$), mediante la distribución $t$-Student ajustada para $\nu = 4.4744$, el cuantil es $t_{0.95,\ 4.4744} \approx 2.0685$.

* **Paso 4: Cálculo del Margen de Error ($E$) y construcción del intervalo.**
  $$E = t_{0.95,\ 4.4744} \cdot SE = 2.0685 \cdot 80.712195 \approx 166.9532 \text{ pulg/h}$$
  $$IC_{90\%}(\mu_{3\%} - \mu_{7\%}) = 189.50 \pm 166.9532 = [189.50 - 166.9532,\ 189.50 + 166.9532]$$
  $$IC_{90\%}(\mu_{3\%} - \mu_{7\%}) = [22.55,\ 356.45] \text{ pulg/h}$$

#### 5. Interpretación y Conclusión Detallada
Con un $90\%$ de confianza, se estima que la permeabilidad media del concreto elaborado con un 3% de asfalto supera a la del concreto con un 7% de asfalto en una cantidad comprendida entre **22.55 y 356.45 pulgadas por hora**.
* **Conclusión estadística y física:** Como todo el intervalo contiene valores estrictamente positivos y el valor cero no está dentro del intervalo ($0 \notin [22.55, 356.45]$), existe evidencia estadísticamente significativa al nivel del 10% de significación de que una menor concentración de asfalto (3%) incrementa sustancialmente la permeabilidad promedio del concreto.

---

### b) Supuestos necesarios para la validez del método

#### 1. ¿Cómo se identifica en el enunciado?
* El enunciado pregunta explícitamente: "¿Qué supuestos son necesarios para construir este intervalo de confianza?"

#### 2. Explicación de los Supuestos Exigidos
1. **Independencia de las muestras y mediciones:** Se requiere que los especímenes preparados con 3% de asfalto sean independientes entre sí y totalmente independientes de los especímenes con 7% de asfalto.
2. **Normalidad en ambas poblaciones:** Al contar con muestras extremadamente pequeñas ($n_1 = 4$ y $n_2 = 4$), no es posible aplicar el Teorema del Límite Central. Es **estrictamente imprescindible** suponer que la permeabilidad en ambos tipos de concreto sigue una distribución poblacional Normal sin presencia de valores atípicos severos.
3. **Ausencia del supuesto de homocedasticidad:** Al emplear el intervalo de Welch, **NO se asume que las varianzas poblacionales sean iguales ($\sigma_1^2 = \sigma_2^2$)**, lo cual invalida la necesidad de igualar varianzas cuando los datos muestran dispersiones distintas.

---

## 2. Proporción de propietarios con al menos un accidente

**Enunciado:** En un estudio sobre accidentes de tránsito, se investiga la proporción de propietarios de automóviles que han tenido al menos un accidente en el último año, según el color del vehículo:
* Autos Rojos: De $n_1 = 100$ propietarios encuestados, $45$ reportaron al menos un accidente.
* Autos Blancos: De $n_2 = 200$ propietarios encuestados, $70$ reportaron al menos un accidente.

Construya un intervalo de confianza del 90% para la diferencia entre la proporción de propietarios de autos rojos y autos blancos que han sufrido al menos un accidente ($p_R - p_B$).

---

### 1. ¿Cómo se identifica en el enunciado?
* **Identificación del parámetro:** Se solicita estimar la "diferencia entre la proporción de propietarios..." $\implies$ **Diferencia de dos proporciones poblacionales ($p_R - p_B$)**.
* **Identificación de la información conocida:**
  * Grupo 1 (Autos rojos): Muestra $n_1 = 100$, exitos $X_1 = 45 \implies \hat{p}_R = \frac{45}{100} = 0.45$.
  * Grupo 2 (Autos blancos): Muestra $n_2 = 200$, exitos $X_2 = 70 \implies \hat{p}_B = \frac{70}{200} = 0.35$.
  * Nivel de confianza: $90\% \implies 1 - \alpha = 0.90 \implies \alpha = 0.10 \implies z_{0.95} = 1.6449$ (o $1.645$).

### 2. ¿Por qué se usa esta solución en particular?
Se utiliza el **Intervalo de Confianza $Z$ no combinado para la diferencia de proporciones en muestras independientes**.
* **Fundamento teórico:** Las dos muestras provienen de poblaciones distintas de propietarios (autos rojos vs autos blancos) y las respuestas son variables Bernoulli independientes (1: Tuvo accidente, 0: No tuvo accidente).
* **Uso del Error Estándar No Combinado:** En la *construcción de intervalos de confianza*, la dispersión de cada grupo se estima utilizando de forma independiente sus propias proporciones muestrales ($\hat{p}_R$ y $\hat{p}_B$).
* **Verificación de condiciones del TLC:**
  * $n_1 \hat{p}_R = 45 \ge 5, \quad n_1 (1-\hat{p}_R) = 55 \ge 5$
  * $n_2 \hat{p}_B = 70 \ge 5, \quad n_2 (1-\hat{p}_B) = 130 \ge 5$
  Dado que el número esperado de éxitos y fracasos en ambos grupos supera holgadamente el umbral de 5, la distribución de la diferencia de proporciones muestrales $(\hat{P}_R - \hat{P}_B)$ se aproxima a una distribución Normal.

### 3. Material Teórico y Fórmulas a usar
* **Estimadores puntuales de proporción:**
  $$\hat{p}_1 = \frac{X_1}{n_1}, \quad \hat{p}_2 = \frac{X_2}{n_2}$$
  $$\text{Diferencia puntual: } \hat{p}_1 - \hat{p}_2$$
* **Error Estándar no combinado ($SE$):**
  $$SE = \sqrt{\frac{\hat{p}_1(1-\hat{p}_1)}{n_1} + \frac{\hat{p}_2(1-\hat{p}_2)}{n_2}}$$
* **Fórmula del IC para la diferencia de proporciones:**
  $$IC_{1-\alpha}(p_1 - p_2) = (\hat{p}_1 - \hat{p}_2) \pm z_{1-\alpha/2} \cdot \sqrt{\frac{\hat{p}_1(1-\hat{p}_1)}{n_1} + \frac{\hat{p}_2(1-\hat{p}_2)}{n_2}}$$

#### 4. Desarrollo Paso a Paso

* **Paso 1: Cálculo de proporciones muestrales y su diferencia.**
  $$\hat{p}_R = \frac{45}{100} = 0.45, \quad \hat{p}_B = \frac{70}{200} = 0.35$$
  $$\hat{p}_R - \hat{p}_B = 0.45 - 0.35 = 0.10 \text{ (es decir, } 10\%\text{)}$$

* **Paso 2: Obtención del cuantil crítico Normal $z_{0.95}$.**
  Para $\alpha = 0.10 \implies 1-\alpha/2 = 0.95$, el cuantil de la Normal Estándar es $z_{0.95} \approx 1.644853$ (aproximado usualmente como $1.645$).

* **Paso 3: Cálculo del Error Estándar ($SE$) y Margen de Error ($E$).**
  $$SE = \sqrt{\frac{0.45 \cdot 0.55}{100} + \frac{0.35 \cdot 0.65}{200}} = \sqrt{\frac{0.2475}{100} + \frac{0.2275}{200}} = \sqrt{0.002475 + 0.0011375} = \sqrt{0.0036125} \approx 0.060104$$
  $$E = z_{0.95} \cdot SE = 1.644853 \cdot 0.060104 \approx 0.098862 \text{ (es decir, } 9.89\%\text{)}$$

* **Paso 4: Construcción del intervalo.**
  $$IC_{90\%}(p_R - p_B) = 0.10 \pm 0.098862 = [0.10 - 0.098862,\ 0.10 + 0.098862]$$
  $$IC_{90\%}(p_R - p_B) = [0.00114,\ 0.19886]$$
  Expresado en porcentaje: **[0.12%, 19.88%]** (o **0.0012 a 0.1988**).

#### 5. Interpretación y Conclusión Detallada
Con un $90\%$ de confianza, la diferencia entre la proporción de propietarios de autos rojos y de autos blancos que han sufrido al menos un accidente en el último año se estima entre **0.12 y 19.88 puntos porcentuales** (es decir, la probabilidad es entre un $0.12\%$ y un $19.88\%$ mayor en conductores de vehículos rojos).
* **Análisis contextual:** Como el intervalo queda íntegramente por encima de cero ($0.0012 > 0$), existe evidencia estadística al nivel del $90\%$ a favor de una mayor siniestralidad en autos rojos. Sin embargo, al estar el límite inferior sumamente próximo a cero, el efecto real podría ser tenue y refleja una margen amplio de incertidumbre que llega hasta 20 puntos porcentuales.

---

## 3. Tiempo de traslado según el medio de transporte

**Enunciado:** Se realiza un estudio para comparar el tiempo de traslado (en minutos) desde el hogar al trabajo utilizando dos medios de transporte: automóvil particular y transporte público. Se obtienen los siguientes datos muestrales:
* Automóvil ($n_1 = 35$): Media muestral $\bar{x}_1 = 32$ minutos, desviación estándar muestral $s_1 = 5$ minutos.
* Transporte Público ($n_2 = 27$): Media muestral $\bar{x}_2 = 38$ minutos, desviación estándar muestral $s_2 = 8$ minutos.

Asuma que los tiempos de traslado en ambos grupos siguen distribuciones normales. Construya un intervalo de confianza del 95% para la diferencia entre los tiempos medios poblacionales de traslado ($\mu_{\text{auto}} - \mu_{\text{público}}$). ¿Existe evidencia de una diferencia en los tiempos medios?

---

### 1. ¿Cómo se identifica en el enunciado?
* **Identificación del parámetro:** Se solicita comparar los promedios de dos grupos independientes $\implies$ **Diferencia de medias poblacionales ($\mu_1 - \mu_2$)**.
* **Identificación de la información conocida:**
  * Grupo 1 (Auto): $n_1 = 35, \bar{x}_1 = 32, s_1 = 5 \implies s_1^2 = 25$.
  * Grupo 2 (Público): $n_2 = 27, \bar{x}_2 = 38, s_2 = 8 \implies s_2^2 = 64$.
  * Desviaciones estándar provienen de las *muestras* ($s_1$ y $s_2$), por lo que las varianzas poblacionales $\sigma_1^2, \sigma_2^2$ son **desconocidas**.
  * Las varianzas muestrales difieren considerablemente ($25$ frente a $64$).
  * Nivel de confianza: $95\% \implies 1 - \alpha = 0.95 \implies \alpha = 0.05 \implies t_{0.975,\ \nu}$.

### 2. ¿Por qué se usa esta solución en particular?
Se utiliza el **Intervalo de Confianza de Welch ($t$-Student con varianzas desconocidas distintas)**.
* **Elección del método:** Como no conocemos las varianzas poblacionales reales y las varianzas de la muestra difieren sensiblemente ($s_2^2 = 64$ es más del doble de $s_1^2 = 25$), el método más riguroso sugerido por la teoría del ramo es el método de Welch sin asumir igualdad de varianzas.

### 3. Material Teórico y Fórmulas a usar
* **Diferencia de medias muestrales:** $\bar{x}_1 - \bar{x}_2$
* **Error Estándar de Welch ($SE$):**
  $$SE = \sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}$$
* **Grados de Libertad de Welch ($\nu$):**
  $$\nu = \frac{\left( \frac{s_1^2}{n_1} + \frac{s_2^2}{n_2} \right)^2}{\frac{(s_1^2 / n_1)^2}{n_1 - 1} + \frac{(s_2^2 / n_2)^2}{n_2 - 1}}$$
* **Fórmula del IC:**
  $$IC_{1-\alpha}(\mu_1 - \mu_2) = (\bar{x}_1 - \bar{x}_2) \pm t_{1-\alpha/2,\ \nu} \cdot SE$$

#### 4. Desarrollo Paso a Paso

* **Paso 1: Cálculo de la diferencia muestral y del Error Estándar ($SE$).**
  $$\bar{x}_1 - \bar{x}_2 = 32 - 38 = -6 \text{ minutos}$$
  $$\frac{s_1^2}{n_1} = \frac{25}{35} \approx 0.714286, \quad \frac{s_2^2}{n_2} = \frac{64}{27} \approx 2.370370$$
  $$SE = \sqrt{0.714286 + 2.370370} = \sqrt{3.084656} \approx 1.756319 \text{ minutos}$$

* **Paso 2: Obtención de los grados de libertad de Welch ($\nu$) y cuantil $t$.**
  $$\nu = \frac{(3.084656)^2}{\frac{(0.714286)^2}{34} + \frac{(2.370370)^2}{26}} = \frac{9.515104}{\frac{0.510204}{34} + \frac{5.618656}{26}} = \frac{9.515104}{0.015006 + 0.216102} = \frac{9.515104}{0.231108} \approx 41.17$$
  Para un $95\%$ de confianza con $\nu \approx 41.17$ grados de libertad: $t_{0.975,\ 41.17} \approx 2.0193$.

* **Paso 3: Cálculo del Margen de Error ($E$).**
  $$E = 2.0193 \cdot 1.756319 \approx 3.5465 \text{ minutos}$$

* **Paso 4: Construcción del intervalo.**
  $$IC_{95\%}(\mu_{\text{auto}} - \mu_{\text{público}}) = -6 \pm 3.5465 = [-6 - 3.5465,\ -6 + 3.5465]$$
  $$IC_{95\%}(\mu_{\text{auto}} - \mu_{\text{público}}) = [-9.55,\ -2.45] \text{ minutos}$$

#### 5. Interpretación y Conclusión Detallada
Con un $95\%$ de confianza, el tiempo medio de traslado en automóvil es menor que el tiempo medio en transporte público en un rango de entre **2.45 y 9.55 minutos** (es decir, la diferencia se halla entre $-9.55$ y $-2.45$ minutos).
* **Respuesta a la pregunta del enunciado:** **SÍ existe evidencia estadísticamente significativa de una diferencia en los tiempos medios al 95% de confianza**. Como todo el intervalo está compuesto por valores estrictamente negativos y **no incluye el cero ($0 \notin [-9.55, -2.45]$)**, se concluye que el tiempo de viaje en automóvil es significativamente menor que en transporte público.

---

## 4. Tiempo de limpieza antes y después de reorganizar las tareas

**Enunciado:** Un gerente de operaciones evalúa la efectividad de una nueva reorganización del trabajo para reducir el tiempo de limpieza (en minutos) en una planta industrial. Para evitar sesgos por variaciones diarias de carga de trabajo, se registran los tiempos de limpieza en las mismas $9$ jornadas industriales bajo el sistema antiguo (Antes) y el sistema reorganizado (Después). Las diferencias obtenidas por jornada ($D_i = \text{Antes}_i - \text{Después}_i$) son:
$$8,\ 7,\ 5,\ 9,\ 8,\ 8,\ 6,\ 9,\ 7$$
Asuma que la población de diferencias se distribuye normalmente. Construya un intervalo de confianza del 95% para la media de las diferencias ($\mu_D$).

---

### 1. ¿Cómo se identifica en el enunciado?
* **Identificación del diseño experimental:** **Muestras Pareadas / Datos Emparejados (Dependientes)**.
  * Clave en el enunciado: "se registran los tiempos de limpieza en las mismas 9 jornadas industriales bajo el sistema antiguo (Antes) y el sistema reorganizado (Después)".
  * No se trata de dos muestras independientes seleccionadas al azar; cada observación proviene del *mismo día industrial* evaluado en dos condiciones temporales distintas.
* **Identificación del parámetro:** Se busca estimar la media de las diferencias pareadas ($\mu_D = \mu_{\text{Antes}} - \mu_{\text{Después}}$).
* **Datos entregados:**
  * Número de pares: $n = 9$ días.
  * Serie de diferencias por día: $D_i$.
  * Supuesto de normalidad sobre la variable diferencia: $D \sim N(\mu_D, \sigma_D^2)$.
  * Confianza: $95\% \implies 1 - \alpha = 0.95 \implies t_{0.975,\ n-1=8} = 2.3060$.

### 2. ¿Por qué se usa esta solución en particular?
Se utiliza el **Intervalo de Confianza $t$-Student para Muestras Pareadas (Diferencias Pareadas)**.
* **Fundamento estadístico:** En un diseño pareado, al tomar la diferencia $D_i = X_{1i} - X_{2i}$ para cada par, el problema se simplifica a la estimación de la media de **una sola muestra de diferencias**.
* **Eliminación de variabilidad inter-unidad:** Este método remueve el efecto de la variabilidad entre las distintas jornadas (días con más o menos suciedad general) y se enfoca en el cambio intrajornada introducido por la reorganización.
* Como la varianza de las diferencias $\sigma_D^2$ es desconocida y $n = 9 < 30$, se recurre a la distribución $t$-Student con $n - 1 = 8$ grados de libertad.

### 3. Material Teórico y Fórmulas a usar
* **Media muestral de las diferencias ($\bar{d}$):**
  $$\bar{d} = \frac{\sum_{i=1}^n D_i}{n}$$
* **Varianza y Desviación Estándar muestral de las diferencias ($s_d^2$ y $s_d$):**
  $$s_d^2 = \frac{\sum_{i=1}^n (D_i - \bar{d})^2}{n - 1} = \frac{\sum D_i^2 - \frac{(\sum D_i)^2}{n}}{n - 1}, \quad s_d = \sqrt{s_d^2}$$
* **Error Estándar de la diferencia pareada ($SE_d$):**
  $$SE_d = \frac{s_d}{\sqrt{n}}$$
* **Fórmula del IC Pareado:**
  $$IC_{1-\alpha}(\mu_D) = \bar{d} \pm t_{1-\alpha/2,\ n-1} \cdot \frac{s_d}{\sqrt{n}}$$

#### 4. Desarrollo Paso a Paso

* **Paso 1: Cálculo de la media muestral de las diferencias ($\bar{d}$).**
  $$\sum_{i=1}^9 D_i = 8 + 7 + 5 + 9 + 8 + 8 + 6 + 9 + 7 = 67$$
  $$\bar{d} = \frac{67}{9} \approx 7.444444 \text{ minutos}$$

* **Paso 2: Cálculo de la varianza muestral ($s_d^2$) y desviación estándar ($s_d$).**
  $$\sum_{i=1}^9 D_i^2 = 8^2 + 7^2 + 5^2 + 9^2 + 8^2 + 8^2 + 6^2 + 9^2 + 7^2 = 64 + 49 + 25 + 81 + 64 + 64 + 36 + 81 + 49 = 513$$
  $$s_d^2 = \frac{513 - \frac{(67)^2}{9}}{9 - 1} = \frac{513 - \frac{4489}{9}}{8} = \frac{513 - 498.777778}{8} = \frac{14.222222}{8} \approx 1.777778$$
  $$s_d = \sqrt{1.777778} \approx 1.333333 \text{ minutos}$$

* **Paso 3: Obtención del Error Estándar ($SE_d$) y del cuantil $t_{0.975,\ 8}$.**
  $$SE_d = \frac{s_d}{\sqrt{n}} = \frac{1.333333}{\sqrt{9}} = \frac{1.333333}{3} \approx 0.444444 \text{ minutos}$$
  Para un $95\%$ de confianza con $n - 1 = 8$ grados de libertad: $t_{0.975,\ 8} = 2.3060$.

* **Paso 4: Cálculo del Margen de Error ($E$) y construcción del intervalo.**
  $$E = t_{0.975,\ 8} \cdot SE_d = 2.3060 \cdot 0.444444 \approx 1.024888 \text{ minutos}$$
  $$IC_{95\%}(\mu_D) = 7.444444 \pm 1.024888 = [7.444444 - 1.024888,\ 7.444444 + 1.024888]$$
  $$IC_{95\%}(\mu_D) = [6.4196,\ 8.4693] \text{ minutos} \approx [6.42,\ 8.47] \text{ minutos}$$

#### 5. Interpretación y Conclusión Detallada
Con un $95\%$ de confianza, se estima que la reorganización de las tareas de trabajo reduce el tiempo medio de limpieza en un promedio de **6.42 a 8.47 minutos** por jornada industrial.
* **Conclusión de efectividad operacional:** Dado que el intervalo se ubica íntegramente en valores positivos por encima de cero ($0 \notin [6.42, 8.47]$), existe evidencia estadísticamente significativa de que el nuevo esquema de trabajo logra disminuir de manera efectiva los tiempos de limpieza en la planta.

