---
tags:
  - certamen2_termo
seguimiento_certamen2: true
progreso_certamen2: false
bloque_certamen2: Entropía y procesos isentrópicos
---

# Práctico 8 — Entropía y procesos isentrópicos

[Ver enunciado del práctico](../02_Ejercicios_y_Guias/Pr%C3%A1ctica%20Nr8%20Termodin%C3%A1mica2026-2.pdf)

## Entropía y Segunda Ley

- La entropía es una propiedad que permite cuantificar la dirección de un proceso y las irreversibilidades.
- En un sistema cerrado:
  $$\Delta S_{\mathrm{sist}}=\int_1^2\frac{\delta Q}{T_{\mathrm{b}}}+S_{\mathrm{gen}}$$
- La entropía generada nunca es negativa:
  $$S_{\mathrm{gen}}\geq 0,\qquad
  \Delta S_{\mathrm{universo}}=S_{\mathrm{gen}}$$
- Para un depósito térmico a temperatura constante:
  $$\Delta S=\frac{Q}{T}$$
  con $Q>0$ si el depósito recibe calor.
- Un proceso es isentrópico si $s_2=s_1$. Idealmente ocurre en una expansión o compresión adiabática y reversible.
- Una diferencia finita de temperatura, el roce, la mezcla y una reacción de agitación generan entropía. Una transferencia adiabática no implica necesariamente que $S_{\mathrm{gen}}=0$.

## Entropía en sustancias y sólidos

- Para un gas ideal con calores específicos constantes:
  $$s_2-s_1=c_p\ln\left(\frac{T_2}{T_1}\right)
  -R\ln\left(\frac{P_2}{P_1}\right)$$
- En una expansión o compresión isentrópica con $k=c_p/c_v$ constante:
  $$\frac{T_2}{T_1}
  =\left(\frac{P_2}{P_1}\right)^{(k-1)/k}$$
- Para sólidos o líquidos con calor específico constante:
  $$\Delta S=mc\ln\left(\frac{T_2}{T_1}\right)$$
- En sustancias reales o cambios de fase se usan las tablas termodinámicas. No conviene calcular entropía específica con una ecuación de gas ideal cuando la sustancia está cerca de la saturación.
- Las temperaturas absolutas en kelvin son obligatorias en logaritmos y relaciones isentrópicas.

## Procesos de transferencia y equilibrio térmico

- En transferencia directa entre dos depósitos, cada uno tiene $\Delta S=Q/T$, con signo positivo en el depósito que recibe calor y negativo en el que entrega.
- El cambio total de entropía es la suma de los depósitos:
  $$\Delta S_{\mathrm{total}}
  =\Delta S_{\mathrm{depósito,frío}}
  +\Delta S_{\mathrm{depósito,caliente}}$$
- Si dos sólidos se ponen en contacto dentro de una frontera adiabática, se conserva la energía sensible y se calcula una temperatura final común:
  $$m_{\mathrm{A}}c_{\mathrm{A}}(T_{\mathrm{f}}-T_{\mathrm{A}})
  +m_{\mathrm{B}}c_{\mathrm{B}}(T_{\mathrm{f}}-T_{\mathrm{B}})=0$$
- La entropía total de los sólidos es la suma de sus cambios:
  $$\Delta S_{\mathrm{total}}
  =m_{\mathrm{A}}c_{\mathrm{A}}\ln\frac{T_{\mathrm{f}}}{T_{\mathrm{A}}}
  +m_{\mathrm{B}}c_{\mathrm{B}}\ln\frac{T_{\mathrm{f}}}{T_{\mathrm{B}}}$$
- Cuando un bloque alcanza el equilibrio con un lago idealizado como reservorio, la entropía del bloque se calcula por tablas o con $mc\ln(T_{\mathrm{f}}/T_{\mathrm{i}})$ y la del lago mediante $Q_{\mathrm{lago}}/T_{\mathrm{lago}}$.
- Un proceso natural con $\Delta S_{\mathrm{universo}}>0$ es irreversible y posible. Si el cambio total fuera cero, sería reversible ideal; si fuera negativo, violaría la Segunda Ley.

## Sistemas cerrados y recipientes rígidos

