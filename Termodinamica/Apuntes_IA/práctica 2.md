---
tags:
  - certamen1_termo
seguimiento_certamen1: true
progreso_certamen1: true
bloque_certamen1: Calor, trabajo y energía
---

# Práctico 2 — Formas y transferencias de energía

[Listado del práctico](../02_Ejercicios_y_Guias/Pr%C3%A1cticaNr2_Termodin%C3%A1mica_2026-2.pdf) | [Solucionario](../02_Ejercicios_y_Guias/Pr%C3%A1cticaNr2SOLUCION_Termodin%C3%A1mica_2026-2%20%281%29.pdf) | Siguiente: [Práctico 3](./pr%C3%A1ctica%203.md)

## Formas de energía

- La energía total de un sistema es la suma de energía interna, cinética y potencial:
  $$E=U+E_{\mathrm{c}}+E_{\mathrm{p}}$$
- La energía cinética macroscópica se debe al movimiento del sistema como un todo; la potencial, a su posición en un campo gravitatorio; la interna agrupa las energías microscópicas asociadas al movimiento e interacción de moléculas.
  $$E_{\mathrm{c}}=\frac{mV^2}{2},\qquad E_{\mathrm{p}}=mgz$$
- Por unidad de masa:
  $$e=\frac{E}{m}=u+\frac{V^2}{2}+gz$$
  Las propiedades específicas se expresan habitualmente en $\mathrm{kJ/kg}$; si la velocidad está en $\mathrm{m/s}$, divide $V^2/2$ por 1000 para expresarlo en esas unidades.
- En muchos recipientes y equipos, los cambios de velocidad y altura son pequeños respecto del cambio de energía interna. Se pueden despreciar solo después de comprobarlo con los datos del problema.

## Calor, trabajo y potencia

- **Calor** ($Q$) es energía que cruza la frontera debido exclusivamente a una diferencia de temperatura. Puede transferirse por conducción, convección o radiación.
- **Trabajo** ($W$) es transferencia de energía por una interacción distinta del calor, como desplazamiento de una frontera, trabajo eléctrico o trabajo de eje. La clasificación depende del mecanismo, no del objeto: un motor que cruza la frontera transporta trabajo eléctrico o de eje, no “calor”.
- Calor y trabajo no son propiedades de estado: dependen de la trayectoria del proceso. En cambio, la energía almacenada sí es una propiedad; su cambio entre dos estados depende solo de los estados extremos.
- Las cantidades con punto representan tasas o potencias:
  $$\dot{Q}=\frac{dQ}{dt},\qquad \dot{W}=\frac{dW}{dt}$$
  La unidad de potencia es el watt; $1\,\mathrm{kW}=1\,\mathrm{kJ/s}$.
- La energía puede transportarse con masa que cruza una frontera abierta. En ese caso se contabiliza mediante propiedades específicas de la corriente, además del calor y el trabajo.

## Primera Ley para sistemas cerrados

- La Primera Ley es conservación de la energía. Con entradas positivas:
  $$\Delta E=Q_{\mathrm{entrada}}-Q_{\mathrm{salida}}+
  W_{\mathrm{entrada}}-W_{\mathrm{salida}}$$
- Equivalentemente, definiendo $Q>0$ hacia el sistema y $W>0$ hecho por el sistema:
  $$\Delta E=Q-W
  =\Delta U+\Delta E_{\mathrm{c}}+\Delta E_{\mathrm{p}}$$
- Si los cambios de velocidad y altura son despreciables, $\Delta E\approx\Delta U$. Si además el sistema es adiabático ($Q=0$), el trabajo que se realiza sobre él puede aumentar su energía interna; adiabático no significa temperatura constante.

## Cómo clasificar las interacciones

- La frontera elegida determina si una interacción es calor, trabajo o transporte de energía con masa. Por ejemplo, al analizar el contenido de un refrigerador como sistema, la electricidad entra como trabajo y el calor puede salir del contenido hacia el evaporador; al analizar el recinto completo, el motor entrega energía al recinto y el calor rechazado al exterior también forma parte del balance.
- Una interacción es calor solo si cruza la frontera por diferencia de temperatura. Si cruza electricidad por cables, es trabajo eléctrico; si cruza masa por una tubería, lleva energía asociada a esa corriente.
- Distingue energía transferida ($Q$, $W$) de su tasa ($\dot Q$, $\dot W$). Los problemas de potencia suelen entregar caudales másicos y velocidades, así que conviene hacer el balance directamente en tasas.

