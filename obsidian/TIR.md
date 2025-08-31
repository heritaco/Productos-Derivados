La **TIR** aquí es la **tasa de interés de referencia de Banxico**: la **tasa objetivo overnight** que el banco central fija y defiende operativamente para anclar el costo del dinero a 1 día. Es el **control** primario del sistema monetario mexicano.

# Qué es

* Variable de política $i_t$ definida por la Junta de Gobierno como meta para el fondeo interbancario O/N.
* Se implementa con **operaciones de mercado abierto** y un **corredor de facilidades** $[i_t^{D},\,i_t^{L}]$ que acota la TIIE de Fondeo:

$$
i_t^{D}\le i_t^{\text{O/N}}\le i_t^{L},\quad i_t\approx \mathbb E[i_t^{\text{O/N}}].
$$

# Mecanismo operativo mínimo

1. Banxico estima la **liquidez estructural** del sistema.
2. Inyecta o retira reservas para que el fondeo efectivo gravite en torno a $i_t$.
3. El corredor $i_t^{L}-i_t^{D}$ y las **señales prospectivas** disciplinan desviaciones intradía.

Formalización simple del fondeo:

$$
di_t^{\text{O/N}}=-\phi\big(i_t^{\text{O/N}}-i_t\big)\,dt+\sigma\,dW_t,\quad \phi>0.
$$

El término de “mean reversion” representa la acción diaria de política.

# Transmisión a la curva y a la economía

La TIR fija el **extremo corto** de la curva; el resto son **expectativas** más primas de plazo:

$$
\text{TIIE}_{n}\approx \frac{1}{n}\sum_{d=1}^{n}\mathbb{E}_t[i^{\text{O/N}}_{t+d}] + \Pi_n.
$$

El canal macro se resume con el bloque nuevo-keynesiano:

$$
\pi_t=\beta\mathbb E_t[\pi_{t+1}] + \kappa\,x_t + u_t,\qquad
x_t=\mathbb E_t[x_{t+1}] - \sigma\big(r_t-\mathbb E_t[\pi_{t+1}]-r_t^\*\big).
$$

Si la **tasa real** $r_t=i_t-\mathbb E_t[\pi_{t+1}]$ cae por debajo de la **neutral** $r_t^\*$, la demanda se acelera $(x_t>0)$ y aumenta la presión inflacionaria. El signo se invierte si $r_t>r_t^\*$.

# Regla de reacción y el “ancla”

Regla tipo Taylor empírica:

$$
i_t \approx r^\* + \pi^\* + \phi_\pi(\pi_t-\pi^\*) + \phi_x x_t + \varepsilon_t,\quad \phi_\pi>1.
$$

* $r^\*$: tasa real neutral, tiempo-variable.
* $\pi^\*$: objetivo de inflación.
* $\varepsilon_t$: choques discretos de riesgo financiero o cambiario que ameritan ajustes tácticos.

# Interfaz con el tipo de cambio y el riesgo

Paridad descubierta con prima:

$$
i_t - i_t^{\text{ext}} \approx \mathbb E_t[\Delta s_{t+1}] + \varphi_t.
$$

Un aumento de TIR tiende a apreciar el peso si reduce $\varphi_t$ y mejora el carry ajustado por riesgo. La magnitud depende de liquidez global y balances locales.

# Derivados y precio del dinero

* **IRS TIIE**: el swap par a vencimiento $T$ es el promedio descontado de TIIE futuras.
* **F-TIIE** y **FRAs**: extraen la trayectoria implícita de $i_t$.
* **Bonos flotantes**: transmiten la TIR al costo de crédito.

Descuento continuo bajo Hull–White para ilustrar expectativas:

$$
dr_t = a(b-r_t)dt+\sigma dW_t,\quad
P(t,T)=\exp\Big(A(t,T)-B(t,T)r_t\Big).
$$

Un shock $+\Delta i_t$ desplaza $r_t$ y, por $B(t,T)$, reprueba toda la curva corta.

# Riesgos de diseño

