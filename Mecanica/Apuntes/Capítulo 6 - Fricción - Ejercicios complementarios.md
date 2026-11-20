---
materia: Mecánica
tipo: Apunte
capitulo: 6
tema: Fricción
dificultad: Media
---

# Capítulo 6: ejercicios complementarios de fricción

> [!info] Ruta de estudio
> - Presentación: [[C6-541271-2024.pdf]]
> - Desarrollo del solucionario: [[Desarrollo del solucionario - Fricción]]
> - Solucionario original: [[Practica_Fricción_solucion.pdf]]
> - Repaso para la evaluación: [[Apunte-Test 6]]
> - Índice de Mecánica: [[Mecanica]]

Estos ejercicios amplían los ejemplos de la presentación y practican distintos aspectos del rozamiento seco: fricción estática y cinética, equilibrio en un plano inclinado, vuelco, cuñas y cables sobre tambores. Se incluyen desarrollos para que puedas revisar el procedimiento después de intentar cada problema.

Se usará $g=9.81\ \mathrm{m/s^2}$. En todos los casos, dibuja primero el diagrama de cuerpo libre (DCL) y determina las normales antes de calcular la fricción.

## Fórmulas para tener a mano

La fricción estática se ajusta al equilibrio hasta alcanzar su máximo:

$$
0\leq f_s\leq\mu_sN,
\qquad
f_{s,\max}=\mu_sN
$$

Si existe deslizamiento:

$$
f_k=\mu_kN
$$

Para una cuerda o correa a punto de deslizar sobre una superficie curva:

$$
\frac{T_{\mathrm{mayor}}}{T_{\mathrm{menor}}}=e^{\mu\beta}
$$

El ángulo de contacto $\beta$ se expresa en radianes. Para el vuelco de un bloque, se igualan los momentos respecto del borde que actúa como pivote.

## Ejercicio 1: ¿reposo o deslizamiento?

Un bloque de $12\ \mathrm{kg}$ está sobre una superficie horizontal. Los coeficientes son $\mu_s=0.40$ y $\mu_k=0.30$. Determina qué ocurre si se aplica una fuerza horizontal de $35\ \mathrm{N}$ y de $60\ \mathrm{N}$. En el segundo caso, calcula la aceleración.

### Desarrollo

La normal es:

$$
N=mg=12(9.81)=117.72\ \mathrm{N}
$$

El máximo de fricción estática vale:

$$
f_{s,\max}=0.40(117.72)=47.09\ \mathrm{N}
$$

**Caso $F=35\ \mathrm{N}$.** Como $F<f_{s,\max}$, el bloque no desliza. La fricción estática toma el valor necesario para equilibrar la fuerza:

$$
f_s=35\ \mathrm{N},
\qquad
a=0
$$

**Caso $F=60\ \mathrm{N}$.** Como $F>f_{s,\max}$, el reposo no es posible. Una vez que desliza, se usa fricción cinética:

$$
f_k=0.30(117.72)=35.32\ \mathrm{N}
$$

Aplicando la segunda ley de Newton en la dirección del movimiento:

$$
a=\frac{F-f_k}{m}
=\frac{60-35.32}{12}
=2.06\ \mathrm{m/s^2}
$$

**Respuesta:** con $35\ \mathrm{N}$ permanece en reposo; con $60\ \mathrm{N}$ desliza y acelera a $2.06\ \mathrm{m/s^2}$.

## Ejercicio 2: intervalo de equilibrio en un plano inclinado

Un bloque de $20\ \mathrm{kg}$ está sobre un plano de $25^\circ$. Se aplica una fuerza $F$ paralela al plano y dirigida hacia arriba. Los coeficientes son $\mu_s=0.35$ y $\mu_k=0.25$.

1. Determina el intervalo de $F$ para que el bloque pueda permanecer en reposo.
2. Si $F=10\ \mathrm{N}$, determina el sentido y la aceleración del movimiento.

### Desarrollo

La normal y el máximo de fricción estática son:

$$
N=mg\cos25^\circ
=20(9.81)\cos25^\circ
=177.82\ \mathrm{N}
$$

$$
f_{s,\max}=0.35N=62.24\ \mathrm{N}
$$

Tomando positivo hacia arriba del plano, el equilibrio tangencial requiere que la fricción pueda compensar la diferencia entre el peso paralelo al plano y $F$:

$$
\left|mg\sin25^\circ-F\right|\leq\mu_smg\cos25^\circ
$$

Despejando $F$:

$$
mg(\sin25^\circ-\mu_s\cos25^\circ)
\leq F\leq
mg(\sin25^\circ+\mu_s\cos25^\circ)
$$

$$
20.68\ \mathrm{N}\leq F\leq145.15\ \mathrm{N}
$$

Para $F=10\ \mathrm{N}$, la fuerza queda bajo el límite inferior, así que el bloque desliza **hacia abajo**. La fricción cinética apunta hacia arriba:

$$
f_k=\mu_kN=0.25(177.82)=44.45\ \mathrm{N}
$$

La aceleración hacia abajo resulta:

$$
a=\frac{mg\sin25^\circ-F-f_k}{m}
=1.42\ \mathrm{m/s^2}
$$

**Respuesta:** el equilibrio es posible si $20.68\leq F\leq145.15\ \mathrm{N}$. Para $F=10\ \mathrm{N}$, el bloque baja con aceleración $1.42\ \mathrm{m/s^2}$.

## Ejercicio 3: ¿desliza o vuelca primero?

Un bloque rectangular pesa $600\ \mathrm{N}$, tiene una base de $0.40\ \mathrm{m}$ y una altura de $0.60\ \mathrm{m}$. Una fuerza horizontal se aplica a la altura del borde superior. El coeficiente de fricción estática con el suelo es $\mu_s=0.50$. Determina si el bloque desliza o vuelca primero al aumentar la fuerza.

### Desarrollo

El deslizamiento comenzaría cuando la fuerza igualara la fricción estática máxima:

$$
F_{\mathrm{deslizamiento}}=\mu_sN
=0.50(600)=300\ \mathrm{N}
$$

Para el vuelco inminente, se toman momentos respecto del borde inferior hacia el que tiende a girar el bloque. El peso actúa a mitad de la base:

$$
F_{\mathrm{vuelco}}(0.60)
=600\left(\frac{0.40}{2}\right)
$$

$$
F_{\mathrm{vuelco}}=200\ \mathrm{N}
$$

Como $200\ \mathrm{N}<300\ \mathrm{N}$, se alcanza el vuelco antes que el deslizamiento. La fricción necesaria en ese instante es $200\ \mathrm{N}$, menor que su máximo de $300\ \mathrm{N}$, de modo que el contacto todavía puede evitar el deslizamiento.

**Respuesta:** el bloque vuelca primero, a $F=200\ \mathrm{N}$.

> [!tip] Criterio general
> Calcula por separado la fuerza que inicia el deslizamiento y la que inicia el vuelco. El modo asociado al menor valor ocurre primero.

## Ejercicio 4: cuña que eleva un bloque

Una cuña de $15^\circ$ se empuja hacia la derecha para elevar un bloque de $600\ \mathrm{N}$, guiado por paredes verticales lisas. La cara superior de la cuña desciende hacia la derecha. El coeficiente estático entre bloque y cuña es $\mu_1=0.40$, y entre cuña y suelo es $\mu_0=0.15$. Calcula la fuerza horizontal mínima para iniciar el movimiento de la cuña hacia la derecha y del bloque hacia arriba.

### Desarrollo

Al comenzar el movimiento, el bloque tiende a subir por la cara inclinada respecto de la cuña. Por eso, la fricción sobre el bloque apunta cuesta abajo a lo largo de la cara. En el umbral:

$$
f_1=\mu_1N_1
$$

El equilibrio vertical del bloque da:

$$
N_1\cos15^\circ-f_1\sin15^\circ-W=0
$$

Sustituyendo $f_1=\mu_1N_1$:

$$
N_1=
\frac{W}{\cos15^\circ-\mu_1\sin15^\circ}
=695.73\ \mathrm{N}
$$

La reacción vertical total transmitida por el bloque a la cuña es $W$, así que la normal del suelo es $N_0=W=600\ \mathrm{N}$. La fricción del suelo al umbral vale:

$$
f_0=\mu_0N_0=0.15(600)=90\ \mathrm{N}
$$

En horizontal, la fuerza aplicada debe vencer la fricción del suelo y la componente horizontal de las fuerzas de contacto entre el bloque y la cuña:

$$
P=f_0+N_1\sin15^\circ+f_1\cos15^\circ
$$

$$
P=90+695.73\sin15^\circ+
(0.40)(695.73)\cos15^\circ
=538.88\ \mathrm{N}
$$

**Respuesta:** $P_{\min}\approx539\ \mathrm{N}$.

## Ejercicio 5: tensión límite de una cuerda sobre un tambor

Una cuerda abraza un tambor fijo en un ángulo de $210^\circ$. El coeficiente de fricción estática es $\mu_s=0.30$. Si en el extremo de menor tensión actúan $120\ \mathrm{N}$, ¿qué tensión máxima puede sostener el otro extremo antes de deslizar?

### Desarrollo

Primero se convierte el ángulo a radianes:

$$
\beta=210^\circ\left(\frac{\pi}{180^\circ}\right)
=\frac{7\pi}{6}
=3.665\ \mathrm{rad}
$$

En el umbral de deslizamiento, la razón entre tensión mayor y menor es:

$$
\frac{T_{\mathrm{mayor}}}{120}
=e^{0.30(3.665)}
$$

Por lo tanto:

$$
T_{\mathrm{mayor}}
=120e^{0.30(3.665)}
=360.34\ \mathrm{N}
$$

**Respuesta:** la tensión máxima es aproximadamente $360\ \mathrm{N}$.

## Ejercicio 6: freno de banda

Una banda frena un tambor de radio $0.15\ \mathrm{m}$. El ángulo de contacto es $160^\circ$, el coeficiente de fricción cinética es $\mu_k=0.25$, y la tensión del lado flojo es $180\ \mathrm{N}$. Determina la tensión del lado tenso y el torque de frenado.

### Desarrollo

El tambor está girando, así que se usa el coeficiente cinético. El ángulo en radianes es:

$$
\beta=160^\circ\left(\frac{\pi}{180^\circ}\right)
=2.793\ \mathrm{rad}
$$

La ecuación de la banda da:

$$
T_{\mathrm{tenso}}
=T_{\mathrm{flojo}}e^{\mu_k\beta}
=180e^{0.25(2.793)}
=361.80\ \mathrm{N}
$$

El torque resultante sobre el tambor es la diferencia entre las tensiones multiplicada por el radio:

$$
M=(T_{\mathrm{tenso}}-T_{\mathrm{flojo}})r
=(361.80-180)(0.15)
=27.27\ \mathrm{N\,m}
$$

**Respuesta:** $T_{\mathrm{tenso}}\approx361.8\ \mathrm{N}$ y $M\approx27.3\ \mathrm{N\,m}$. El sentido del torque es el de frenado, opuesto al giro del tambor.

## Lista de comprobación

- ¿La fricción estática calculada es menor o igual que $\mu_sN$?
- ¿Solo igualé $f_s$ a $\mu_sN$ en el contacto al límite?
- ¿El sentido de cada fricción se opone al movimiento relativo inminente?
- ¿Separé los posibles modos de deslizamiento y vuelco?
- ¿Convertí el ángulo de contacto a radianes en la ecuación de la cuerda?
- ¿El resultado tiene unidades y sentido físico coherentes?

## Conexiones

- [[C6-541271-2024.pdf]]
- [[Desarrollo del solucionario - Fricción]]
- [[Practica_Fricción_solucion.pdf]]
- [[Pauta Test 6 - Fricción.pdf]]
- [[Apunte-Test 6]]
- [[Mecanica]]
