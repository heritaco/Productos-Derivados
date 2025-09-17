La “tasa objetivo” de un país es el precio operacional del dinero a muy corto plazo que fija su banco central para anclar el sistema nominal. Es el control directo $i_t$ en un problema de estabilización sujeto a restricciones reales y financieras.

# 1) Definición y taxonomía

* **Objeto**: tasa de política a 1–14 días que el banco central fija y defiende con operaciones de mercado abierto y facilidades. Nombres: *federal funds target range* (EE. UU.), *deposit facility rate* (zona euro), **SELIC** (Brasil), **TPM** (Chile), **tasa de referencia** O/N (México), *bank rate* (Reino Unido), *repo* (India), *OCR* (Nueva Zelanda).
* **Regímenes**:
  **a)** *Inflation targeting* con tipo de cambio flotante: $\pi_t \to \pi^\*$.
  **b)** Fijaciones cambiarias o cajas de conversión: el ancla es $s_t$ (tipo de cambio), la tasa endogeneiza la paridad.
  **c)** Objetivos de agregados monetarios o variantes de *price-level/average-inflation targeting*.

# 2) Problema de política

Minimización de pérdidas intertemporales:

$$
\min_{\{i_t\}} \; \mathbb{E}_0\sum_{t\ge0}\beta^t\Big[(\pi_t-\pi^\*)^2+\lambda x_t^2+\gamma \Delta i_t^2\Big]
$$

sujeto a

$$
\underbrace{\pi_t=\beta \mathbb{E}_t[\pi_{t+1}] + \kappa x_t + u_t}_{\text{NKPC}},\qquad
\underbrace{x_t=\mathbb{E}_t[x_{t+1}] - \sigma\big(i_t-\mathbb{E}_t[\pi_{t+1}]-r_t^\*\big)}_{\text{IS}}
$$

y a *constraints* financieros (prima de riesgo, traspaso cambiario, liquidez bancaria). La regla implementable es una **Taylor-like**:

$$
i_t \approx r_t^\* + \pi^\* + \phi_\pi(\pi_t-\pi^\*) + \phi_x x_t,\quad \phi_\pi>1.
$$

Clave: el instrumento es **nominal**, pero la transmisión opera vía la **tasa real** $r_t=i_t-\mathbb{E}_t[\pi_{t+1}]$ relativa a la **neutral** $r_t^\*$ (tiempo-variable).

# 3) Implementación operativa

Dos arquitecturas dominantes:

* **Floor system** (reservas abundantes): el piso de facilidades o la tasa de depósitos “clava” el O/N. Ej.: Fed, BCE.
* **Corredor simétrico** (reservas escasas): ventanillas de crédito/deposito acotan y OMAs ubican el O/N cerca del centro. Ej.: Banxico, varios EMEs.

Dinámica estilizada del fondeo:

$$
di^{\text{O/N}}_t = -\phi\big(i^{\text{O/N}}_t - i_t\big)\,dt + \sigma\,dW_t,\quad \phi>0.
$$

# 4) Transmisión a precios de activos y crédito

La tasa objetivo fija el extremo corto de la curva; los plazos $n$ descuentan expectativas y primas:

$$
y(t,n)\approx \frac{1}{n}\sum_{k=1}^{n}\mathbb{E}_t[i_{t+k}] + \text{TP}_n,\qquad
\text{OIS}_n \simeq \mathbb{E}_t[i] \text{ libre de crédito}.
$$

Canales: (i) costo de fondeo bancario $\to$ tasas de crédito; (ii) valoración de activos $\to$ riqueza y *risk-taking*; (iii) tipo de cambio vía paridad no cubierta con prima

$$
i_t - i_t^{\text{ext}} \approx \mathbb{E}_t[\Delta s_{t+1}] + \varphi_t.
$$

# 5) Heterogeneidad entre países

* **Economías avanzadas**: transmisión más predecible, mercados profundos, $\varphi_t$ menor; ELB/zero lower bound relevante $\Rightarrow$ balance-sheet policies.
* **Mercados emergentes**: mayor **pass-through** cambiario $(\Delta p \approx \alpha\,\Delta e)$, prima de riesgo volátil $\varphi_t$, *fear of floating* y riesgos de dominancia fiscal/financiera.
* **Dolarizadas o con *pegs***: la tasa objetivo efectiva es importada; autonomía limitada.
* **China**: multiplicidad de tasas operativas con de-facto anclas (7-day repo/LPR) y control cuantitativo del crédito.

# 6) Interfaz con la política fiscal y la estabilidad financiera

Sin consistencia fiscal, el nivel de precios puede obedecer a la **teoría fiscal del nivel de precios**:

$$
P_t=\frac{B_t}{\text{VP de superávits primarios futuros}}\;\;\Rightarrow\;\; i_t\text{ pierde tracción si hay dominancia.}
$$

Con *financial dominance*, alzas de $i_t$ pueden tensionar balances bancarios o deudores altamente apalancados, alterando la transmisión. Por eso muchos bancos centrales incorporan un término de suavizamiento $\gamma \Delta i_t^2$ y facilidades de liquidez como *lender of last resort*.

# 7) Restricciones tecnológicas

* **ELB/ILB**: cotas inferior/superior efectivas $\Rightarrow$ uso de tasas de facilidades negativas, *forward guidance*, QE/QT.
* **Medición de $r_t^\*$**: estimaciones tipo Laubach-Williams con gran incertidumbre. Decisiones robustas requieren bandas, no puntos.
* **Expectativas**: comunicación y credibilidad anclan $\mathbb{E}_t[\pi]$. Sin ellas, el multiplicador de la regla cae.

# 8) Derivados y revelación de expectativas

Los **FRA**, **IRS** y futuros sobre O/N codifican la trayectoria implícita de $i_t$:

$$
\text{ParSwap}_T \approx \frac{\sum_i \Delta_i\,\mathbb{E}_t[i_{t+i}]\,DF_i}{\sum_i \Delta_i\,DF_i}.
$$

La comparación entre la curva implícita y la guía oficial detecta **sorpresas** y el grado de credibilidad.

# 9) Diagnóstico operativo universal

* Si $r_t<r_t^\*$ de forma persistente $\Rightarrow x_t>0 \Rightarrow \pi_t\uparrow$.
* Si $r_t>r_t^\*$ $\Rightarrow$ enfriamiento y desinflación.
* Choques de oferta $u_t$ exigen distinguir **nivel** vs **tendencia**: *no todo salto de precios amerita subir*.

# 10) Síntesis

$$
\boxed{\text{La tasa objetivo es el ancla de corto plazo del sistema nominal. Su eficacia}=\text{función}\big(\text{credibilidad},\,r_t^\*,\,\text{fiscal},\,\varphi_t,\,\text{microestructura}\big).}
$$

> Wicksell: “Cuando la tasa de mercado cae por debajo de la natural, los precios suben; por encima, bajan.”
> Friedman: “Actúa con rezagos largos y variables”; por eso el *timing* y la comunicación son parte del instrumento.

En cualquier país, el arte consiste en fijar $i_t$ para que la tasa **real** converja alrededor de $r_t^\*$ mientras se mantienen ancladas las expectativas de inflación y se contiene la prima de riesgo. El resto es ingeniería de balance y de mercado para que esa señal atraviese la tubería sin perderse.
