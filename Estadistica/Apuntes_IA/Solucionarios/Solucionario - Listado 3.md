# Solucionario — Listado 3

#certamen1_estadistica

**Fuente:** [[Listado 3 523250 E y P_II_2026.pdf]]  
**Material relacionado:** [[Clase 2 - Probabilidad paso a paso]]

## 1. Vuelos que salen y llegan a tiempo

Sean \(S\): “sale a tiempo” y \(L\): “llega a tiempo”. Se sabe que \(P(S)=0,83\), \(P(L)=0,82\) y \(P(S\cap L)=0,78\).

### a) Llegar a tiempo dado que salió a tiempo

\[
P(L\mid S)=\frac{P(L\cap S)}{P(S)}
=\frac{0,78}{0,83}\approx\boxed{0,9398}.
\]

La probabilidad es aproximadamente 93,98 %.

### b) Salir a tiempo dado que llegó a tiempo

\[
P(S\mid L)=\frac{P(S\cap L)}{P(L)}
=\frac{0,78}{0,82}\approx\boxed{0,9512}.
\]

La probabilidad es aproximadamente 95,12 %.

## 2. Peso del recubrimiento y rugosidad

La tabla de frecuencias es:

| Rugosidad | Recubrimiento alto | Recubrimiento bajo | Total |
|---|---:|---:|---:|
| Alta | 12 | 16 | 28 |
| Baja | 88 | 34 | 122 |
| **Total** | **100** | **50** | **150** |

### a) Rugosidad alta, dado recubrimiento alto

\[
P(\text{rugosidad alta}\mid\text{peso alto})
=\frac{12}{12+88}=\boxed{0,12}.
\]

### b) Peso alto, dada rugosidad alta

\[
P(\text{peso alto}\mid\text{rugosidad alta})
=\frac{12}{12+16}=\frac{3}{7}\approx\boxed{0,4286}.
\]

El denominador cambia porque cambia la condición.

## 3. Huelga y término de una autopista

Sean \(H\): ocurre huelga y \(T\): obra terminada a tiempo. Se tiene \(P(H)=0,6\), \(P(H^c)=0,4\), \(P(T\mid H)=0,35\) y \(P(T\mid H^c)=0,85\).

### a) Probabilidad de terminar a tiempo

Por probabilidad total:

\[
P(T)=P(T\mid H)P(H)+P(T\mid H^c)P(H^c)
=0,35(0,6)+0,85(0,4)=0,21+0,34=\boxed{0,55}.
\]

### b) Probabilidad de huelga, dado que terminó a tiempo

\[
P(H\mid T)=\frac{P(T\mid H)P(H)}{P(T)}
=\frac{0,35(0,6)}{0,55}
=\frac{0,21}{0,55}\approx\boxed{0,3818}.
\]

Es aproximadamente 38,18 %.

## 4. Auto propio y auto de la empresa

Sean \(P\): usa su auto propio y \(E\): usa el auto de la empresa. Se sabe \(P(P)=2/5=0,4\), \(P(E)=3/5=0,6\), \(P(T)=1/5=0,2\), y \(P(T\mid E)=1/4\).

Primero:

\[
P(T\cap E)=P(T\mid E)P(E)=\frac14\frac35=\frac3{20}=0,15.
\]

Como los dos autos son las únicas opciones, \(T=(T\cap P)\cup(T\cap E)\), unión disjunta. Por tanto:

\[
P(T\cap P)=0,2-0,15=0,05.
\]

### a) Llegar a tiempo dado que usó su propio auto

\[
P(T\mid P)=\frac{P(T\cap P)}{P(P)}
=\frac{0,05}{0,4}=\boxed{0,125}.
\]

### b) Usar el auto de la empresa dado que llegó a tiempo

\[
P(E\mid T)=\frac{P(T\cap E)}{P(T)}
=\frac{0,15}{0,2}=\boxed{0,75}.
\]

## 5. Detector de mentiras

Sea \(G\): persona culpable; \(I\): inocente; \(+\): detector dice “culpable”; y \(-\): detector dice “inocente”. Se interpreta la precisión indicada como \(P(+\mid G)=0,90\) y \(P(-\mid I)=0,95\). Además, \(P(G)=0,40\) y \(P(I)=0,60\). Así, \(P(+\mid I)=0,05\) y \(P(-\mid G)=0,10\).

### a) Inocente dado que el detector dice culpable

\[
P(I\mid +)
=\frac{P(+\mid I)P(I)}
{P(+\mid I)P(I)+P(+\mid G)P(G)}
=\frac{0,05(0,60)}{0,05(0,60)+0,90(0,40)}
=\frac{0,03}{0,39}
=\boxed{\frac1{13}\approx0,0769}.
\]

### b) Inocente o detector dice “inocente”

\[
P(I\cup -)=P(I)+P(-)-P(I\cap -).
\]

\[
P(-)=0,10(0,40)+0,95(0,60)=0,61,\qquad
P(I\cap -)=0,95(0,60)=0,57.
\]

\[
P(I\cup -)=0,60+0,61-0,57=\boxed{0,64}.
\]

Como comprobación, el complemento de \(I\cup-\) es \(G\cap+\), cuya probabilidad es \(0,4(0,9)=0,36\); entonces la unión vale \(1-0,36=0,64\).
