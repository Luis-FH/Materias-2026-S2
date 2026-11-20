---
materia: Mecánica
tipo: Apunte
capitulo: 6
tema: Fricción
fuente: "[[Practica_Fricción_solucion.pdf]]"
---

# Desarrollo teórico del solucionario: fricción

> [!info] Material relacionado
> - Solucionario: [[Practica_Fricción_solucion.pdf]]
> - Teoría del capítulo: [[C6-541271-2024.pdf]]
> - Ejercicios adicionales: [[Capítulo 6 - Fricción - Ejercicios complementarios]]
> - Evaluación relacionada: [[Apunte-Test 6]]
> - Índice de Mecánica: [[Mecanica]]

Este apunte desarrolla los dos ejercicios completos del solucionario que permiten reconstruir con claridad los datos y cálculos: el sistema de bloques sobre un plano inclinado y el bloque conectado a una cuerda que roza una superficie curva. El PDF también contiene páginas manuscritas; para esos desarrollos, consulta las imágenes del archivo fuente.

## 1. Ideas y fórmulas fundamentales

### 1.1 Fricción estática y cinética

La fuerza de fricción actúa tangencialmente a la superficie de contacto y se opone al movimiento relativo existente o que está a punto de comenzar.

Mientras no haya deslizamiento, la fricción estática se ajusta a lo que exija el equilibrio:

$$
0 \leq f_s \leq f_{s,\max} = \mu_s N
$$

Solo cuando el deslizamiento es inminente se alcanza el valor máximo:

$$
f_s = \mu_s N
$$

Si las superficies ya deslizan, se usa la fricción cinética:

$$
f_k = \mu_k N
$$

Donde $N$ es la fuerza normal y $\mu_s,\mu_k$ son los coeficientes de fricción estático y cinético, respectivamente. No se debe asignar automáticamente $f_s=\mu_s N$: primero hay que comprobar si el contacto está efectivamente en el umbral de deslizamiento.

### 1.2 Equilibrio

Para cada cuerpo aislado, se dibuja su diagrama de cuerpo libre (DCL) y se plantean las ecuaciones de equilibrio:

$$
\sum \vec{F} = \vec{0}
\qquad \text{y} \qquad
\sum M_O = 0
$$

En un plano inclinado de ángulo $\theta$, el peso $W=mg$ se descompone en:

$$
W_{\parallel} = mg\sin\theta,
\qquad
W_{\perp} = mg\cos\theta
$$

Si no hay otras fuerzas con componente normal, $N=mg\cos\theta$. En sistemas de varios bloques, la normal entre superficies puede incluir también las cargas transmitidas por otros bloques.

### 1.3 Cuerda o correa sobre una superficie curva

Para una cuerda a punto de deslizar sobre un cilindro o una superficie curva, la relación entre las tensiones extrema mayor y menor es:

$$
\frac{T_{\text{mayor}}}{T_{\text{menor}}}
= e^{\mu \beta}
\qquad \Longleftrightarrow \qquad
T_{\text{mayor}} = T_{\text{menor}} e^{\mu\beta}
$$

Aquí $\beta$ es el ángulo total de contacto, expresado en **radianes**. El lado de tensión mayor cambia según el sentido inminente del deslizamiento.

## 2. Ejercicio: tres bloques sobre un plano inclinado

### Datos y objetivo

El solucionario considera bloques de $30$, $50$ y $40\ \mathrm{kg}$ sobre un plano de $30^\circ$. Una fuerza $P$, paralela al plano, se aplica al bloque de $50\ \mathrm{kg}$; el de $30\ \mathrm{kg}$ está retenido por un cable. Los coeficientes estáticos son:

Se usa $g=9.81\ \mathrm{m/s^2}$.

| Contacto | $\mu_s$ |
|---|---:|
| Bloque de $30\ \mathrm{kg}$ con bloque de $50\ \mathrm{kg}$ | $0.30$ |
| Bloque de $50\ \mathrm{kg}$ con bloque de $40\ \mathrm{kg}$ | $0.40$ |
| Bloque de $40\ \mathrm{kg}$ con el plano | $0.45$ |

Se busca el máximo $P$ antes de que comience algún deslizamiento.

### Paso 1: determinar las normales

Se toma el eje paralelo al plano para las fuerzas tangenciales y el eje perpendicular para las normales. El peso de cada bloque aporta una componente $mg\cos 30^\circ$ en la dirección normal.

Para el bloque superior:

$$
N_1 = 30g\cos 30^\circ \approx 255\ \mathrm{N}
$$

Para el contacto entre los bloques de $30$ y $50\ \mathrm{kg}$, la carga normal soportada incluye ambos pesos:

$$
N_2 = N_1 + 50g\cos 30^\circ \approx 680\ \mathrm{N}
$$

