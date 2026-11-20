---
tags:
  - certamen2_termo
---

# Ensayos de práctica — Test 4

Estos ensayos originales practican los temas anunciados para el Test 4: Segunda Ley, máquinas térmicas, refrigeradores y bombas de calor. El formato sigue el estilo aplicado de los tests anteriores: situaciones físicas, datos de operación y varias etapas de análisis.

Cada ensayo contiene **exactamente dos preguntas**. Intenta resolver primero todos los enunciados; las pautas están al final, separadas para facilitar la autocorrección. Supón dispositivos cíclicos en régimen estacionario y reservorios térmicos a temperatura constante, salvo que se indique lo contrario.

## Ensayo 1

### Pregunta 1 — Máquina térmica y límite de Carnot

Una máquina térmica recibe calor desde un foco a $627\,^{\circ}\mathrm{C}$ a una tasa de $900\,\mathrm{kJ/min}$. Rechaza calor a un foco que se encuentra a $27\,^{\circ}\mathrm{C}$. La potencia mecánica producida equivale a una tasa de trabajo de $450\,\mathrm{kJ/min}$.

a) Determine la tasa de calor rechazada y el rendimiento térmico de la máquina.  
b) Calcule el rendimiento máximo posible entre esos dos focos.  
c) Decida si la máquina propuesta es imposible, reversible o compatible con una máquina real irreversible. Justifique usando la Primera y la Segunda Ley.

### Pregunta 2 — Refrigerador de una cámara de conservación

Una cámara de conservación debe mantenerse a $4\,^{\circ}\mathrm{C}$ mientras el ambiente está a $30\,^{\circ}\mathrm{C}$. El refrigerador extrae $18\,000\,\mathrm{kJ}$ de la cámara durante un período de 2 horas. Su COP real es 3,2.

a) Determine la tasa de refrigeración y la potencia de entrada requerida.  
b) Calcule la tasa de calor que el refrigerador entrega al ambiente.  
c) Determine el COP máximo reversible entre esos focos y evalúe si el COP real es posible.

## Ensayo 2

### Pregunta 1 — Bomba de calor para calefacción

Una bomba de calor entrega $20\,\mathrm{kW}$ de calor a una vivienda cuya temperatura interior se mantiene en $45\,^{\circ}\mathrm{C}$. Extrae calor del exterior a $-5\,^{\circ}\mathrm{C}$ y opera con $COP_{\mathrm{BC}}=4{,}0$.

a) Determine la potencia eléctrica consumida y la tasa de calor extraída del exterior.  
b) Calcule el COP máximo reversible de calefacción entre ambos focos.  
c) Evalúe la posibilidad del equipo según la Segunda Ley e indique la relación entre $COP_{\mathrm{BC}}$ y $COP_{\mathrm{R}}$ para este mismo ciclo.

### Pregunta 2 — Central térmica

Una central opera entre una fuente caliente a $800\,^{\circ}\mathrm{C}$ y un río a $25\,^{\circ}\mathrm{C}$. Recibe calor a una tasa de $1{,}20\,\mathrm{MW}$ y descarga $0{,}72\,\mathrm{MW}$ al río.

a) Determine la potencia neta producida y el rendimiento térmico.  
b) Calcule el rendimiento de Carnot entre esos focos y evalúe la central.  
c) Si opera durante 5 horas en las mismas condiciones, determine el trabajo neto producido y el calor recibido en ese período.

## Ensayo 3

### Pregunta 1 — Máquinas térmicas en cascada

Dos máquinas térmicas operan en serie. La primera recibe calor a $900\,\mathrm{K}$ a una tasa de $500\,\mathrm{kW}$ y rechaza su calor al foco intermedio a $600\,\mathrm{K}$. Su rendimiento térmico es 0,30. La segunda recibe íntegramente el calor rechazado por la primera, opera entre $600\,\mathrm{K}$ y $300\,\mathrm{K}$ y tiene un rendimiento de 0,40.

a) Determine la potencia producida por cada máquina y el calor rechazado finalmente al foco de $300\,\mathrm{K}$.  
b) Calcule la potencia total y el rendimiento global respecto del calor que entra a la primera máquina.  
c) Compruebe los límites de Carnot para cada máquina y para el conjunto que opera entre $900\,\mathrm{K}$ y $300\,\mathrm{K}$.

### Pregunta 2 — Refrigerador y trabajo mínimo

Un refrigerador extrae calor de una cámara a $5\,^{\circ}\mathrm{C}$ y lo descarga a una sala a $35\,^{\circ}\mathrm{C}$. La tasa de refrigeración es $12\,\mathrm{kW}$ y el COP real del equipo es 2,5.