- En un cilindro con agua o refrigerante, el volumen específico permanece constante si el recipiente es rígido.
- En el enfriamiento de vapor en un radiador rígido, se determinan inicialmente las propiedades en el estado inicial y luego, con $v_2=v_1$ y $T_2$ conocida, se obtiene el estado final y $\Delta s=s_2-s_1$.
- En un recipiente aislado y rígido con un agitador:
  - No hay transferencia de calor ni trabajo de frontera.
  - El trabajo de eje aumenta la energía interna.
  - Para un gas ideal cerrado a volumen fijo, puede hallarse el estado final usando $P/T=\mathrm{constante}$.
  - Si el proceso no es reversible, el cambio de entropía no se obtiene suponiendo $Q=0$; se calcula con las propiedades o con la relación de entropía del gas.
- En calentamiento eléctrico de agua a presión constante, el trabajo eléctrico realiza trabajo sobre el agua y puede haber expansión de la frontera. Se requiere la tabla de propiedades o el balance completo para determinar el estado final antes de calcular $\Delta S$.

## Turbinas, compresores y bombas

- Para una tobera o turbina adiabática se define el estado ideal isentrópico como el que sale a la misma presión con $s_{2s}=s_1$.
- Eficiencia isentrópica de una turbina:
  $$\eta_{\mathrm{t}}=\frac{h_1-h_{2,\mathrm{real}}}
  {h_1-h_{2s}}$$
- Eficiencia isentrópica de un compresor o bomba:
  $$\eta_{\mathrm{c}}=\frac{h_{2s}-h_1}
  {h_{2,\mathrm{real}}-h_1}$$
- En vapor se usan tablas y el estado $2s$ se encuentra mediante igualdad de entropía específica y presión de salida. Luego se determina $h_{2s}$ o $h_{2,\mathrm{real}}$ según el dato conocido.
- En una turbina real se puede obtener la potencia a partir de:
  $$\dot W=\dot m(h_1-h_2)$$
  incluyendo $\left(V_1^2-V_2^2\right)/2$ si se especifican velocidades distintas.
- Para compresores de gas ideal con calores variables se usan tablas de aire o relaciones de propiedades con base en entalpía y entropía.
- Una turbina isentrópica es el límite ideal entre entradas y presión de salida iguales: produce el máximo trabajo entre procesos adiabáticos porque opera sin irreversibilidades y utiliza la mayor caída de entalpía posible.

## Trabajo mínimo, máximo y bombeo

- La compresión reversible de un gas ideal es el trabajo mínimo teórico por unidad de masa en el límite adiabático reversible:
  $$w_{\mathrm{s,in}}=h_2-h_1$$
- Para vapor o gases reales se compara el estado real con el estado ideal isentrópico y se usan tablas o relaciones de entalpía.
- En una bomba de agua, la aproximación de líquido comprimido puede estimar:
  $$w_{\mathrm{bomba}}\approx v(P_2-P_1)$$
- Como aproximaciones alternativas se puede usar el volumen específico de entrada o un promedio entre entrada y salida. No son intercambiables con la energía específica obtenida por datos de entropía y comprimido.
- Para una bomba de flujo estacionario:
  $$\dot W_{\mathrm{bomba}}=\dot m\,w_{\mathrm{bomba}}$$
- En una bomba reversible, $s_2=s_1$ y no hay generación de entropía; las aproximaciones de volumen específico pueden introducir pequeños errores que deben cuantificarse.

## Expansión y compresión de gases

- Para aire con calores específicos variables se deben usar tablas de aire y resultados de isentrópia, no asumir $k$ constante si el enunciado exige precisión.
- Para argón u otro gas ideal monatómico pueden usarse:
  $$T_2=T_1\left(\frac{P_2}{P_1}\right)^{(k-1)/k},
  \qquad k=\frac{c_p}{c_v}$$
- El trabajo específico máximo de una turbina reversible se aproxima por:
  $$w_{\mathrm{t,\max}}=h_1-h_2$$
- En una tobera, la eficiencia isentrópica permite obtener la temperatura o entalpía real de salida. Luego se aplica la conservación de energía para calcular la velocidad:
  $$h_1+\frac{V_1^2}{2}=h_2+\frac{V_2^2}{2}$$
- En una turbina real con cambios de velocidad cinética, estos términos pueden ser relevantes y no deben omitirse.

## Generación de entropía en procesos abiertos

- En procesos estacionarios adiabáticos sin inventarios acumulados:
  $$\dot S_{\mathrm{gen}}
  =\sum_{\mathrm{salidas}}\dot m s
  -\sum_{\mathrm{entradas}}\dot m s$$