Para el contacto inferior con el plano, la normal soporta los tres bloques:

$$
N_3 = N_2 + 40g\cos 30^\circ \approx 1019\ \mathrm{N}
$$

### Paso 2: calcular los máximos de fricción

En cada contacto, el máximo estático es $f_{s,\max}=\mu_sN$:

$$
\begin{aligned}
f_{1,\max} &= 0.30(255) \approx 76.5\ \mathrm{N} \\
f_{2,\max} &= 0.40(680) \approx 272\ \mathrm{N} \\
f_{3,\max} &= 0.45(1019) \approx 459\ \mathrm{N}
\end{aligned}
$$

Estos son límites superiores, no necesariamente los valores reales de fricción en todos los contactos.

### Paso 3: probar un primer modo de movimiento

Se prueba la hipótesis de que el bloque de $50\ \mathrm{kg}$ comienza a deslizar respecto de sus dos vecinos mientras el de $40\ \mathrm{kg}$ permanece en reposo. En ese caso, los dos contactos del bloque de $50\ \mathrm{kg}$ estarían en sus límites:

$$
f_1 = 76.5\ \mathrm{N},
\qquad
f_2 = 272\ \mathrm{N}
$$

Con el eje positivo hacia arriba del plano, el equilibrio tangencial del bloque de $50\ \mathrm{kg}$ da:

$$
P + 50g\sin 30^\circ - f_1 - f_2 = 0
$$

$$
P \approx 103\ \mathrm{N}
$$

Pero esta hipótesis debe verificarse con el bloque de $40\ \mathrm{kg}$. Para mantenerlo en reposo, el contacto con el plano tendría que proporcionar:

$$
f_3 = f_2 + 40g\sin 30^\circ
\approx 272 + 196
= 468\ \mathrm{N}
$$

Como $468\ \mathrm{N} > f_{3,\max}\approx459\ \mathrm{N}$, el plano no puede sostener ese estado. Por lo tanto, el modo de movimiento supuesto no es posible: el deslizamiento comienza primero en el contacto entre el bloque de $40\ \mathrm{kg}$ y el plano.

### Paso 4: resolver el modo de movimiento posible

En el inicio del deslizamiento inferior, la fricción entre el bloque de $40\ \mathrm{kg}$ y el plano sí alcanza su máximo:

$$
f_3 = f_{3,\max} \approx 459\ \mathrm{N}
$$

El equilibrio del bloque de $40\ \mathrm{kg}$ permite obtener la fricción requerida entre los bloques de $50$ y $40\ \mathrm{kg}$:

$$
f_2 + 40g\sin 30^\circ - f_3 = 0
$$

$$
f_2 \approx 459 - 196 = 263\ \mathrm{N}
$$

La comprobación es esencial:

$$
f_2 \approx 263\ \mathrm{N}
<
f_{2,\max}\approx272\ \mathrm{N}
$$

Así, los bloques de $50$ y $40\ \mathrm{kg}$ pueden moverse juntos, sin deslizar entre sí, mientras el bloque inferior comienza a deslizar sobre el plano.

Finalmente, para el bloque de $50\ \mathrm{kg}$:

$$
P + 50g\sin 30^\circ - f_1 - f_2 = 0
$$

$$
P \approx 76.5 + 263 - 245 \approx 94\ \mathrm{N}
$$

El solucionario reporta $P=93.8\ \mathrm{N}$; la pequeña diferencia con el cálculo redondeado anterior se debe a las aproximaciones intermedias. Se conserva como resultado:

$$
\boxed{P_{\max} \approx 93.8\ \mathrm{N}}
$$

### Qué enseña este ejercicio

- En un sistema con varios contactos, cada interfaz tiene su propio límite $\mu_sN$.
- Se debe comprobar cada modo de deslizamiento posible; no basta con suponer que todos los contactos llegan simultáneamente al máximo.
- Una fricción calculada debe ser menor o igual que su máximo. Si lo supera, la hipótesis de equilibrio es físicamente imposible.
- La fricción estática en un contacto puede ser menor que $\mu_sN$, como ocurre aquí con $f_2\approx263\ \mathrm{N}$.

## 3. Ejercicio: bloque, cuerda y superficie curva

### Datos y objetivo

Una barra uniforme de $9\ \mathrm{kg}$ determina la tensión $T_A$ en un extremo de la cuerda. La cuerda abraza una superficie curva con ángulo total de $30^\circ+40^\circ=70^\circ$. El coeficiente estático cuerda-superficie es $\mu_s=0.20$, y el bloque está sobre un plano de $40^\circ$, con $\mu_s=0.40$. Se busca el intervalo de masas $m$ para que el sistema permanezca en equilibrio.

Se usa $g=9.81\ \mathrm{m/s^2}$.

### Paso 1: obtener la tensión de la barra

