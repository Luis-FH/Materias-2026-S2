---
tags:
  - certamen2_termo
---

[⬅️ Volver a Termodinámica](../Termodinamica.md) | [🎨 Tablero Canvas](../Termodinamica.canvas)

# Repaso Test 4 — Segunda Ley, máquinas térmicas y refrigeradores

## Alcance según el calendario del curso

El programa de Termodinámica 541203 de Ingeniería Civil Industrial UdeC ubica el **Test 4** en las semanas 10 y 11 del calendario: **Segunda Ley** (secciones 6.1–6.3) y **refrigeradores** (secciones 6.4–6.11). La evaluación aparece asociada a la semana 12, el 6 de noviembre. Por ese alcance, este apunte prioriza enunciados de la Segunda Ley, máquinas térmicas, rendimiento, ciclo de Carnot, refrigeradores, bombas de calor y COP. La entropía aparece después en el calendario; no se considera parte del alcance anunciado para este test, salvo indicación distinta del curso.

El programa describe la asignatura como aplicación de modelos para determinar propiedades de la materia antes y después de un proceso, cuantificar flujos de energía y evaluar equipos y ciclos térmicos. Por eso el repaso no se limita a memorizar fórmulas: exige definir sistemas, realizar balances, interpretar el sentido de las transferencias y verificar que el desempeño respete la Segunda Ley.

### Material relacionado

- [Ensayos de práctica — Test 4](../03_Evaluaciones_y_Certamenes/Ensayos%20de%20pr%C3%A1ctica%20Test%204.md)
- [Tests 1–4 disponibles](../03_Evaluaciones_y_Certamenes/test%201-4.pdf)

---

## 1. Qué estudian la Primera y la Segunda Ley

La **Primera Ley** expresa conservación de energía. Permite calcular cuánto calor, trabajo o cambio de energía corresponde a un proceso, pero no determina por sí sola si el proceso puede ocurrir ni cuál es su dirección espontánea.

La **Segunda Ley** fija esa dirección y limita las transformaciones posibles. Por ejemplo, la energía eléctrica puede convertirse íntegramente en calor en una resistencia, pero una máquina cíclica no puede convertir íntegramente el calor tomado de una sola fuente en trabajo neto. Para mover calor desde una fuente fría a otra caliente se requiere trabajo.

Las dos leyes se usan juntas:

1. **Primera Ley:** verifica que el balance energético cierre.
2. **Segunda Ley:** verifica que la dirección y el desempeño sean físicamente posibles.

Un balance de energía correcto no basta para demostrar que un motor o refrigerador es posible.

## 2. Sistemas cíclicos, fuentes térmicas y convenciones

- Un **ciclo** termina en el mismo estado en que comenzó. Por ello, el cambio neto de toda propiedad de estado del fluido de trabajo es cero; en particular, $\Delta E_{\mathrm{ciclo}}=0$.
- Una **fuente térmica** o **reservorio** puede recibir o entregar energía como calor sin que su temperatura cambie apreciablemente.
- Se usarán las magnitudes positivas $Q_{\mathrm{H}}$ para calor recibido desde la fuente caliente, $Q_{\mathrm{L}}$ para calor rechazado al foco frío, y $W_{\mathrm{neto}}$ para trabajo producido por una máquina térmica.
- Para un refrigerador, $Q_{\mathrm{L}}$ es el calor extraído del espacio frío, $Q_{\mathrm{H}}$ el rechazado al espacio caliente y $W_{\mathrm{entrada}}$ el trabajo suministrado.
- Los subíndices $\mathrm{H}$ y $\mathrm{L}$ indican focos de temperatura alta (*hot*) y baja (*low*). Las temperaturas deben cumplir $T_{\mathrm{H}}>T_{\mathrm{L}}$.

No mezcles la convención algebraica de signos de la Primera Ley con diagramas donde todos los calores y trabajos se anotan como magnitudes positivas en la dirección indicada. En cada ejercicio dibuja las flechas y declara qué convención usas.

## 3. Enunciados fundamentales de la Segunda Ley

### Kelvin–Planck

Es imposible construir una máquina que opere en ciclo cuyo único efecto sea extraer calor de una sola fuente y transformarlo íntegramente en trabajo. Una máquina térmica debe rechazar parte del calor recibido a un foco de menor temperatura.