## Energía en sistemas abiertos

- Un volumen de control permite que masa atraviese su frontera. La corriente transporta energía interna, trabajo de flujo (incluido en la entalpía), energía cinética y potencial.
- La entalpía específica se define como:
  $$h=u+pv$$
  Es útil en el análisis de flujo porque el término $pv$ representa el trabajo requerido para empujar fluido a través de la frontera del volumen de control.
- En régimen estacionario, no hay acumulación neta de masa ni energía dentro del volumen de control, aunque puede haber transferencias continuas de entrada y salida.
- El caudal volumétrico y el másico se relacionan por:
  $$\dot{V}=AV,\qquad \dot{m}=\rho\dot{V}=\rho AV$$
  donde $A$ es el área de la sección y $V$ la velocidad media normal al área.

## Potencia de un flujo

- La energía mecánica que transporta un flujo con velocidad $V$ es $\dot{m}V^2/2$; su tasa de cambio entre entrada y salida puede convertirse en potencia de eje, como en una turbina o aerogenerador.
- Si un fluido cae una altura $H$, la tasa de disminución de energía potencial gravitatoria es $\dot{m}gH$. Solo una parte puede convertirse en potencia útil debido a pérdidas e irreversibilidades.
- Para un rotor con aire uniforme, el área barrida es $A=\pi D^2/4$ y el flujo de energía cinética incidente es:
  $$\dot{E}_{\mathrm{c}}=\frac{1}{2}\rho AV^3$$
  Esta es la potencia cinética disponible en el flujo, no necesariamente la potencia eléctrica obtenida.

## Situaciones típicas de conversión de energía

- **Elevación o descenso de un cuerpo:** el cambio de energía potencial gravitatoria es $\Delta E_{\mathrm{p}}=mg(z_2-z_1)$. Al elevarlo, aumenta la energía del sistema; al descender, esa energía puede transformarse en trabajo o cinética.
- **Agua que cae hacia una turbina:** con caudal másico $\dot m$, la tasa de energía potencial disponible es aproximadamente $\dot m gH$. La potencia real se reduce por pérdidas hidráulicas y por eficiencias de la turbina/generador.
- **Viento sobre un rotor:** calcula primero el área barrida y el flujo másico del aire, $\dot m=\rho AV$. La potencia cinética que atraviesa esa área es $\dot mV^2/2$. No toda puede extraerse: el aire debe conservar velocidad de salida y existen pérdidas de conversión.
- **Cambio de altura y velocidad simultáneos:** usa la diferencia total de energía mecánica específica, $(V_2^2-V_1^2)/2+g(z_2-z_1)$, en lugar de considerar solo el término más evidente.
- **Dispositivo en una habitación:** especifica si el sistema es el aparato, su contenido o toda la habitación. Cambiar la frontera puede cambiar qué energía aparece como calor, trabajo o energía transportada, sin alterar la conservación total.

## Selección del balance correcto

- Para masa fija, no hay términos de transporte de masa; la Primera Ley se escribe con cambios de energía del sistema y calor/trabajo.
- Para un volumen de control estacionario, no hay acumulación neta de masa ni energía, pero sí puede haber flujos de entrada/salida que transportan energía. La entalpía incorpora el trabajo de flujo.
- Si se comparan estados de un fluido, usa propiedades específicas compatibles con su fase. Para gas ideal puede calcularse la densidad con presión absoluta y temperatura absoluta; para agua o refrigerantes, consulta tablas.
- Un balance global puede ocultar transferencias internas entre componentes. Si una máquina acciona un generador, el trabajo que sale de una parte y entra a otra se cancela al tomar el conjunto como sistema, pero no al analizar cada equipo por separado.

## Estrategia de análisis

1. Define el sistema o volumen de control y representa entradas, salidas e interacciones de energía.
2. Escribe la Primera Ley con una convención de signos explícita y consistente.
3. Decide si corresponde un sistema cerrado o abierto; no cuentes energía transportada por masa en un sistema cerrado.
4. Elige la forma de energía pertinente: interna para cambios térmicos, cinética para velocidad, potencial para altura y entalpía para corrientes.
5. Convierte unidades antes de sumar términos. Verifica que energía se exprese, por ejemplo, en kJ y potencia en kW.
6. Desprecia términos de velocidad, altura, calor o trabajo solo cuando la configuración o los datos lo justifiquen.
