---
tags:
  - certamen2_termo
seguimiento_certamen2: true
progreso_certamen2: false
bloque_certamen2: Segunda Ley y máquinas térmicas
---

# Práctico 6 — Segunda Ley y máquinas térmicas

[Ver listado del práctico](../02_Ejercicios_y_Guias/Pr%C3%A1cticaNr6_Termodin%C3%A1mica_2026-2.pdf) | [Repaso Test 4](../01_Teoria_y_Conceptos/Repaso%20Test%204%20-%20Segunda%20Ley%20y%20Refrigeradores.md) | Siguiente: [Práctico 7](./pr%C3%A1ctica%207.md)

## Primera y Segunda Ley

- La Primera Ley conserva la energía y relaciona calor, trabajo y cambios de energía almacenada. Por sí sola no determina la dirección de un proceso ni si puede ocurrir espontáneamente.
- La Segunda Ley establece la dirección de los procesos y limita la conversión de calor en trabajo. El calor fluye espontáneamente de una fuente de mayor temperatura a otra de menor temperatura; invertir ese flujo requiere trabajo.
- Un proceso reversible es un ideal límite que puede invertirse sin dejar cambios netos en el sistema y su entorno. Los procesos reales son irreversibles por fricción, mezclas, expansión libre y transferencia de calor con diferencias finitas de temperatura.
- Un **reservorio térmico** o foco ideal puede absorber o entregar calor sin que su temperatura cambie apreciablemente. Los diagramas de máquina suelen representar como focos la fuente caliente y el sumidero frío.
- La Segunda Ley tiene dos enunciados equivalentes para ciclos:
  - **Kelvin–Planck:** ninguna máquina cíclica puede recibir calor de una sola fuente y convertirlo íntegramente en trabajo neto.
  - **Clausius:** ningún dispositivo cíclico puede transferir calor desde un cuerpo frío a uno caliente sin que se suministre trabajo.
- Las irreversibilidades hacen que el trabajo obtenido sea menor o el trabajo requerido sea mayor que en el límite reversible. Un balance de energía correcto es necesario, pero no suficiente para certificar que un dispositivo sea posible.

## Máquinas térmicas

- Una máquina térmica cíclica recibe calor $Q_{\mathrm{H}}$ de una fuente caliente, entrega trabajo neto $W_{\mathrm{neto}}$ y rechaza el calor restante $Q_{\mathrm{L}}$ a una fuente fría. En un ciclo, el cambio neto de energía almacenada es cero:
  $$W_{\mathrm{neto}}=Q_{\mathrm{H}}-Q_{\mathrm{L}}$$
- El rendimiento térmico mide la fracción del calor recibido que se convierte en trabajo neto:
  $$\eta_{\mathrm{th}}=\frac{W_{\mathrm{neto}}}{Q_{\mathrm{H}}}
  =1-\frac{Q_{\mathrm{L}}}{Q_{\mathrm{H}}}$$
- Para una máquina que opera continuamente, se usan tasas de transferencia:
  $$\dot{W}_{\mathrm{neto}}=\dot{Q}_{\mathrm{H}}-\dot{Q}_{\mathrm{L}},
  \qquad
  \eta_{\mathrm{th}}=\frac{\dot{W}_{\mathrm{neto}}}{\dot{Q}_{\mathrm{H}}}$$
- Una máquina cíclica no puede convertir todo el calor recibido en trabajo: debe rechazar calor a un foco frío. Por ello, su rendimiento es menor que 1.

## Límite reversible de Carnot

- Entre dos fuentes térmicas a temperaturas $T_{\mathrm{H}}$ y $T_{\mathrm{L}}$, la máquina reversible de Carnot establece el rendimiento máximo teórico:
  $$\eta_{\mathrm{th,rev}}=1-\frac{T_{\mathrm{L}}}{T_{\mathrm{H}}}$$
- Las temperaturas deben expresarse en kelvin y cumplir $T_{\mathrm{H}}>T_{\mathrm{L}}$. El rendimiento de cualquier máquina real que opere entre esas mismas fuentes no puede superar el de Carnot.
- Aumentar la temperatura de la fuente caliente o disminuir la de la fuente fría aumenta el límite reversible. Esto no implica que cualquier máquina real alcance ese valor.
- Para las mismas dos fuentes, si $\eta_{\mathrm{th}}<\eta_{\mathrm{th,rev}}$ la máquina es irreversible (real); si son iguales, es reversible ideal; si $\eta_{\mathrm{th}}>\eta_{\mathrm{th,rev}}$, la máquina es imposible.
- Para un ciclo reversible entre dos fuentes, las magnitudes de los calores se relacionan con las temperaturas absolutas:
  $$\frac{Q_{\mathrm{L}}}{Q_{\mathrm{H}}}
  =\frac{T_{\mathrm{L}}}{T_{\mathrm{H}}}$$
- El teorema de Carnot implica que todas las máquinas reversibles entre los mismos dos reservorios tienen el mismo rendimiento, independientemente de su diseño, y que ninguna máquina irreversible puede ser más eficiente.
- Para clasificar una máquina propuesta, calcula primero:
  $$\eta_{\mathrm{th}}=1-\frac{Q_{\mathrm{L}}}{Q_{\mathrm{H}}},\qquad
  \eta_{\mathrm{Carnot}}=1-\frac{T_{\mathrm{L}}}{T_{\mathrm{H}}}$$
  Luego compara ambos: un valor menor que Carnot es compatible con una máquina irreversible (pero no demuestra por sí solo que el diseño sea realizable); igual a Carnot corresponde al límite reversible ideal; mayor que Carnot es imposible.
