---
tags:
  - certamen1_termo
seguimiento_certamen1: true
progreso_certamen1: true
bloque_certamen1: Gas ideal y sistemas cerrados
---

# Práctico 4 — Sistemas cerrados

[Listado del práctico](../02_Ejercicios_y_Guias/Pr%C3%A1cticaNr4_Termodin%C3%A1mica_2026-2%20%281%29.pdf) | [Solucionario](../02_Ejercicios_y_Guias/Pr%C3%A1cticaNr4SOLUCION_Termodin%C3%A1mica_2026-2.pdf) | Siguiente: [Práctico 5](./pr%C3%A1ctica%205.md)

## Definición y energía almacenada

- Un sistema cerrado contiene una cantidad fija de masa. No hay flujo de masa a través de su frontera; sí puede haber calor y/o trabajo.
- Su energía total es:
  $$E=U+E_{\mathrm{c}}+E_{\mathrm{p}}$$
  Por tanto, entre dos estados $\Delta E=\Delta U+\Delta E_{\mathrm{c}}+\Delta E_{\mathrm{p}}$. Si los cambios de velocidad y altura son despreciables, $\Delta E\approx\Delta U$.
- Las propiedades de estado se evalúan en los estados inicial y final. Calor y trabajo no son propiedades almacenadas: son interacciones que ocurren durante el proceso.

## Primera Ley y convención de signos

- Se usará $Q>0$ cuando el calor entra al sistema y $W>0$ cuando el sistema realiza trabajo sobre el entorno. Con esta convención:
  $$\Delta E=Q-W$$
- Si se separan las interacciones por dirección:
  $$\Delta E=Q_{\mathrm{entrada}}-Q_{\mathrm{salida}}+
  W_{\mathrm{entrada}}-W_{\mathrm{salida}}$$
- Ambas expresiones son equivalentes, siempre que los signos se apliquen de forma coherente. Si se usa otra convención, debe mantenerse en todo el desarrollo.
- La forma general entre estados es:
  $$U_2-U_1+E_{\mathrm{c},2}-E_{\mathrm{c},1}
  +E_{\mathrm{p},2}-E_{\mathrm{p},1}=Q-W$$
- **Adiabático** significa $Q=0$, no que la temperatura o energía interna sean constantes. Una compresión adiabática puede aumentar la energía interna por trabajo realizado sobre el gas. **Isotérmico** significa temperatura constante, pero no implica necesariamente $Q=0$.

## Trabajo de frontera

- En un proceso cuasiequilibrio, el trabajo de frontera de expansión o compresión es:
  $$W_{\mathrm{b}}=\int_{V_1}^{V_2}p_{\mathrm{ext}}\,dV$$
  Para un proceso cuasiestático, la presión en la frontera se aproxima por la presión del sistema. Con $W>0$ hecho por el sistema, una expansión produce trabajo positivo; una compresión produce trabajo negativo.
- El trabajo es el área bajo la trayectoria en un diagrama $p-v$ (o $P-V$). Depende del camino seguido, por lo que distintos procesos entre los mismos estados pueden intercambiar diferente trabajo.
- A presión constante:
  $$W_{\mathrm{b}}=p(V_2-V_1)$$
- En un recipiente rígido, $V_2=V_1$ y no hay trabajo de frontera. Esto no excluye otros tipos de trabajo, como el eléctrico o el de eje.
- El trabajo total puede contener varias contribuciones: $W=W_{\mathrm{b}}+W_{\mathrm{eléctrico}}+W_{\mathrm{eje}}+\cdots$. Con la convención adoptada, el trabajo que el entorno suministra al sistema es negativo en el balance $Q-W$.

## Trayectoria del proceso y trabajo

- Para evaluar $W_{\mathrm{b}}$, se necesita cómo varía la presión durante el cambio de volumen. No basta conocer únicamente los estados extremos, salvo que se especifique la trayectoria o una ley que la determine.
- Para un resorte lineal, la fuerza del resorte y la presión del gas pueden cambiar con el desplazamiento del pistón. Si la presión varía linealmente con el volumen, el trabajo es el área trapezoidal:
  $$W_{\mathrm{b}}=\frac{p_1+p_2}{2}(V_2-V_1)$$
  siempre que la presión de frontera siga esa variación lineal.
