---
tags:
  - certamen1_termo
seguimiento_certamen1: true
progreso_certamen1: true
bloque_certamen1: Sistemas abiertos y flujo estacionario
---

# Práctico 5 — Sistemas abiertos

[Listado del práctico](../02_Ejercicios_y_Guias/Pr%C3%A1cticaNr5_Termodin%C3%A1mica_2026-2.pdf.pdf) | [Solucionario](../02_Ejercicios_y_Guias/Pr%C3%A1cticaNr5_Termodin%C3%A1mica_2026-2%20resoluci%C3%B3n.pdf)

## Volumen de control y flujo

- Un sistema abierto se analiza como un **volumen de control** delimitado por una superficie de control. Masa y energía pueden cruzar esa superficie.
- Un dispositivo de flujo estacionario se encuentra en régimen estacionario cuando las propiedades en cada punto y las tasas de entrada y salida no cambian con el tiempo. Puede haber flujo continuo sin acumulación dentro del equipo.
- Las corrientes transportan masa y energía. Para una corriente uniforme que atraviesa una sección:
  $$\dot{V}=AV,\qquad \dot{m}=\rho AV$$
  donde $\dot{V}$ es caudal volumétrico, $\dot{m}$ caudal másico, $A$ área normal al flujo, $V$ velocidad media y $\rho$ densidad.
- Para un gas ideal, $\rho=p/(RT)$ con presión absoluta y temperatura en kelvin. Si cambia el estado del gas, puede cambiar su densidad y, con ella, el caudal volumétrico aunque el caudal másico se conserve.

## Balance de masa

- La acumulación de masa dentro del volumen de control es entrada menos salida:
  $$\frac{dm_{\mathrm{VC}}}{dt}
  =\sum\dot{m}_{\mathrm{entrada}}-\sum\dot{m}_{\mathrm{salida}}$$
- En régimen estacionario:
  $$\sum\dot{m}_{\mathrm{entrada}}=\sum\dot{m}_{\mathrm{salida}}$$
  Para una entrada y una salida, $\dot{m}_1=\dot{m}_2$. Esto no implica que las velocidades o caudales volumétricos sean iguales si cambian el área o la densidad.
- En un proceso transitorio sí puede acumularse o agotarse masa en el volumen de control; no se puede imponer igualdad instantánea entre flujos sin comprobarlo.

## Entalpía y energía transportada

- La entalpía específica combina energía interna y trabajo de flujo:
  $$h=u+pv$$
- Cada unidad de masa que cruza la frontera lleva entalpía, energía cinética específica y energía potencial específica:
  $$e_{\mathrm{flujo}}=h+\frac{V^2}{2}+gz$$
- La tasa de transferencia de energía con una corriente es el producto del caudal másico por la energía específica transportada. Por eso las propiedades deben corresponder al estado de esa corriente en la sección de entrada o salida.

## Primera Ley en régimen estacionario

- Para un volumen de control con una entrada y una salida, usando $\dot{Q}>0$ hacia el volumen y $\dot{W}>0$ producido por el volumen:
  $$\dot{Q}-\dot{W}
  =\dot{m}\left[(h_2-h_1)+\frac{V_2^2-V_1^2}{2}
  +g(z_2-z_1)\right]$$
- Con varias corrientes, la forma general es:
  $$\dot{Q}-\dot{W}
  =\sum_{\mathrm{salidas}}\dot{m}\left(h+\frac{V^2}{2}+gz\right)
  -\sum_{\mathrm{entradas}}\dot{m}\left(h+\frac{V^2}{2}+gz\right)$$
- En un proceso transitorio, debe incluirse la acumulación de energía dentro del volumen de control, $dE_{\mathrm{VC}}/dt$, además de las tasas de energía que cruzan la frontera.
- Los cambios de energía cinética son importantes en boquillas, difusores y chorros; los de energía potencial pueden ser importantes en equipos con gran desnivel. En otros dispositivos pueden ser despreciables, pero se debe justificar.

## Balance general y situaciones transitorias

- Con la convención $\dot Q>0$ hacia el volumen de control y $\dot W>0$ saliendo como trabajo, el balance de masa y energía general es:
  $$\frac{dm_{\mathrm{VC}}}{dt}
  =\sum_{\mathrm{ent}}\dot m-\sum_{\mathrm{sal}}\dot m$$
  $$\frac{dE_{\mathrm{VC}}}{dt}
  =\dot Q-\dot W
  +\sum_{\mathrm{ent}}\dot m\left(h+\frac{V^2}{2}+gz\right)
  -\sum_{\mathrm{sal}}\dot m\left(h+\frac{V^2}{2}+gz\right)$$
