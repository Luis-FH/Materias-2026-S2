---
tags:
  - certamen1_termo
seguimiento_certamen1: true
progreso_certamen1: true
bloque_certamen1: Sustancias puras y tablas
---

# Práctico 3 — Propiedades de las sustancias puras

[Listado del práctico](../02_Ejercicios_y_Guias/Pr%C3%A1cticaNr3__Termodin%C3%A1mica_2026_2%20%281%29.pdf) | [Solucionario](../02_Ejercicios_y_Guias/Pr%C3%A1cticaNr3SOLUCION_Termodin%C3%A1mica_2026-2.pdf) | Siguiente: [Práctico 4](./pr%C3%A1ctica%204.md)

## Sustancia pura y propiedades específicas

- Una **sustancia pura** tiene composición química uniforme. Puede coexistir en más de una fase y seguir siendo pura, como agua líquida y vapor de agua en equilibrio.
- Las propiedades específicas son propiedades extensivas divididas por la masa:
  $$v=\frac{V}{m},\qquad u=\frac{U}{m},\qquad h=\frac{H}{m}$$
  Aquí $v$ es volumen específico, $u$ energía interna específica y $h$ entalpía específica. En las tablas del curso suelen expresarse en $\mathrm{m^3/kg}$ y $\mathrm{kJ/kg}$, respectivamente.
- La entalpía se define por $h=u+pv$. Para una cantidad total de masa fija, $U=mu$ y $H=mh$.

## Fases y estados de saturación

- Al calentar un líquido a presión fija, su temperatura aumenta hasta alcanzar la temperatura de saturación. Durante la vaporización a esa presión, coexisten líquido y vapor; al finalizar, queda vapor saturado. Más calentamiento produce vapor sobrecalentado.
- **Líquido comprimido o subenfriado:** el estado está en la región líquida, antes de alcanzar saturación a la presión dada.
- **Líquido saturado:** está a punto de comenzar a vaporizarse.
- **Mezcla saturada líquido-vapor:** ambas fases coexisten en equilibrio.
- **Vapor saturado:** está a punto de condensarse.
- **Vapor sobrecalentado:** se encuentra a una temperatura mayor que la de saturación para su presión.
- Para una sustancia pura en equilibrio, $T_{\mathrm{sat}}$ y $P_{\mathrm{sat}}$ no son independientes: conocida una, la otra queda determinada. En la región de mezcla, fijar presión fija la temperatura de saturación, y viceversa.

## Calidad de una mezcla

- La calidad $x$ es la fracción de la masa total que está en fase vapor:
  $$x=\frac{m_{\mathrm{v}}}{m_{\mathrm{total}}}$$
  En la mezcla saturada, $0\le x\le1$: $x=0$ corresponde a líquido saturado y $x=1$ a vapor saturado. No se define para líquido comprimido ni para vapor sobrecalentado.
- Una propiedad específica extensiva en la mezcla es el promedio ponderado de las fases. Usando los valores de líquido saturado ($f$) y vapor saturado ($g$):
  $$y=y_{\mathrm{f}}+x(y_{\mathrm{g}}-y_{\mathrm{f}})
  =y_{\mathrm{f}}+xy_{\mathrm{fg}}$$
  donde $y_{\mathrm{fg}}=y_{\mathrm{g}}-y_{\mathrm{f}}$. La relación puede aplicarse a $v$, $u$ y $h$.
- Por ejemplo, $v=v_{\mathrm{f}}+xv_{\mathrm{fg}}$. Si se conoce el volumen específico de una mezcla, puede despejarse $x=(v-v_{\mathrm{f}})/v_{\mathrm{fg}}$ y comprobar que el resultado esté entre 0 y 1.

## Cómo usar tablas de propiedades

1. Identifica la sustancia y convierte las propiedades conocidas a las unidades de las tablas.
2. Busca saturación por temperatura o presión. Compara los datos con los valores de saturación para ubicar la región.
3. Si dos propiedades independientes ubican el estado entre los valores saturados, se trata de mezcla; calcula calidad y propiedades con la relación de mezcla.
4. Si el estado está antes de saturación, usa la tabla de líquido comprimido. Si está más allá de vapor saturado, usa la tabla de vapor sobrecalentado.
5. Interpola entre entradas tabuladas cuando corresponda y comprueba la región antes de interpolar. No extrapoles ni uses calidad fuera de la mezcla sin justificación.
- En líquido comprimido, a veces se aproxima una propiedad por el valor de líquido saturado a la misma temperatura, pero es una aproximación y debe usarse cuando el método del curso lo permita.

## Determinación de fase a partir de los datos

- Para agua a una presión dada, consulta $T_{\mathrm{sat}}$ de esa presión:
  - Si $T<T_{\mathrm{sat}}$, el estado es líquido comprimido/subenfriado.
  - Si $T=T_{\mathrm{sat}}$, el estado es saturado; se necesita otra propiedad, como $v$, $u$ o $h$, para saber si es líquido, mezcla o vapor.
  - Si $T>T_{\mathrm{sat}}$, el estado es vapor sobrecalentado.
