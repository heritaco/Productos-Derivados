Respuesta corta: combinan mandato legal, costo social de la inflación y riesgo de piso efectivo. Eligen un $\pi^{*}>0$ que minimiza pérdidas esperadas y sea fácil de comunicar. México: punto 3% con banda $\pm1\%$.

# Procedimiento típico

1. **Quién decide**

   * La ley fija el mandato (“estabilidad de precios”).
   * El **número** lo define: gobierno+banque central por acuerdo (p. ej. remit), o el banco central de forma autónoma. Se revisa esporádicamente.

2. **Criterio económico (pérdidas sociales)**
   Regla de diseño como problema de control:

   $$
   \min_{\pi^{*}}\ \mathbb E\sum_{t}\Big[(\pi_t-\pi^{*})^2+\lambda_x x_t^2+\lambda_i(\Delta i_t)^2\Big]\;+\;\lambda_{ZLB}\Pr(i_t\le \underline i).
   $$

   El $\pi^{*}$ óptimo equilibra cuatro fuerzas.

3. **Cuatro fuerzas que fijan $\pi^{*}$**

   * **Sesgo del IPC** ($b>0$): calidad, sustitución, alquiler imputado. Si el índice **sobre-mide** la inflación en $b$, elegir $\pi^{*}\approx b$ evita forzar deflación “real”.
   * **Riesgo de piso efectivo (ZLB/ELB)**: con $i_t^{\text{ss}}=r_t^{*}+\pi^{*}$, metas muy bajas elevan $\Pr(i_t\!\le\!\underline i)$. Se elige $\pi^{*}$ tal que

     $$
     \Pr\big(r^{*}+\pi^{*}\le \underline i\big)\le \tau,
     $$

     con $\tau$ umbral tolerado. Mayor incertidumbre sobre $r^{*}$ ⇒ $\pi^{*}$ algo mayor.
   * **Rigideces nominales**: precios y salarios pegajosos. Un $\pi^{*}>0$ facilita **ajustes reales** sin recesión prolongada.
   * **Costos de inflación tendencial**: distorsiones tributarias no indexadas, “menu costs”, dispersión de precios relativos. Crecen **convexamente** con $\pi^{*}$ ⇒ se prefiere $\pi^{*}$ bajo.

   Balance típico: $b\sim 0.3\!-\!1.0$ pp, riesgo ZLB no trivial, rigideces relevantes ⇒ $\pi^{*}$ alrededor de **2–3%** en economías avanzadas. Economías abiertas con alto “pass-through” mantienen el **mismo rango**, pero usan **bandas** para choques de FX/energía.

4. **Ancho de banda y simetría**
   Meta puntual con **banda simétrica** (p. ej. $\pm1\%$) para absorber choques y sancionar desvíos **por arriba y por abajo**. La simetría ancla expectativas.

5. **Comunicación y verificabilidad**
   Número **redondo** y estable, calendario de reportes, proyecciones a 8–12 trimestres, explicación de desvíos y horizonte de convergencia. Credibilidad > fine-tuning.

6. **México (referencia)**
   Banxico comunica **3%** con intervalo de **variabilidad $\pm1\%$**. Punto central bajo, pero no tan bajo que eleve el riesgo ELB. La banda reconoce choques transitorios en energéticos y tipo de cambio.

---

## Resumen formal

* Estado estacionario: $i^{\text{ss}}=r^{*}+\pi^{*}$.
* Diseño: $\pi^{*}\approx b + \text{colchón}_{\text{ELB}}$, sujeto a costos convexos de inflación tendencial.
* Operación: regla tipo-Taylor para minimizar $\mathbb E[(\pi_t-\pi^{*})^2+\lambda_x x_t^2]$ sin tocar el ELB con frecuencia.

**Idea central**: la meta se fija **positiva y baja** para balancear medición, rigideces y el riesgo de quedarse sin munición nominal.