- En régimen estacionario, los términos de acumulación son cero. En llenado o vaciado de un tanque no lo son: se deben integrar los balances en el tiempo o relacionar los estados inicial y final con la masa que entra/sale.
- Para un tanque rígido con una entrada y sin salida, no existe trabajo de frontera en la pared; puede, sin embargo, haber calor y energía transportada por la corriente entrante. El estado final requiere un balance de masa y otro de energía.

## Simplificaciones y aplicaciones

- **Turbina:** normalmente entrega trabajo de eje; una caída de entalpía puede convertirse en trabajo y/o cambios de velocidad y altura.
- **Compresor o bomba:** recibe trabajo para aumentar la presión o la entalpía del fluido.
- **Tubería o intercambiador:** puede haber transferencia de calor; el trabajo de eje suele ser nulo si no hay máquina rotatoria.
- **Boquilla/difusor:** suelen aproximarse como adiabáticos y sin trabajo; la entalpía se intercambia principalmente con energía cinética.
- Estas son idealizaciones habituales, no reglas automáticas. Revisa siempre si el enunciado permite asumir adiabaticidad, régimen estacionario o cambios de altura despreciables.

## Modelo de dispositivos y atajos justificados

- **Turbina adiabática**, una entrada/salida, cambios de energía cinética/potencial pequeños:
  $$\dot W_{\mathrm{salida}}\approx\dot m(h_1-h_2)$$
  Una caída de entalpía disponible produce trabajo; si la salida tiene velocidad elevada, parte de la caída aparece como energía cinética.
- **Compresor adiabático**, sin cambios cinéticos/potenciales:
  $$\dot W_{\mathrm{entrada}}\approx\dot m(h_2-h_1)$$
  El trabajo eleva la entalpía y, normalmente, la presión del gas.
- **Boquilla adiabática sin trabajo:**
  $$h_1+\frac{V_1^2}{2}\approx h_2+\frac{V_2^2}{2}$$
  Si el cambio de entalpía es grande, la velocidad de salida puede aumentar. Usa unidades consistentes al combinar kJ/kg con $V^2/2$ en J/kg.
- **Intercambiador de calor:** si se toma como sistema el equipo completo y se desprecia intercambio con el entorno y trabajo de eje, el calor que pierde una corriente es el que recibe la otra. Se conserva energía total, aunque cambie la temperatura de ambas.
- **Mezclador:** se aplican balances de masa y energía a todas las entradas y salidas. Las propiedades de salida no son, en general, el promedio simple de temperaturas; se pondera energía (entalpía) y se consulta el estado de la mezcla.
- **Pérdidas de presión y calentamiento de una tubería:** calcula primero el caudal másico por continuidad. Para un gas, cambios de $p,T$ alteran $\rho$; no asumas velocidad constante si cambian área o densidad.

## Cómo abordar ejercicios con aire ideal

- Si el aire se modela como gas ideal, usa $pv=RT$ con presión absoluta y kelvin. A partir de $v=RT/p$ se obtiene la densidad $\rho=1/v=p/(RT)$.
- En una tubería de área $A$, con estado local conocido:
  $$\dot V=AV,\qquad \dot m=\rho AV$$
  Calcula $\dot m$ en una sección y úsalo para la otra sección si el régimen es estacionario y no hay ramificaciones ni acumulación. Luego despeja la velocidad/caudal volumétrico de salida con sus propiedades locales.
- Para determinar el flujo de calor agregado, primero resuelve continuidad y estados; luego sustituye las entalpías/velocidades en el balance de energía. No mezcles presión manométrica en la ecuación de gas ideal.

## Método de resolución

1. Dibuja el volumen de control y etiqueta cada entrada, salida, calor y trabajo.
2. Escribe el balance de masa para hallar caudales desconocidos.
3. Usa propiedades de cada corriente (tablas o gas ideal) para obtener $h$, $v$, $\rho$ u otras cantidades requeridas.
4. Decide si el proceso es estacionario o transitorio y conserva los términos de acumulación cuando corresponda.
5. Aplica la Primera Ley con una convención de signos explícita. Incluye energía cinética y potencial antes de decidir si son despreciables.
6. Comprueba dimensiones: $\dot{m}$ en $\mathrm{kg/s}$ multiplicado por una diferencia de energía específica en $\mathrm{kJ/kg}$ da potencia en $\mathrm{kW}$.
