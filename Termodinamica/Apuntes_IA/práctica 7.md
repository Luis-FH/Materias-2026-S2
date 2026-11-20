---
tags:
  - certamen2_termo
seguimiento_certamen2: true
progreso_certamen2: false
bloque_certamen2: Refrigeradores y bombas de calor
---

# Práctico 7 — Refrigeradores y bombas de calor

[Ver enunciado del práctico](../02_Ejercicios_y_Guias/Pr%C3%A1cticaNr7_Termodin%C3%A1mica_2026-2.pdf) | [Guía ayudantía](../02_Ejercicios_y_Guias/Guia_Practica_7_ayudantia.pdf) | [Repaso Test 4](../01_Teoria_y_Conceptos/Repaso%20Test%204%20-%20Segunda%20Ley%20y%20Refrigeradores.md) | Siguiente: [Práctico 8](./pr%C3%A1ctica%208.md)

## Focos térmicos y ciclo inverso

- Un **foco térmico** es un cuerpo o región suficientemente grande para recibir o entregar calor sin que su temperatura cambie apreciablemente.
- Un refrigerador opera en ciclo y transfiere calor desde un espacio frío ($T_{\mathrm{L}}$) hacia un entorno más caliente ($T_{\mathrm{H}}$). Como ese sentido no ocurre espontáneamente, requiere trabajo de entrada.
- La bomba de calor opera con el mismo ciclo, pero el efecto útil es calentar el espacio caliente. La diferencia entre refrigerador y bomba de calor está en el objetivo, no en la dirección del ciclo.
- Para un ciclo, el estado del fluido de trabajo vuelve al punto inicial, de modo que el cambio neto de energía almacenada es cero. La Primera Ley da:
  $$Q_{\mathrm{H}}=Q_{\mathrm{L}}+W_{\mathrm{entrada}}$$
  El calor rechazado al foco caliente es mayor que el extraído del foco frío porque también incluye el trabajo suministrado.

## Coeficiente de desempeño

- El **coeficiente de desempeño** (COP) compara el efecto útil con el trabajo requerido:
  $$COP_{\mathrm{R}}=\frac{Q_{\mathrm{L}}}{W_{\mathrm{entrada}}},\qquad
  COP_{\mathrm{BC}}=\frac{Q_{\mathrm{H}}}{W_{\mathrm{entrada}}}$$
- Si se analiza funcionamiento por unidad de tiempo, se usan tasas:
  $$COP_{\mathrm{R}}=\frac{\dot{Q}_{\mathrm{L}}}{\dot{W}_{\mathrm{entrada}}},\qquad
  COP_{\mathrm{BC}}=\frac{\dot{Q}_{\mathrm{H}}}{\dot{W}_{\mathrm{entrada}}}$$
- Aplicando el balance del ciclo:
  $$COP_{\mathrm{BC}}=COP_{\mathrm{R}}+1$$
- El COP no es una eficiencia térmica: su valor puede ser mayor que 1 porque el equipo mueve calor del foco frío, además de utilizar trabajo. Un COP alto indica más calor útil transferido por unidad de trabajo.
- En un refrigerador, el efecto útil es extraer calor del espacio frío; en una bomba de calor, el efecto útil es entregar calor al espacio caliente. La misma máquina puede evaluarse de las dos formas.
- Con un COP y una capacidad de refrigeración conocidos, la potencia eléctrica consumida se obtiene con $\dot W_{\mathrm{entrada}}=\dot Q_{\mathrm{L}}/COP_{\mathrm{R}}$. No confundas capacidad (tasa de calor movido) con consumo eléctrico.

## Segunda Ley y límite de Carnot

- La Segunda Ley establece que ningún dispositivo cíclico puede transferir calor del foco frío al caliente sin consumir trabajo; además, ningún ciclo real puede superar el desempeño de un ciclo reversible entre los mismos focos.
- Para un ciclo reversible de Carnot que opera entre dos focos:
  $$COP_{\mathrm{R,rev}}=\frac{T_{\mathrm{L}}}{T_{\mathrm{H}}-T_{\mathrm{L}}},\qquad
  COP_{\mathrm{BC,rev}}=\frac{T_{\mathrm{H}}}{T_{\mathrm{H}}-T_{\mathrm{L}}}$$
- En estas expresiones, $T_{\mathrm{L}}$ y $T_{\mathrm{H}}$ deben estar en kelvin, con $T_{\mathrm{H}}>T_{\mathrm{L}}$. La diferencia de temperatura determina cuánto trabajo mínimo se requiere para mover una cantidad de calor.
- Si disminuye la diferencia $T_{\mathrm{H}}-T_{\mathrm{L}}$, el COP reversible aumenta. Si ambos focos están a la misma temperatura, el denominador tiende a cero: es un límite ideal, no una operación práctica con potencia finita.
- Los equipos reales son irreversibles por fricción, caídas de presión, diferencias finitas de temperatura y otras pérdidas; por eso su COP es menor que el de Carnot.
- Para una refrigeración reversible:
  $$\frac{Q_{\mathrm{H}}}{Q_{\mathrm{L}}}=\frac{T_{\mathrm{H}}}{T_{\mathrm{L}}}$$
  Junto con $Q_{\mathrm{H}}=Q_{\mathrm{L}}+W_{\mathrm{entrada}}$, esta relación conduce al COP reversible. Cualquier COP real debe ser menor que el límite correspondiente entre los mismos focos.