- Si se conoce la temperatura, también puede consultarse $P_{\mathrm{sat}}(T)$ y comparar la presión dada. En la región de mezcla, $P=P_{\mathrm{sat}}(T)$; por debajo de esa presión de saturación a la misma temperatura suele corresponder vapor sobrecalentado y por encima, líquido comprimido.
- No concluyas que una sustancia es vapor solo porque la temperatura sea alta en términos cotidianos: la fase depende conjuntamente de presión y temperatura.
- Para un estado saturado, conocer solo $P$ o solo $T$ no basta para encontrar todas las propiedades: ambas fijan la saturación, pero no la fracción de líquido/vapor. Se necesita una propiedad adicional o la calidad.

## Balance de mezcla y calidad

- La fórmula de mezcla se deduce ponderando cada fase por su fracción másica:
  $$y=(1-x)y_{\mathrm{f}}+xy_{\mathrm{g}}$$
  Esto equivale a $y=y_{\mathrm{f}}+xy_{\mathrm{fg}}$. La misma forma se usa para volumen total si se emplean propiedades totales de fase, pero en tablas se usan valores específicos.
- Si se conoce la masa total y la calidad:
  $$m_{\mathrm{v}}=xm,\qquad m_{\mathrm{f}}=(1-x)m$$
- Si un tanque rígido contiene mezcla, calcula primero el volumen específico global $v=V/m$. Compara con $v_{\mathrm{f}}$ y $v_{\mathrm{g}}$ a la saturación propuesta: si $v_{\mathrm{f}}<v<v_{\mathrm{g}}$, existe mezcla y se obtiene $x=(v-v_{\mathrm{f}})/(v_{\mathrm{g}}-v_{\mathrm{f}})$.
- En una evaporación de líquido saturado a vapor saturado, $x$ pasa de 0 a 1. En una condensación completa ocurre lo contrario. Una calidad mayor que 1 o menor que 0 señala que el estado supuesto está fuera de la región de mezcla o que se eligieron tablas/datos incompatibles.

## Interpolación y consistencia de tablas

- Si una propiedad se encuentra entre dos filas de una tabla y se justifica interpolación lineal:
  $$y=y_1+\frac{X-X_1}{X_2-X_1}(y_2-y_1)$$
  donde $X$ es la variable tabulada entre $X_1$ y $X_2$. Interpola dentro de la misma región y tabla; no interpoles atravesando la campana de saturación.
- Verifica que las unidades de presión sean absolutas y que las tablas usen la escala/unidad esperada. Las presiones manométricas deben convertirse antes de consultar tablas termodinámicas.
- Si los datos no satisfacen ninguna región o contradicen una restricción (por ejemplo, un estado saturado con $v$ fuera del intervalo $[v_f,v_g]$), revisa las unidades, la fase asumida y si la masa o el volumen total se interpretaron correctamente.

## Diagramas y cambios de fase

- En un diagrama $T-v$ o $P-v$, la región de mezcla queda bajo la campana de saturación. Su borde izquierdo es líquido saturado; el derecho, vapor saturado. El punto crítico es el extremo de la campana, donde deja de existir una distinción entre líquido y vapor.
- Durante la vaporización a presión constante de una sustancia pura, el volumen específico y la calidad aumentan mientras la temperatura permanece en $T_{\mathrm{sat}}$; se necesita energía para el cambio de fase (calor latente).
- En un recipiente rígido, el volumen total no cambia y, si la masa es fija, el volumen específico también permanece constante. El estado final se encuentra siguiendo esa condición junto con la energía suministrada.
- En un proceso a presión constante que atraviesa la región de mezcla, la temperatura permanece en $T_{\mathrm{sat}}$ durante el cambio de fase. A presión no constante, no supongas que la temperatura se mantiene fija durante la vaporización.

## Relacionar propiedades y energía

- Para masa fija, los cambios de propiedades totales se obtienen multiplicando el cambio específico por la masa:
  $$\Delta V=m(v_2-v_1),\qquad
  \Delta U=m(u_2-u_1),\qquad
  \Delta H=m(h_2-h_1)$$
- Si un proceso de vaporización ocurre a presión constante y solo hay trabajo de frontera, el calor intercambiado puede relacionarse con el cambio de entalpía. Para otros procesos debe aplicarse el balance de energía correspondiente; no supongas que $Q=\Delta H$ en general.
- Revisa la base de las tablas: valores específicos se expresan por unidad de masa; conviértelos a valores totales usando la masa solo al final.

## Modelos de proceso frecuentes en los problemas

- **Recipiente rígido:** $V$ y, con masa fija, $v$ son constantes. No hay trabajo de frontera; la presión puede cambiar. Se identifica el estado final usando el volumen específico y la energía/propiedad que permanezca fija.
- **Pistón con carga constante:** suele aproximarse como presión constante mientras el pistón se mueve. Si el pistón llega a topes, desde ese instante el volumen permanece constante y cambia la condición del proceso.
- **Evaporación completa a presión constante:** estado inicial líquido saturado, estado final vapor saturado; $\Delta v=v_g-v_f$, $\Delta u=u_g-u_f$ y el calor se determina con el balance de energía apropiado.
- **Vapor en región sobrecalentada:** usa la tabla de vapor sobrecalentado con dos propiedades independientes. No asignes calidad a ese estado.