a) Determine la potencia de entrada y la tasa de calor rechazada a la sala.  
b) Calcule el COP reversible máximo para esas temperaturas.  
c) Determine la potencia mínima que requeriría un refrigerador reversible para entregar la misma tasa de refrigeración y explique qué representa la diferencia respecto del equipo real.

---

# Pautas de resolución

## Ensayo 1

### Pregunta 1

En un ciclo, el cambio neto de energía del fluido de trabajo es cero. El balance es:

$$\dot{Q}_{\mathrm{H}}=\dot{W}_{\mathrm{neto}}+\dot{Q}_{\mathrm{L}}$$

a) Entonces:

$$\dot{Q}_{\mathrm{L}}=900-450=450\,\mathrm{kJ/min}$$

$$\eta_{\mathrm{th}}=\frac{\dot{W}_{\mathrm{neto}}}{\dot{Q}_{\mathrm{H}}}
=\frac{450}{900}=0{,}50=50\%$$

b) Las temperaturas absolutas son $T_{\mathrm{H}}=627+273{,}15=900{,}15\,\mathrm{K}$ y $T_{\mathrm{L}}=27+273{,}15=300{,}15\,\mathrm{K}$. Por Carnot:

$$\eta_{\mathrm{Carnot}}=1-\frac{300{,}15}{900{,}15}\approx0{,}6666=66{,}66\%$$

c) El balance de energía cierra: $900=450+450$. Además, $0{,}50<0{,}6666$, por lo que la máquina no supera el límite de Carnot. Es compatible con una máquina irreversible real; no es reversible porque su rendimiento es menor que el máximo reversible.

### Pregunta 2

a) El período es $\Delta t=2\,\mathrm{h}=7200\,\mathrm{s}$. La tasa de calor extraída es:

$$\dot{Q}_{\mathrm{L}}=\frac{18\,000\,\mathrm{kJ}}{7200\,\mathrm{s}}
=2{,}5\,\mathrm{kJ/s}=2{,}5\,\mathrm{kW}$$

Como $COP_{\mathrm{R}}=\dot{Q}_{\mathrm{L}}/\dot{W}_{\mathrm{entrada}}$:

$$\dot{W}_{\mathrm{entrada}}=\frac{2{,}5}{3{,}2}
=0{,}78125\,\mathrm{kW}$$

b) Del balance del refrigerador:

$$\dot{Q}_{\mathrm{H}}=\dot{Q}_{\mathrm{L}}+\dot{W}_{\mathrm{entrada}}
=2{,}5+0{,}78125=3{,}28125\,\mathrm{kW}$$

c) $T_{\mathrm{L}}=277{,}15\,\mathrm{K}$ y $T_{\mathrm{H}}=303{,}15\,\mathrm{K}$:

$$COP_{\mathrm{R,rev}}=\frac{T_{\mathrm{L}}}{T_{\mathrm{H}}-T_{\mathrm{L}}}
=\frac{277{,}15}{303{,}15-277{,}15}\approx10{,}66$$

Como $3{,}2<10{,}66$, el equipo no viola el límite reversible y es compatible con un refrigerador real irreversible.

## Ensayo 2

### Pregunta 1

a) Para una bomba de calor:

$$COP_{\mathrm{BC}}=\frac{\dot{Q}_{\mathrm{H}}}{\dot{W}_{\mathrm{entrada}}}$$

Por tanto:

$$\dot{W}_{\mathrm{entrada}}=\frac{20}{4{,}0}=5\,\mathrm{kW}$$

El balance da la tasa extraída del exterior:

$$\dot{Q}_{\mathrm{L}}=\dot{Q}_{\mathrm{H}}-\dot{W}_{\mathrm{entrada}}
=20-5=15\,\mathrm{kW}$$

b) $T_{\mathrm{H}}=45+273{,}15=318{,}15\,\mathrm{K}$ y $T_{\mathrm{L}}=-5+273{,}15=268{,}15\,\mathrm{K}$. Así:

$$COP_{\mathrm{BC,rev}}=\frac{T_{\mathrm{H}}}{T_{\mathrm{H}}-T_{\mathrm{L}}}
=\frac{318{,}15}{50}\approx6{,}36$$

c) El COP real, 4,0, es menor que el máximo reversible de aproximadamente 6,36; el funcionamiento es posible y consistente con irreversibilidades. Para el mismo ciclo:

$$COP_{\mathrm{BC}}=COP_{\mathrm{R}}+1$$

Por consiguiente, $COP_{\mathrm{R}}=4{,}0-1=3{,}0$.

### Pregunta 2

a) Para la central, la Primera Ley en régimen estacionario y ciclo da:

$$\dot{W}_{\mathrm{neto}}=\dot{Q}_{\mathrm{H}}-\dot{Q}_{\mathrm{L}}
=1{,}20-0{,}72=0{,}48\,\mathrm{MW}$$

$$\eta_{\mathrm{th}}=\frac{0{,}48}{1{,}20}=0{,}40=40\%$$

b) $T_{\mathrm{H}}=1073{,}15\,\mathrm{K}$ y $T_{\mathrm{L}}=298{,}15\,\mathrm{K}$:

$$\eta_{\mathrm{Carnot}}=1-\frac{298{,}15}{1073{,}15}
\approx0{,}7222=72{,}22\%$$

El rendimiento real es inferior al de Carnot; por tanto, el desempeño es posible y corresponde a una máquina irreversible, no reversible.

c) En 5 horas:

$$W_{\mathrm{neto}}=(0{,}48\,\mathrm{MW})(5\,\mathrm{h})=2{,}40\,\mathrm{MWh}$$

$$Q_{\mathrm{H}}=(1{,}20\,\mathrm{MW})(5\,\mathrm{h})=6{,}00\,\mathrm{MWh}$$

Como comprobación, el calor descargado en ese período es $(0{,}72)(5)=3{,}60\,\mathrm{MWh}$ y $6{,}00=2{,}40+3{,}60$.

## Ensayo 3

### Pregunta 1

a) Primera máquina:

$$\dot{W}_1=\eta_1\dot{Q}_{\mathrm{H},1}
=(0{,}30)(500)=150\,\mathrm{kW}$$

$$\dot{Q}_{\mathrm{L},1}=500-150=350\,\mathrm{kW}$$

Ese calor es la entrada de la segunda máquina:

$$\dot{W}_2=\eta_2\dot{Q}_{\mathrm{H},2}
=(0{,}40)(350)=140\,\mathrm{kW}$$

$$\dot{Q}_{\mathrm{L},2}=350-140=210\,\mathrm{kW}$$

b) La potencia total es:

$$\dot{W}_{\mathrm{total}}=150+140=290\,\mathrm{kW}$$

El calor intermedio de $350\,\mathrm{kW}$ se transfiere internamente entre las máquinas y no se suma al calor externo de entrada. Por eso:

$$\eta_{\mathrm{global}}=\frac{290}{500}=0{,}58=58\%$$

También se verifica el balance global: $500=290+210$.

c) Los límites de Carnot individuales son:

$$\eta_{\mathrm{Carnot},1}=1-\frac{600}{900}=\frac{1}{3}\approx0{,}3333$$

$$\eta_{\mathrm{Carnot},2}=1-\frac{300}{600}=0{,}50$$

Los rendimientos reales de 0,30 y 0,40 son inferiores a sus respectivos límites. Para el conjunto entre $900\,\mathrm{K}$ y $300\,\mathrm{K}$:

$$\eta_{\mathrm{Carnot,global}}=1-\frac{300}{900}=\frac{2}{3}\approx0{,}6667$$

El rendimiento global de 0,58 también es menor que ese límite. Las tres comparaciones son consistentes con dispositivos irreversibles posibles.

### Pregunta 2

a) El consumo de potencia es:

$$\dot{W}_{\mathrm{entrada}}=\frac{\dot{Q}_{\mathrm{L}}}{COP_{\mathrm{R}}}
=\frac{12}{2{,}5}=4{,}8\,\mathrm{kW}$$

El calor descargado a la sala es:

$$\dot{Q}_{\mathrm{H}}=\dot{Q}_{\mathrm{L}}+\dot{W}_{\mathrm{entrada}}
=12+4{,}8=16{,}8\,\mathrm{kW}$$

b) $T_{\mathrm{L}}=278{,}15\,\mathrm{K}$ y $T_{\mathrm{H}}=308{,}15\,\mathrm{K}$:

$$COP_{\mathrm{R,rev}}=\frac{278{,}15}{308{,}15-278{,}15}
\approx9{,}27$$

El COP real de 2,5 está bajo el máximo reversible.

c) Para el mismo efecto de refrigeración, un equipo reversible requeriría:

$$\dot{W}_{\min}=\frac{\dot{Q}_{\mathrm{L}}}{COP_{\mathrm{R,rev}}}
=\frac{12}{9{,}27}\approx1{,}29\,\mathrm{kW}$$

La diferencia, $4{,}8-1{,}29\approx3{,}51\,\mathrm{kW}$, es el exceso de potencia que consume el equipo real respecto del mínimo termodinámico reversible para esta transferencia. Se asocia a sus irreversibilidades; no es trabajo “perdido” que pueda recuperarse íntegramente en un equipo real.