- Si se da rendimiento y calor de entrada, recupera el trabajo y calor rechazado:
  $$W_{\mathrm{neto}}=\eta_{\mathrm{th}}Q_{\mathrm{H}},\qquad
  Q_{\mathrm{L}}=(1-\eta_{\mathrm{th}})Q_{\mathrm{H}}$$
  La misma forma aplica a tasas de transferencia en operación continua.

## Generación de potencia y cogeneración

- La potencia neta producida es la diferencia entre las tasas de calor que entran y salen. Si se conocen el rendimiento y la tasa de calor suministrada:
  $$\dot{W}_{\mathrm{neto}}=\eta_{\mathrm{th}}\dot{Q}_{\mathrm{H}}$$
- En cogeneración, parte del calor que normalmente se rechazaría se aprovecha para calefacción u otro proceso. El calor útil no se convierte en trabajo: se contabiliza como producto energético adicional, con la frontera del sistema definida claramente.
- Si dos máquinas térmicas operan en serie, el calor rechazado por la primera puede alimentar la segunda. El trabajo total es la suma de los trabajos netos y el rendimiento global se calcula respecto del calor que ingresa al conjunto:
  $$\dot{W}_{\mathrm{total}}=\dot{W}_1+\dot{W}_2,\qquad
  \eta_{\mathrm{global}}=\frac{\dot{W}_{\mathrm{total}}}{\dot{Q}_{\mathrm{entrada,global}}}$$
- Para hallar flujos en sistemas en serie, aplica el balance de energía a cada máquina y conecta la salida térmica de una con la entrada de la siguiente. No confundas el rendimiento individual con el global.
- En una central con cogeneración puede interesar maximizar el aprovechamiento total del combustible:
  $$\eta_{\mathrm{uso}}=
  \frac{\dot W_{\mathrm{neto}}+\dot Q_{\mathrm{útil}}}{\dot Q_{\mathrm{entrada}}}$$
  Esta medida contabiliza energía térmica útil además de potencia, por lo que no es el rendimiento térmico de una máquina que convierte calor en trabajo. Deben especificarse los productos y la frontera.
- En un motor de alta y otro de baja temperatura conectados en serie, el motor superior rechaza calor al foco intermedio y el inferior lo recibe. La tasa de calor intermedia es interna al conjunto; al analizar ambos como un solo sistema, se cancela del balance global.
- El rendimiento de dos etapas en serie no se obtiene promediando sus rendimientos. Calcula la potencia de cada etapa a partir de su propio calor de entrada, suma las potencias y divide por el calor de entrada externo al conjunto.

## Segunda Ley aplicada a los casos del listado

- **Rendimiento del 100 %:** implicaría $Q_{\mathrm{L}}=0$. Aunque la Primera Ley podría cerrar el balance energético, violaría Kelvin–Planck si la máquina opera cíclicamente entre una sola fuente y produce trabajo sin otro efecto.
- **Máquinas con igual eficiencia y distintas fuentes:** compara individualmente cada eficiencia con su propio límite de Carnot. La misma eficiencia puede ser posible para una pareja de temperaturas e imposible para otra.
- **Eficiencia igual a una fracción del límite reversible:** por ejemplo, si $\eta=r\eta_{\mathrm{Carnot}}$, calcula primero el límite con kelvin y luego aplica la fracción. No se debe multiplicar por temperaturas en Celsius.
- **Fuente térmica de océano o ambiente:** el máximo teórico se obtiene usando las temperaturas absolutas de la fuente y el sumidero. La diferencia pequeña entre ambas limita fuertemente la conversión a trabajo.
- **Dispositivo de movimiento perpetuo:** revisa primero si viola la Primera Ley (energía creada) y luego si, aun conservando energía, viola Kelvin–Planck o Clausius.

## Enunciados de imposibilidad

- Un dispositivo que pretende producir trabajo neto en un ciclo mientras recibe calor de una sola fuente y no genera ningún otro efecto contradice el enunciado de Kelvin–Planck de la Segunda Ley.
- Un dispositivo que pretende transferir calor desde una fuente fría a una caliente sin aporte de trabajo contradice el enunciado de Clausius.
- Las afirmaciones de funcionamiento deben evaluarse para el dispositivo completo y todos sus intercambios con el entorno. Un balance de energía que “cierra” no basta para demostrar que el dispositivo sea posible: también debe respetar la Segunda Ley.

## Estrategia para resolver ejercicios

1. Dibuja la máquina y señala la fuente caliente, la fría, los calores y el trabajo con sus direcciones.
2. Escribe el balance de energía del ciclo antes de calcular rendimiento o potencia.
3. Convierte todas las temperaturas a kelvin al usar Carnot; las diferencias de temperatura no reemplazan a las temperaturas absolutas en esa relación.
4. Compara el rendimiento propuesto con el límite de Carnot entre las mismas temperaturas.
5. En sistemas de varias etapas o cogeneración, define la frontera global y evita contar dos veces el calor transferido internamente.
6. Comprueba simultáneamente la Primera Ley y la Segunda Ley: conservación de energía y posibilidad física son pruebas distintas.
