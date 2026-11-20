---
tags:
  - certamen1_termo
seguimiento_certamen1: true
progreso_certamen1: true
bloque_certamen1: Introducción y conceptos fundamentales
---

# Práctico 1 — Conceptos fundamentales

[Listado del práctico](../02_Ejercicios_y_Guias/Pr%C3%A1cticaNr1_Termodin%C3%A1mica_2026-2.pdf) | [Solucionario](../02_Ejercicios_y_Guias/Pr%C3%A1cticaNr1SOLUCION_Termodin%C3%A1mica_2026-2%20%281%29.pdf) | [Apunte manuscrito](../02_Ejercicios_y_Guias/pr%C3%A1ctica%201/pr%C3%A1ctica%201.pdf) | [Taller N°1 (Barco)](../02_Ejercicios_y_Guias/20260812_Tallern%C2%B01_barco.pdf) | Siguiente: [Práctico 2](./pr%C3%A1ctica%202.md)

## Sistema, entorno y propiedades

- Un **sistema** es la cantidad de materia o región que se estudia; su frontera puede ser real o imaginaria. Todo lo que queda fuera es el entorno.
- En un **sistema cerrado** no cruza masa la frontera, aunque sí puede cruzar energía. En un **sistema abierto** cruzan masa y energía. Un sistema **aislado** no intercambia ni masa ni energía.
- Una **propiedad** describe el estado del sistema. Las propiedades extensivas dependen de la cantidad de materia (masa, volumen, energía); las intensivas no (presión, temperatura, densidad). Una propiedad específica es extensiva dividida por la masa, por ejemplo $v=V/m$.
- El **estado** queda definido por un conjunto suficiente de propiedades independientes. Un cambio de estado conecta un estado inicial con uno final; un proceso describe cómo ocurre ese cambio.

## Equilibrio y temperatura

- Un sistema está en equilibrio termodinámico cuando no hay tendencias espontáneas a cambiar sus propiedades. Puede requerir equilibrio térmico, mecánico y químico.
- La **ley cero** establece que si dos sistemas están por separado en equilibrio térmico con un tercero, están en equilibrio térmico entre sí. Esto fundamenta la medición de temperatura.
- La temperatura mide el estado térmico y determina la dirección de la transferencia espontánea de calor: el calor fluye del cuerpo de mayor temperatura al de menor temperatura hasta alcanzar el equilibrio térmico. Calor no es algo “contenido” en el sistema, sino energía en tránsito por diferencia de temperatura.
- Escalas y conversiones:
  $$T(\mathrm{K})=t(^{\circ}\mathrm{C})+273{,}15$$
  $$t(^{\circ}\mathrm{F})=\frac{9}{5}t(^{\circ}\mathrm{C})+32,\qquad
  t(^{\circ}\mathrm{C})=\frac{5}{9}\left[t(^{\circ}\mathrm{F})-32\right]$$
- Kelvin es una escala absoluta: $0\,\mathrm{K}$ es el cero absoluto. En ecuaciones de estado y relaciones termodinámicas se debe usar temperatura absoluta.
- En diferencias de temperatura no se suma ni resta 273,15:
  $$\Delta T(\mathrm{K})=\Delta t(^{\circ}\mathrm{C}),\qquad
  \Delta t(^{\circ}\mathrm{F})=\frac{9}{5}\Delta t(^{\circ}\mathrm{C})$$

## Presión

- La presión es la fuerza normal por unidad de área:
  $$p=\frac{F_n}{A}$$
  En el SI, $1\,\mathrm{Pa}=1\,\mathrm{N/m^2}$ y $1\,\mathrm{kPa}=1000\,\mathrm{Pa}$. La presión de un fluido en reposo actúa perpendicularmente a las superficies que contacta.
- La **presión absoluta** se mide desde el vacío; la **manométrica** se mide desde la presión atmosférica local:
  $$p_{\mathrm{abs}}=p_{\mathrm{atm}}+p_{\mathrm{man}}$$
  Una presión manométrica negativa indica que la presión es menor que la atmosférica, pero la presión absoluta no puede ser negativa.
- Conversiones habituales: $1\,\mathrm{atm}=101{,}325\,\mathrm{kPa}=101\,325\,\mathrm{Pa}$ y $1\,\mathrm{psi}=6{,}89476\,\mathrm{kPa}$.
- En un fluido estático de densidad constante, el cambio de presión con la altura cumple $\Delta p=\rho g\Delta h$ en magnitud. La presión aumenta al descender. En un manómetro, la diferencia de niveles permite hallar una diferencia de presión; se debe seguir la columna fluida paso a paso para determinar el signo.
- Para un pistón en equilibrio, se hace un balance de fuerzas. Si atmósfera, peso y resorte empujan hacia abajo y el gas hacia arriba:
  $$p_{\mathrm{gas}}=p_{\mathrm{atm}}+\frac{mg+F_{\mathrm{resorte}}}{A}$$
  La relación cambia si las fuerzas o el movimiento tienen otra orientación.