Por tanto, una máquina cíclica que recibiera $Q_{\mathrm{H}}$ y produjera $W_{\mathrm{neto}}=Q_{\mathrm{H}}$ con $Q_{\mathrm{L}}=0$ sería imposible.

### Clausius

Es imposible construir un dispositivo cíclico cuyo único efecto sea transferir calor desde una fuente fría hacia una fuente caliente sin aporte de trabajo. El refrigerador sí realiza esa transferencia, pero consume trabajo.

### Equivalencia

Los enunciados de Kelvin–Planck y Clausius son equivalentes: violar uno permitiría construir un dispositivo compuesto que violaría el otro. En problemas de “máquinas imposibles” hay que considerar todos los intercambios y efectos del conjunto, no solo el componente aislado.

## 4. Máquinas térmicas y rendimiento

Una máquina térmica cíclica:

1. recibe calor de una fuente caliente;
2. convierte una parte en trabajo neto;
3. rechaza el resto a una fuente fría.

Como el fluido de trabajo completa un ciclo, la Primera Ley da:

$$Q_{\mathrm{H}}=W_{\mathrm{neto}}+Q_{\mathrm{L}}$$

El **rendimiento térmico** es la fracción del calor de entrada convertida en trabajo:

$$\eta_{\mathrm{th}}=\frac{W_{\mathrm{neto}}}{Q_{\mathrm{H}}}
=1-\frac{Q_{\mathrm{L}}}{Q_{\mathrm{H}}}$$

Para funcionamiento continuo se emplean tasas de transferencia:

$$\dot{Q}_{\mathrm{H}}=\dot{W}_{\mathrm{neto}}+\dot{Q}_{\mathrm{L}},
\qquad
\eta_{\mathrm{th}}=\frac{\dot{W}_{\mathrm{neto}}}{\dot{Q}_{\mathrm{H}}}$$

Si se conocen dos de las tres tasas, se determina la tercera con el balance. Si se conoce el rendimiento:

$$\dot{W}_{\mathrm{neto}}=\eta_{\mathrm{th}}\dot{Q}_{\mathrm{H}},
\qquad
\dot{Q}_{\mathrm{L}}=(1-\eta_{\mathrm{th}})\dot{Q}_{\mathrm{H}}$$

El rendimiento es adimensional y para una máquina real debe ser menor que 1. Eso es necesario, pero no suficiente: también debe respetarse el límite de Carnot.

## 5. Reversibilidad, irreversibilidad y límite de Carnot

- Un proceso **reversible** es un ideal límite que puede invertirse dejando sin cambios tanto el sistema como el entorno.
- Un proceso real es **irreversible**. Causas frecuentes son fricción, expansión no restringida, mezclado, deformación inelástica y transferencia de calor a través de una diferencia finita de temperatura.
- Una máquina reversible entre dos reservorios es la referencia de máximo rendimiento. Todas las máquinas reversibles entre los mismos reservorios tienen el mismo rendimiento; ninguna máquina irreversible puede superarlo.

Para fuentes a temperaturas absolutas $T_{\mathrm{H}}$ y $T_{\mathrm{L}}$:

$$\eta_{\mathrm{Carnot}}=1-\frac{T_{\mathrm{L}}}{T_{\mathrm{H}}}$$

En un ciclo reversible entre las mismas fuentes:

$$\frac{Q_{\mathrm{L}}}{Q_{\mathrm{H}}}
=\frac{T_{\mathrm{L}}}{T_{\mathrm{H}}}$$

La temperatura debe estar en kelvin. Si el enunciado entrega grados Celsius:

$$T(\mathrm{K})=t(^{\circ}\mathrm{C})+273{,}15$$

No uses valores Celsius directamente en cocientes como $T_{\mathrm{L}}/T_{\mathrm{H}}$.

### Cómo clasificar una máquina propuesta

1. Calcula su rendimiento a partir de calores o trabajo:
   $$\eta_{\mathrm{propuesta}}=1-\frac{Q_{\mathrm{L}}}{Q_{\mathrm{H}}}$$