- Para comparar equipos que operan entre temperaturas distintas, no basta comparar sus COP reales: compáralos también con su propio COP de Carnot. Una diferencia relativa como $COP/COP_{\mathrm{rev}}$ indica cuán cerca está el dispositivo del límite ideal.

## Fronteras y escenarios de análisis

- **Refrigerador como dispositivo:** la frontera incluye la máquina. Entran trabajo y calor desde el foco frío; sale calor hacia el foco caliente.
- **Espacio refrigerado como sistema:** el calor extraído del espacio es una salida de energía térmica. Si el objetivo es mantenerlo a temperatura constante, el calor que entra desde el entorno debe ser compensado por el refrigerador.
- **Habitación con refrigerador cerrado:** el evaporador extrae calor de la habitación y el condensador lo devuelve junto con la energía eléctrica consumida. El balance neto calienta la habitación en una cantidad igual al trabajo aportado, si se desprecia el calor que cruza sus paredes.
- **Puerta abierta:** el equipo extrae calor de una zona y lo devuelve a la misma habitación con un excedente asociado al trabajo eléctrico. No puede enfriar indefinidamente la habitación completa; en el mejor caso el neto es calentamiento por el consumo.
- **Bomba de calor para calefacción:** la tasa útil es $\dot Q_{\mathrm{H}}$. Si se conoce la pérdida de calor del edificio en estado estacionario, la bomba debe suministrar una tasa igual para mantener la temperatura.
- La frontera elegida evita confundir el efecto deseado con energía interna al aparato. Dibuja siempre los focos y las flechas antes de aplicar la Primera Ley.

## Ejercicios con capacidades y energía acumulada

- Si la capacidad de refrigeración es constante durante un intervalo $\Delta t$, la energía extraída es $Q_{\mathrm{L}}=\dot Q_{\mathrm{L}}\Delta t$. Con COP constante, $W_{\mathrm{entrada}}=Q_{\mathrm{L}}/COP_{\mathrm{R}}$ y $Q_{\mathrm{H}}=Q_{\mathrm{L}}+W_{\mathrm{entrada}}$.
- Si se enfría una cantidad de sustancia cuya energía interna disminuye, combina el balance del espacio/sustancia con el COP del equipo. No confundas el calor que sale del producto con el calor total rechazado por el condensador.
- Si el sistema incluye el refrigerador y el objeto enfriado juntos, el trabajo eléctrico cruza la frontera y el calor rechazado sale; el calor transferido entre objeto y evaporador es interno y se cancela del balance del conjunto.
- Si el COP cambia con la temperatura o el proceso no está en régimen estacionario, no multipliques una capacidad nominal por el tiempo sin verificar esa hipótesis.

## Potencia, capacidad y resolución

- La **capacidad de refrigeración** suele expresarse como tasa de calor extraído, $\dot{Q}_{\mathrm{L}}$; no es lo mismo que la potencia eléctrica consumida, $\dot{W}_{\mathrm{entrada}}$.
- Con un COP conocido, puede despejarse el consumo o la capacidad:
  $$\dot{W}_{\mathrm{entrada}}=\frac{\dot{Q}_{\mathrm{L}}}{COP_{\mathrm{R}}},\qquad
  \dot{W}_{\mathrm{entrada}}=\frac{\dot{Q}_{\mathrm{H}}}{COP_{\mathrm{BC}}}$$
- Para resolver, dibuja el ciclo y marca $Q_{\mathrm{L}}$ entrando desde el foco frío, $Q_{\mathrm{H}}$ saliendo hacia el foco caliente y el trabajo de entrada. Identifica qué efecto es útil antes de elegir el COP.
- Verifica que las temperaturas usadas en las expresiones de Carnot sean absolutas y que los balances de energía cierren: $\dot{Q}_{\mathrm{H}}=\dot{Q}_{\mathrm{L}}+\dot{W}_{\mathrm{entrada}}$.
- Una potencia de refrigeración dada en toneladas de refrigeración u otra unidad debe convertirse a kW antes de combinarse con potencia eléctrica. Mantén todas las tasas en unidades consistentes.
- Prueba de posibilidad: verifica que el COP propuesto sea positivo y no exceda el límite reversible de Carnot entre los focos especificados. Un COP por encima del límite es imposible aunque el balance de energía parezca correcto.