- Para un proceso politrópico idealizado $pV^n=C$, con $n\ne1$:
  $$W_{\mathrm{b}}=\frac{p_2V_2-p_1V_1}{1-n}$$
  Para $n=1$ (isotérmico ideal):
  $$W_{\mathrm{b}}=p_1V_1\ln\left(\frac{V_2}{V_1}\right)$$
  Estas expresiones requieren que el proceso siga realmente la relación indicada y que el trabajo de frontera pueda modelarse como cuasiestático.
- En un proceso irreversible, el trabajo de frontera se calcula con la presión externa que resiste el movimiento, no necesariamente con la presión uniforme del sistema. Un caso típico es la expansión contra una presión externa constante.

## Casos frecuentes

- **Volumen constante y sin otros trabajos:** $W=0$ y $\Delta U=Q$ si se desprecia energía cinética y potencial.
- **Adiabático y sin cambios cinéticos o potenciales:** $\Delta U=-W$. El trabajo hecho sobre el sistema (trabajo negativo en esta convención) aumenta su energía interna.
- **Presión constante con solo trabajo de frontera:** $Q=\Delta H$ para un sistema cerrado simple compresible, si los cambios de energía cinética y potencial son despreciables. Esta igualdad requiere esas hipótesis; no es una identidad universal.
- **Resorte o carga eléctrica:** contabiliza el trabajo correspondiente por separado. El calentamiento eléctrico puede elevar la temperatura aunque el recipiente sea rígido y adiabático.

## Interpretación de configuraciones de los ejercicios

- **Cilindro-pistón adiabático comprimido:** no cruza calor ($Q=0$), pero puede entrar trabajo al gas. Si se desprecia energía cinética/potencial, $\Delta U=-W$ con trabajo positivo hecho por el sistema; durante la compresión $W<0$, por lo que normalmente $\Delta U>0$.
- **Calentamiento con pistón móvil y topes:** mientras el pistón se mueve, el gas desplaza la frontera y realiza trabajo; si la carga es constante, la presión puede ser constante. Al tocar los topes, $dV=0$ y cesa el trabajo de frontera. Analiza cada tramo y suma los cambios de energía.
- **Cilindro con resistencia eléctrica:** el trabajo eléctrico que ingresa al sistema es una entrada de energía. Si el cilindro es rígido y adiabático, $W_{\mathrm{b}}=0$ y $Q=0$, pero no todo el trabajo es cero: hay trabajo eléctrico.
- **Refrigerador dentro de una habitación:** si el sistema es el aire de la habitación, el refrigerador extrae calor de ese mismo aire y luego rechaza al aire más calor porque añade el trabajo eléctrico. Con las puertas cerradas, el recinto tiende a calentarse; analiza el conjunto refrigerador-habitación si se busca el balance total.
- **Recipiente rígido dividido en compartimentos:** cada compartimento puede intercambiar calor con el otro aunque la pared exterior esté aislada. Para cada compartimento, el calor intercambiado tiene signo opuesto; para el conjunto, esa transferencia es interna y se cancela.

## Conexión con propiedades de la sustancia

- Una vez calculada $\Delta U$, debe relacionarse con los estados. Para una sustancia pura se obtienen $u_1,u_2$ de tablas; para un gas ideal, $u$ depende principalmente de la temperatura.
- Para un gas ideal con calor específico constante en un intervalo:
  $$\Delta U=m c_v(T_2-T_1)$$
  y, análogamente, $\Delta H=m c_p(T_2-T_1)$. Si el intervalo de temperatura es amplio, los calores específicos varían y se usan valores tabulados o integrales.
- No concluyas que $Q=0$ porque el recipiente esté aislado térmicamente si existe trabajo eléctrico, de eje o de frontera. El aislamiento elimina calor, no todas las interacciones.

## Procedimiento de resolución

1. Define la frontera y confirma que la masa permanece fija.
2. Escribe todos los intercambios como calor o trabajo; incluye trabajo de frontera y otros trabajos si existen.
3. Selecciona una sola convención de signos y aplica $\Delta E=Q-W$.
4. Elimina cambios cinéticos, potenciales o transferencias solo si el enunciado o los datos permiten despreciarlos.
5. Obtén el trabajo con la trayectoria adecuada: integral, área bajo la curva o expresión de proceso especificada.
6. Relaciona $\Delta U$ con propiedades de estado usando tablas o un modelo de sustancia apropiado.
7. Revisa el signo del resultado: expansión, compresión, calentamiento y enfriamiento deben ser consistentes con el balance planteado.