2. Convierte las temperaturas de los focos a kelvin y calcula $\eta_{\mathrm{Carnot}}$.
3. Compara:
   - $\eta_{\mathrm{propuesta}}<\eta_{\mathrm{Carnot}}$: compatible con una máquina irreversible según ese límite; no demuestra por sí solo que el diseño sea realizable.
   - $\eta_{\mathrm{propuesta}}=\eta_{\mathrm{Carnot}}$: límite reversible ideal.
   - $\eta_{\mathrm{propuesta}}>\eta_{\mathrm{Carnot}}$: imposible entre esas fuentes.

Un rendimiento del 100 % viola Kelvin–Planck para una máquina que opera entre una fuente y sin otro efecto. Una máquina que supera Carnot también es imposible, aunque su balance de energía cierre.

## 6. Refrigeradores y bombas de calor

Un refrigerador usa trabajo para extraer calor $Q_{\mathrm{L}}$ de una región fría y rechazar $Q_{\mathrm{H}}$ a una región más caliente. La bomba de calor usa el mismo ciclo, pero el efecto útil buscado es el calentamiento del espacio caliente.

Para el ciclo:

$$Q_{\mathrm{H}}=Q_{\mathrm{L}}+W_{\mathrm{entrada}}$$

### Coeficiente de desempeño (COP)

Para refrigeración, el efecto útil es extraer calor del foco frío:

$$COP_{\mathrm{R}}=\frac{Q_{\mathrm{L}}}{W_{\mathrm{entrada}}}
=\frac{Q_{\mathrm{L}}}{Q_{\mathrm{H}}-Q_{\mathrm{L}}}$$

Para calefacción, el efecto útil es entregar calor al foco caliente:

$$COP_{\mathrm{BC}}=\frac{Q_{\mathrm{H}}}{W_{\mathrm{entrada}}}
=\frac{Q_{\mathrm{H}}}{Q_{\mathrm{H}}-Q_{\mathrm{L}}}$$

También se calculan con tasas:

$$COP_{\mathrm{R}}=\frac{\dot{Q}_{\mathrm{L}}}{\dot{W}_{\mathrm{entrada}}},
\qquad
COP_{\mathrm{BC}}=\frac{\dot{Q}_{\mathrm{H}}}{\dot{W}_{\mathrm{entrada}}}$$

Para el mismo ciclo:

$$COP_{\mathrm{BC}}=COP_{\mathrm{R}}+1$$

El COP **no es una eficiencia térmica**: puede ser mayor que 1 porque el equipo mueve energía térmica desde el foco frío además de recibir trabajo. Un COP de 4, por ejemplo, significa que cada unidad de trabajo permite extraer cuatro unidades de calor (si se habla de refrigeración), no que se cree energía.

### Límites reversibles de COP

Para una máquina reversible de Carnot:

$$COP_{\mathrm{R,rev}}=\frac{T_{\mathrm{L}}}{T_{\mathrm{H}}-T_{\mathrm{L}}},
\qquad
COP_{\mathrm{BC,rev}}=\frac{T_{\mathrm{H}}}{T_{\mathrm{H}}-T_{\mathrm{L}}}$$

Los dos focos deben estar en kelvin. Se cumple:

$$COP_{\mathrm{R}}<COP_{\mathrm{R,rev}},
\qquad
COP_{\mathrm{BC}}<COP_{\mathrm{BC,rev}}$$

para dispositivos reales irreversibles. La diferencia $T_{\mathrm{H}}-T_{\mathrm{L}}$ es el salto térmico. Al disminuir, aumenta el COP reversible y disminuye el trabajo mínimo necesario para mover una cantidad fija de calor. Si el salto es grande, la refrigeración o calefacción es termodinámicamente más exigente.

Para el ciclo reversible:

$$\frac{Q_{\mathrm{H}}}{Q_{\mathrm{L}}}
=\frac{T_{\mathrm{H}}}{T_{\mathrm{L}}}$$

Combinando esta relación con la Primera Ley se obtienen las expresiones de COP de Carnot.

## 7. Cómo plantear cada tipo de pregunta

### A. Completar calores y trabajo de una máquina

Usa primero:

$$\dot{W}_{\mathrm{neto}}=\dot{Q}_{\mathrm{H}}-\dot{Q}_{\mathrm{L}}$$