- Si hay una transferencia de calor $Q$ hacia el ambiente a $T_0$:
  $$s_{\mathrm{gen}}
  =s_2-s_1-\frac{q_{\mathrm{exterior}}}{T_0}$$
  según el signo establecido para el calor desde el sistema.
- Para un compresor con entropía específica y calor perdidos conocidos, primero se usa la relación de entropía para hallar la temperatura de salida o la variación de entalpía.
- La generación de entropía en turbinas reales indica el grado de irreversibilidad; puede determinarse a partir de estados específicos, flujo másico y balances.
- La generación se expresa por unidad de masa o por unidad de tiempo según el objetivo:
  $$s_{\mathrm{gen}}\,[\mathrm{kJ/(kg\,K)}],
  \qquad
  \dot S_{\mathrm{gen}}\,[\mathrm{kW/K}]$$

## Ciclo de Carnot y adición isotérmica

- Durante la adición isotérmica de calor de un ciclo de Carnot, el fluido recibe calor desde una fuente a temperatura constante.
- Para el fluido:
  $$\Delta S_{\mathrm{fluido}}=\frac{Q}{T}$$
- Para la fuente:
  $$\Delta S_{\mathrm{fuente}}=-\frac{Q}{T}$$
- En el límite ideal reversible, $\Delta S_{\mathrm{universo}}=0$. Si se produce una diferencia finita de temperatura entre fuente y fluido, el proceso real genera entropía.

## Problemas del listado

1. **Transferencia térmica directa:** entropía de dos depósitos y segunda ley.
2. **Evaporador con R-134a:** entropía del refrigerante, del espacio frío y del conjunto.
3. **Aluminio y hierro:** temperatura final y entropía de equilibrio térmico.
4. **Vapor enfriándose en recipiente rígido:** propiedades finales y cambio de entropía.
5. **Tanque rígido con agitador:** entropía de un gas ideal al aumentar su presión.
6. **Expansión isentrópica de aire:** temperatura final con tablas y aproximación de $k$ constante.
7. **Compresor isentrópico de nitrógeno:** trabajo mínimo de entrada.
8. **Turbina real de vapor:** estados ideal y real, eficiencia y potencia.
9. **Compresor de R-134a:** eficiencia isentrópica con tablas.
10. **Adición isotérmica de Carnot:** entropía del fluido, fuente y universo.
11. **Calentamiento eléctrico aislado:** cambio de entropía del agua.
12. **Compresión isentrópica de vapor:** temperatura y entalpía de salida.
13. **Bomba reversible:** trabajo específico con datos de entropía y aproximaciones de volumen.
14. **Bloques a un lago:** entropía de sólidos y reservorio.
15. **Turbina de gas:** trabajo máximo reversible por unidad de masa.
16. **Compresión reversible de vapor:** trabajo con volumen específico constante.
17. **Bomba de una central:** potencia reversible de entrada.
18. **Compresor de aire:** eficiencia y temperatura reversible de salida.
19. **Tobera de turborreactor:** eficiencia, velocidad y temperatura de salida.
20. **Compresor con pérdida de calor:** temperatura, trabajo y generación de entropía.
21. **Turbina con energía cinética:** flujo másico, temperatura y generación de entropía.
22. **Turbina de vapor:** generación de entropía a partir de estados y potencia.
23. **Justificación teórica:** máximo trabajo de una turbina isentrópica.
24. **Argón isentrópico:** temperatura y trabajo específico.
25. **Turbina con variación de velocidades:** flujo másico y eficiencia.
26. **Compresor de argón:** temperatura reversible y eficiencia isentrópica.

## Método de resolución

1. Identifica si el sistema es cerrado, abierto, rígido o adiabático.
2. Define los estados inicial y final; dibuja el diagrama $T$–$s$, $h$–$s$ o $P$–$v$ cuando resulte útil.
3. Determina si la sustancia es gas ideal, vapor, líquido o sólido y selecciona la relación o tabla correcta.
4. Aplica conservación de masa y balance de energía. Para sistemas estacionarios, incluye trabajo, calor y energías cinética y potencial relevantes.
5. Calcula el estado isentrópico con $s_2=s_1$ y presión igual a la presión real de salida.
6. Usa la eficiencia isentrópica para pasar del estado ideal al estado real.
7. Calcula entropía generada o cambio total del universo en procesos con transferencia de calor o irreversibilidades.
8. Convierte temperaturas a kelvin, revisa unidades y verifica que $S_{\mathrm{gen}}\geq0$.