* **Dominancia fiscal**: si la trayectoria de superávits primarios esperados no respalda la deuda, el nivel de precios sube y neutraliza parte del endurecimiento monetario.
* **Microestructura**: estrés de liquidez eleva $\Pi_n$ y abre “basis” entre TIIE, fondeo y swaps.
* **Expectativas**: si no están ancladas, $\beta\mathbb E_t[\pi_{t+1}]$ domina y la TIR pierde tracción.

# Lectura hermenéutica

La TIR funciona como **operador de selección** en un espacio de trayectorias nominales: elige, entre muchas historias posibles del precio del dinero, aquella compatible con estabilidad. Es una **condición de contorno** sobre el sistema macro que disciplina narrativas privadas de precios, salarios y crédito. Sin consistencia fiscal y credibilidad comunicacional, el operador pierde unicidad.

# Heurística decisional

* Shock de **demanda** persistente → $i_t\uparrow$.
* Shock **transitorio** de oferta con expectativas ancladas → paciencia.
* Episodios de **desanclaje** o **depreciación desordenada** → $i_t\uparrow$ y guía más dura.

# En una línea

$$
\boxed{\text{La TIR es el ancla operacional del precio del dinero; su potencia real depende de expectativas y coherencia fiscal.}}
$$

> Wicksell: “La estabilidad requiere alinear la tasa de mercado con la natural.”
> Friedman: “La política monetaria actúa con rezagos largos y variables.”


1. **Liquidez estructural**
   Saldo **persistente** de déficit o superávit de **reservas bancarias** generado por factores autónomos del sistema de pagos y del fisco. Determina cuánto debe inyectar o drenar el banco central para que el O/N converja al objetivo.

2. **Reservas**
   a) **Bancarias**: depósitos de los bancos en el banco central usados para pagos y para el **encaje**. Son el “dinero de alto poder” del sistema.
   b) **Internacionales**: activos externos del banco central en divisas y oro usados para estabilidad financiera y operativa cambiaria.

3. **Corredor**
   Rango operativo de tasas fijado por facilidades permanentes. Notación típica:

$$
i^{D}\le i^{\text{O/N}}\le i^{L},
$$

donde $i^{D}$ es la tasa de depósito y $i^{L}$ la de préstamo del banco central.

4. **Señales prospectivas**
   Comunicación de **trayectoria futura** de la política monetaria. También llamado **forward guidance**. Alinea expectativas $\mathbb E_t[i_{t+k}]$ y comprime volatilidad.

5. **Fondeo**
   Obtención de pasivos de corto plazo para financiar activos o liquidez operativa. Incluye **interbancario O/N**, **repo**, pagarés y líneas con el banco central.

6. **Regla de Taylor**
   Heurística para la tasa objetivo:

$$
i_t \approx r^\*+\pi^\*+\phi_\pi(\pi_t-\pi^\*)+\phi_x x_t,\quad \phi_\pi>1,
$$

con $r^\*$ tasa real neutral, $\pi^\*$ objetivo de inflación y $x_t$ brecha de producto.

7. **Paridad**
   Relación entre tasas y tipo de cambio.

* **CIP** (cubierta):

$$
F=S\frac{1+i_d}{1+i_f},
$$

sin arbitraje al cubrir FX.

* **UIP** (descubierta):

$$
i_d-i_f \approx \mathbb E_t[\Delta s_{t+1}] + \varphi_t,
$$

con $\varphi_t$ prima de riesgo.

8. **Carry ajustado**
   Rendimiento esperado por diferenciales de tasa **después** de costos y riesgo. Ejemplo simple no cubierto:

$$
\text{carry} \approx i_d-i_f-\mathbb E_t[\Delta s],
$$

y ajustado por riesgo $\approx \frac{\text{carry}}{\sigma}$ o por VaR.

9. **Liquidez global**
   Capacidad agregada del sistema financiero mundial para proveer balance y crédito a bajo costo. Depende de política de bancos centrales sistémicos, condiciones en USD, apalancamiento de intermediarios y apetito de riesgo.

10. **Balances locales**
    Estructura de activos, pasivos y capital de bancos y no bancos domésticos. Restricciones como **LCR**, **NSFR**, razón préstamos-depósitos y colaterales disponibles determinan spreads y la transmisión de tasas.