Ejemplo de organización: si se conocen $\dot{Q}_{\mathrm{H}}$ y $\dot{Q}_{\mathrm{L}}$, resta para obtener potencia; si se conocen $\dot{Q}_{\mathrm{H}}$ y $\dot{W}_{\mathrm{neto}}$, despeja el calor rechazado. Luego calcula $\eta_{\mathrm{th}}$ y verifica que esté entre 0 y el límite de Carnot.

### B. Decidir si una máquina es reversible, irreversible o imposible

- Convierte primero las temperaturas de Celsius a kelvin.
- Calcula el rendimiento real a partir de los calores.
- Calcula el rendimiento de Carnot para esas mismas temperaturas.
- Compara con Carnot y justifica la conclusión con la Segunda Ley, no solo con la Primera.
- Si no hay temperaturas de foco, aún puede identificarse una violación evidente de Kelvin–Planck, como convertir todo el calor de una sola fuente en trabajo cíclico.

### C. Encontrar consumo eléctrico o capacidad de refrigeración

Para un refrigerador:

$$\dot{W}_{\mathrm{entrada}}=\frac{\dot{Q}_{\mathrm{L}}}{COP_{\mathrm{R}}}$$

Para una bomba de calor:

$$\dot{W}_{\mathrm{entrada}}=\frac{\dot{Q}_{\mathrm{H}}}{COP_{\mathrm{BC}}}$$

Después verifica el calor del otro foco con el balance. No confundas capacidad de refrigeración (tasa de calor movido) con potencia eléctrica.

### D. Máquinas térmicas en serie

Si el calor rechazado por una máquina alimenta a otra:

1. Define las fuentes y temperaturas de cada etapa.
2. Aplica el balance y el rendimiento a cada máquina por separado.
3. El calor intermedio que sale de la primera y entra a la segunda es una transferencia interna al conjunto.
4. Suma las potencias netas; el rendimiento global es potencia total dividida por el calor que entra desde el exterior.

No promedies los rendimientos de las etapas. Si $\dot{Q}_{\mathrm{H},2}$ es el calor que recibe la segunda, usa $\dot{W}_2=\eta_2\dot{Q}_{\mathrm{H},2}$ y conecta ese calor con el balance de la primera.

### E. Cogeneración

Una instalación de cogeneración produce trabajo y entrega calor útil para otro proceso. El calor útil no es trabajo. Si se solicita aprovechamiento total de energía, una razón posible es:

$$\eta_{\mathrm{uso}}
=\frac{\dot{W}_{\mathrm{neto}}+\dot{Q}_{\mathrm{útil}}}
{\dot{Q}_{\mathrm{entrada}}}$$

Lee con cuidado qué definición de eficiencia pide el problema. No sustituyas automáticamente esta medida de aprovechamiento total por el rendimiento térmico de una máquina.

### F. Máquina imposible o “movimiento perpetuo”

- Si el dispositivo entrega más energía que la que recibe, viola la Primera Ley.
- Si conserva energía pero convierte todo el calor de una sola fuente en trabajo cíclico, viola Kelvin–Planck.
- Si transfiere calor de frío a caliente sin trabajo de entrada, viola Clausius.
- Si su rendimiento o COP supera el límite de Carnot, viola la Segunda Ley.
- Evalúa el sistema completo, incluidas las fuentes, cargas y posibles efectos externos.

## 8. Ejemplos-guía con datos ilustrativos

### Ejemplo 1: rendimiento y calor rechazado

Una máquina recibe $500\,\mathrm{kW}$ y tiene rendimiento $0{,}40$:

$$\dot{W}_{\mathrm{neto}}=0{,}40(500)=200\,\mathrm{kW}$$

$$\dot{Q}_{\mathrm{L}}=500-200=300\,\mathrm{kW}$$

La respuesta debe satisfacer tanto el rendimiento como el balance.

### Ejemplo 2: límite de Carnot

Una máquina opera entre $600\,\mathrm{K}$ y $300\,\mathrm{K}$:

$$\eta_{\mathrm{Carnot}}=1-\frac{300}{600}=0{,}50$$

Una propuesta de 55 % es imposible entre esos reservorios; una de 40 % no supera Carnot y podría ser irreversible.

### Ejemplo 3: refrigerador

Si un refrigerador extrae $4\,\mathrm{kW}$ con $COP_{\mathrm{R}}=4$, entonces:

$$\dot{W}_{\mathrm{entrada}}=\frac{4}{4}=1\,\mathrm{kW}$$