## Gas ideal y cambios de estado

- El modelo de gas ideal relaciona presión, volumen y temperatura:
  $$pV=nR_{\mathrm{u}}T=mRT$$
  Aquí $p$ es absoluta, $V$ volumen total, $n$ cantidad de sustancia, $m$ masa, $R_{\mathrm{u}}$ constante universal y $R$ constante específica del gas. La temperatura debe estar en kelvin.
- Para una masa fija, entre dos estados del mismo gas:
  $$\frac{p_1V_1}{T_1}=\frac{p_2V_2}{T_2}$$
  De aquí se obtienen casos particulares: a volumen constante $p/T$ es constante; a presión constante $V/T$ es constante.
- Un gas real se aproxima mejor al modelo ideal cuando su densidad es baja (presiones relativamente bajas y temperaturas suficientemente altas respecto de la saturación). Si el gas está cerca de condensarse, se requieren propiedades reales.
- En un cilindro con pistón móvil, una carga exterior constante puede mantener la presión aproximadamente fija mientras el gas se expande al calentarse. Si el pistón alcanza topes, el volumen deja de cambiar; al seguir calentando, aumentan la temperatura y la presión.

## Lectura termodinámica de situaciones típicas

- **Misma temperatura no significa misma presión.** Para comparar gases se necesita información suficiente sobre cantidad de gas, volumen y modelo de sustancia. En un gas ideal la presión depende de $nT/V$; dos gases a igual temperatura pueden tener presiones distintas si cambia $n$ o $V$.
- **Mismo gas no significa misma presión.** En recipientes de igual volumen, con igual cantidad de gas ideal, una temperatura mayor implica mayor presión. Si las cantidades o volúmenes difieren, no se puede comparar la presión solo conociendo la temperatura.
- **Cilindro con pistón móvil:** mientras el pistón pueda desplazarse libremente y la carga no cambie, el gas se ajusta mecánicamente a una presión exterior casi constante. El calentamiento causa expansión; el enfriamiento, compresión.
- **Pistón que llega a topes:** a partir del contacto, el volumen queda fijo. Si se sigue calentando una cantidad fija de gas ideal, aumenta su temperatura y también la presión. El proceso tiene dos tramos con restricciones distintas y se deben analizar por separado.
- **Gas encerrado en un recipiente rígido:** si no hay fuga, la masa y el volumen son constantes. Para un gas ideal, $p/T$ permanece constante entre estados, pero las presiones de esa relación deben ser absolutas.

## Presión hidrostática y manómetros: método de recorrido

- En un fluido estático, entre dos puntos del mismo fluido a densidad constante:
  $$p_2-p_1=\rho g(z_1-z_2)$$
  Si el punto 2 está más bajo que el punto 1, su presión es mayor. En líquidos con densidad variable se requiere integrar la relación hidrostática.
- En un manómetro con varios fluidos, parte desde una presión conocida y recorre la columna: al bajar una altura $h$ en un fluido se suma $\rho gh$; al subir se resta. La presión es continua en una interfaz entre fluidos inmiscibles.
- La relación $\Delta p=\rho g\Delta h$ es una diferencia de presión, no necesariamente presión absoluta. Primero calcula la diferencia y después usa la presión atmosférica si se pide presión absoluta.
- En un pistón de área $A$, todas las presiones aplicadas generan fuerzas $pA$. Incluye presión atmosférica en el lado expuesto, peso del pistón/carga y fuerza del resorte, cuidando qué dirección tiene cada una.

## Temperatura, contacto térmico y calor

- Si dos sistemas inicialmente a distinta temperatura se ponen en contacto térmico dentro de un conjunto aislado, el calor cedido por el caliente es igual al recibido por el frío, siempre que no haya otras formas de trabajo o cambios de energía relevantes.
- Para un cuerpo que no cambia de fase y tiene calor específico aproximadamente constante, el cambio de energía sensible puede estimarse como $Q=mc\Delta T$. Esta relación no sustituye tablas durante un cambio de fase: allí se requiere calor latente o propiedades de saturación.
- La dirección del calor se determina comparando temperaturas, no energías internas totales: un objeto pequeño a mayor temperatura puede entregar calor a uno grande a menor temperatura.

## Método para resolver los ejercicios

1. Define el sistema, dibuja su frontera y anota qué intercambia con el entorno.
2. Distingue temperaturas de diferencias de temperatura; convierte siempre a kelvin cuando uses una ecuación de estado.
3. En gases ideales, usa presión absoluta. En manómetros y pistones, plantea primero la relación hidrostática o el equilibrio de fuerzas.
4. Identifica qué permanece constante antes de usar una relación entre dos estados.
5. Si un proceso cambia de restricción (pistón móvil y luego topes), separa los tramos y usa la condición correcta en cada estado.
6. Revisa unidades, sentido físico y consistencia: por ejemplo, $p_{\mathrm{abs}}>0$ y un aumento de temperatura a volumen fijo debe aumentar la presión del gas ideal.