Se toma momento respecto del pivote $O$, de modo que las reacciones del pivote no aparecen en la ecuación. Usando los brazos de momento del diagrama del solucionario:

$$
-T_A\left(\frac{2L}{3}\cos35^\circ\right)
+9g\left(\frac{L}{2}\cos25^\circ\right)
=0
$$

Al despejar:

$$
T_A
=
\frac{9g\left(\frac{L}{2}\cos25^\circ\right)}
{\left(\frac{2L}{3}\cos35^\circ\right)}
\approx 73.3\ \mathrm{N}
$$

La longitud $L$ se cancela, por lo que no es necesario conocer su valor.

### Paso 2: expresar el ángulo de contacto en radianes

El ángulo de contacto total es:

$$
\beta = 70^\circ\left(\frac{\pi}{180^\circ}\right)
= \frac{7\pi}{18}
\approx 1.222\ \mathrm{rad}
$$

La relación de tensiones en el límite de deslizamiento es:

$$
e^{\mu_s\beta}
= e^{0.20(1.222)}
\approx 1.277
$$

Según cuál extremo tenga mayor tensión, la tensión asociada al bloque toma uno de estos valores límite:

$$
T_1 = \frac{T_A}{e^{\mu_s\beta}}
\approx 57.4\ \mathrm{N},
\qquad
T_2 = T_Ae^{\mu_s\beta}
\approx 93.5\ \mathrm{N}
$$

No se intercambian arbitrariamente $T_1$ y $T_2$: se elige el caso que corresponde al sentido inminente del movimiento.

### Paso 3: hallar el límite cuando la masa tiende a subir

Si el bloque está a punto de subir por el plano, la fricción del plano apunta hacia abajo. La tensión en el lado del bloque es la menor, $T_1$. La normal vale:

$$
N = mg\cos40^\circ
$$

El equilibrio tangencial en el umbral de movimiento es:

$$
T_1 - mg\sin40^\circ - \mu_sN = 0
$$

Sustituyendo $N=mg\cos40^\circ$:

$$
m_{\min}
=
\frac{T_1}
{g\left(\sin40^\circ+0.40\cos40^\circ\right)}
\approx 6.16\ \mathrm{kg}
$$

### Paso 4: hallar el límite cuando la masa tiende a bajar

Si el bloque está a punto de bajar, la fricción del plano apunta hacia arriba. Ahora la tensión del lado del bloque es la mayor, $T_2$:

$$
T_2 + \mu_sN - mg\sin40^\circ = 0
$$

Por lo tanto:

$$
m_{\max}
=
\frac{T_2}
{g\left(\sin40^\circ-0.40\cos40^\circ\right)}
\approx 28.3\ \mathrm{kg}
$$

El denominador es positivo, así que este límite es físicamente consistente.

### Resultado

El sistema permanece en equilibrio estático para:

$$
\boxed{6.16\ \mathrm{kg} \leq m \leq 28.3\ \mathrm{kg}}
$$

En los extremos, una de las interfaces está al límite de deslizamiento. Entre ambos límites, las fricciones estáticas toman los valores necesarios para conservar el equilibrio.

## 4. Procedimiento recomendado para ejercicios de fricción

1. Aislar cada cuerpo o bloque que tenga un movimiento relativo distinto y dibujar su DCL.
2. Elegir ejes convenientes; en planos inclinados, usar ejes paralelo y perpendicular al plano.
3. Determinar las normales mediante el equilibrio perpendicular antes de calcular los límites de fricción.
4. Asignar a cada fricción una dirección que se oponga al movimiento relativo inminente, no simplemente al movimiento global del sistema.
5. Escribir $f_s\leq\mu_sN$ para contactos que siguen adheridos y usar $f_s=\mu_sN$ solo en los contactos al umbral.
6. Si hay varias formas posibles de deslizar, resolver y verificar cada modo contra los límites de todos los contactos.
7. Para cuerdas sobre superficies curvas, convertir el ángulo de contacto a radianes y decidir cuál lado tiene la tensión mayor según el sentido inminente.
8. Revisar signos, unidades y coherencia física de los resultados.

## 5. Errores frecuentes

- Suponer que toda fricción estática vale su máximo.
- Omitir las fuerzas normales transmitidas por otros bloques.
- Confundir el sentido del movimiento inminente de un bloque con el de la fricción que actúa sobre él.
- Aceptar una solución aunque una fricción requerida exceda $\mu_sN$.
- Usar grados directamente en el exponente $e^{\mu\beta}$.
- Aplicar la misma orientación de las tensiones de la cuerda en ambos sentidos de movimiento.

---

Siguiente lectura: [[Capítulo 6 - Fricción - Ejercicios complementarios]] · Fuente de los ejercicios: [[Practica_Fricción_solucion.pdf]]