$$\dot{Q}_{\mathrm{H}}=4+1=5\,\mathrm{kW}$$

El calor rechazado es mayor que el extraído porque incluye la potencia de entrada.

### Ejemplo 4: bomba de calor

Si una bomba entrega $10\,\mathrm{kW}$ de calefacción con $COP_{\mathrm{BC}}=5$, consume:

$$\dot{W}_{\mathrm{entrada}}=\frac{10}{5}=2\,\mathrm{kW}$$

y extrae $8\,\mathrm{kW}$ del foco frío. Se comprueba $10=8+2$.

## 9. Fronteras de sistema: refrigerador en una habitación

- **Refrigerador como sistema:** entra trabajo eléctrico y calor desde el foco frío; sale calor al foco caliente.
- **Contenido frío como sistema:** el calor extraído es energía que sale del contenido. El trabajo eléctrico no necesariamente entra directamente al alimento; depende de dónde se ubique la frontera.
- **Habitación con refrigerador cerrado:** si el condensador descarga al mismo recinto, el refrigerador saca calor del recinto y devuelve ese calor más el trabajo eléctrico. Si las paredes son adiabáticas, el balance neto calienta la habitación en una tasa igual a la potencia eléctrica consumida.
- **Puerta abierta:** el equipo no puede enfriar indefinidamente la habitación completa; extrae calor de una zona y lo devuelve al mismo espacio con un excedente asociado al trabajo consumido.

La regla para estos problemas es dibujar la frontera antes de asignar flechas. El calor que se transfiere internamente entre partes incluidas dentro de una misma frontera no aparece como interacción externa del conjunto.

## 10. Errores típicos y chequeos

1. **Usar Celsius en Carnot.** Convierte cada temperatura a kelvin antes de formar cocientes.
2. **Confundir calor con trabajo.** En un refrigerador, el trabajo es la energía que permite bombear calor contra su dirección espontánea.
3. **Confundir rendimiento con COP.** El rendimiento térmico de un motor es menor que 1; el COP puede ser mayor que 1.
4. **Cambiar la definición del efecto útil.** Refrigerador usa $Q_{\mathrm{L}}$; bomba de calor usa $Q_{\mathrm{H}}$.
5. **Olvidar el balance del ciclo.** Verifica $Q_{\mathrm{H}}=Q_{\mathrm{L}}+W_{\mathrm{entrada}}$.
6. **Afirmar que “menor que Carnot” prueba que el diseño funciona.** Solo indica que no viola ese límite; todavía debe satisfacer los demás balances y restricciones.
7. **Promediar eficiencias en cascada.** Calcula etapa por etapa y luego el rendimiento total.
8. **Usar temperaturas de los equipos en vez de las de los reservorios.** En la fórmula de Carnot se usan las temperaturas de los focos térmicos especificados.
9. **Sumar transferencias internas en un balance global.** Si una etapa alimenta a otra, el flujo intermedio se cancela al analizar el conjunto.
10. **Ignorar las unidades.** Tasas de calor y trabajo deben usar unidades compatibles; por ejemplo, $\mathrm{kJ/s}=\mathrm{kW}$.

## 11. Lista de comprobación para el test

- [ ] Identifiqué qué dispositivo se analiza y cuál es su frontera.
- [ ] Dibujé los reservorios y las direcciones de $Q_{\mathrm{H}}$, $Q_{\mathrm{L}}$ y $W$.
- [ ] Escribí el balance de la Primera Ley antes de despejar.
- [ ] Usé la definición correcta: $\eta_{\mathrm{th}}$, $COP_{\mathrm{R}}$ o $COP_{\mathrm{BC}}$.
- [ ] Convertí todas las temperaturas de Carnot a kelvin.
- [ ] Comparé la máquina con el límite reversible correspondiente.
- [ ] En cascadas/cogeneración, distinguí flujos internos de los que cruzan la frontera global.
- [ ] Verifiqué magnitudes, unidades y sentido físico de la respuesta.

### Idea central para recordar

La Primera Ley indica **cuánto** puede transferirse según el balance energético; la Segunda Ley indica **en qué dirección** y **con qué desempeño máximo** puede ocurrir. Toda respuesta de máquina térmica o refrigerador debe respetar ambas.
